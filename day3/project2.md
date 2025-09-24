# 📝 Group Task: System Design for File Storage & Sharing Platform

## 🎯 Task Objective

Design a web-based file storage & sharing platform (like a simplified Google Drive/Dropbox) on the whiteboard.

- Users can authenticate and upload files
- Files are stored securely
- Users can share files with others
- **Goal**: Collaborate as a group to draw and explain the design, trade-offs, and choices

## 📌 Requirements

### Functional Requirements
- **User Authentication**
  - Users must sign in (email/password, SSO, or OAuth)
- **File Upload/Download**
  - Users can upload files (PDF, images, docs)
  - Users can download their files
- **File Sharing**
  - User can share file via link or by email access control
- **Web UI**
  - Simple UI for login, upload, list files, and share

### Non-Functional Requirements
- **Scalability** → Should handle millions of users
- **Reliability** → Files should not be lost
- **Security** → Only authorized users can access their files
- **Performance** → Upload/download should be fast
- **Cost efficiency** → Optimize storage & network usage

## 🏗️ Suggested System Design Components

### Frontend (Web UI)
- HTML/CSS/JS or React-based web app
- Calls backend APIs

### Authentication Service
- OAuth 2.0 / JWT tokens
- Could use Identity Provider (e.g., Auth0, Firebase Auth, Cognito)

### API Gateway / Load Balancer
- Routes traffic to backend services
- Provides rate-limiting & logging

### Backend Service (App Layer)
- REST/GraphQL APIs to handle file upload, metadata, and sharing
- Runs on App Engine, Cloud Run, or Kubernetes

### Storage Layer
- **Files** → Object Storage (e.g., GCP Cloud Storage, AWS S3, Azure Blob)
- **Metadata** → Relational DB (e.g., PostgreSQL/MySQL) for user-file mapping

### File Sharing Mechanism
- Generate signed URL (time-limited)
- OR maintain ACLs in DB for user-based access

### CDN / Caching Layer
- To accelerate file downloads
- Example: Cloud CDN, CloudFront, Azure CDN

### Monitoring & Logging
- Track usage, failures, and security events

## 🖼️ Whiteboard Layout (Hint for TPMs)


**Extras**: CDN in front of Storage for faster delivery

## 💡 Group Discussion Prompts

1. **Which cloud provider service would you pick for storage?** (S3 vs Blob vs GCS)
2. **Would you use SQL or NoSQL for file metadata? Why?**
3. **How to enforce file access security?** (signed URL vs DB ACL)
4. **How to make system scalable across regions?**
5. **Trade-off**: Consistency vs Availability (CAP theorem) — which is more important here?

## ✅ Deliverable from TPMs

- A whiteboard diagram with 5–7 core blocks (Auth, API, Storage, DB, CDN, Users)
- Explanation of design choices & trade-offs
- Identify future enhancements (versioning, search, collaboration features)