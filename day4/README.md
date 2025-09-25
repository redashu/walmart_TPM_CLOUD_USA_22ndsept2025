# walmart_TPM_CLOUD_USA_22ndsept2025

### Revision 

<img src="rev1.png">

### some info about Nosql 

<img src="rev2.png">

### Understanding of metrics 

<img src="mtr1.png">

### =====

# Latency, Throughput, Uptime

| **Concept**  | **Meaning (Simple)**                          | **TPM’s Perspective (User Impact)**        | **Example (Azure & GCP)**                                  |
|--------------|-----------------------------------------------|--------------------------------------------|------------------------------------------------------------|
| **Latency**  | Time it takes for a request to get a response | High latency → users feel app is “slow”    | Azure Front Door latency optimization; GCP Cloud CDN edge caching |
| **Throughput** | Number of requests system can handle per second | Low throughput → app crashes or queues during peak load | Azure Event Hubs for high-ingestion; GCP Pub/Sub            |
| **Uptime**   | % of time service is available                | Downtime = lost business, broken trust     | Azure guarantees 99.95% uptime for VMs; GCP BigQuery ~99.99% |

💡 **User view analogy:**
- **Latency** = waiting in line for service  
- **Throughput** = how many counters are open  
- **Uptime** = whether the shop is even open  

---

# SLAs, SLOs, SLIs

These are often mixed up, but think of them as **Promise → Goal → Measurement.**

| **Term** | **Meaning** | **Example in Azure / GCP** | **TPM Relevance** |
|----------|-------------|-----------------------------|-------------------|
| **SLA (Service Level Agreement)** | Formal contract from provider to customer | Azure SQL DB: 99.99% SLA | TPM ensures product meets external commitments |
| **SLO (Service Level Objective)** | Internal target set by the team | “We aim for <200ms latency 95% of the time” | Helps TPM guide team priorities & focus |
| **SLI (Service Level Indicator)** | Actual metric measured | “This week, average latency was 180ms” | TPM tracks SLIs to ensure SLOs are met |

💡 **Analogy for TPMs:**
- **SLA** = Promise to the customer  
- **SLO** = Team’s performance goal  
- **SLI** = Speedometer (real-time truth)  

---

# ✅ What TPMs should monitor:
- Latency spikes (**signals bad user experience**)  
- Throughput drops (**signals scaling issues**)  
- Uptime dips (**signals availability risk**)  
- SLI vs SLO gaps (**signals commitments at risk**)  