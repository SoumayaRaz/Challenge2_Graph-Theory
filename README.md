# 📧 Zero Email 
*A Data Science Project on Reducing Email Overload in the Workplace*

[![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)](https://www.python.org/)  
[![Project Status](https://img.shields.io/badge/Status-Completed-brightgreen)]()  

---

## 🧾 Overview

Email overload is a growing challenge in modern organizations, leading to technostress, reduced productivity, and blurred work-life boundaries.  
**This project applies data science techniques to analyze and reduce email overload** using communication data from a consulting firm over a 2-week period.

We model email exchanges as a graph, detect communication inefficiencies, and propose organizational changes based on:

- Network centrality
- Community detection
- Behavioral patterns

---

## 📁 Data Description

- 📅 **Period**: March 4 to March 19, 2019  
- 🧑‍💼 **Scope**: Internal & external email communications  
- 📦 **Size**: 1,174,928 messages  
- 📄 **Key fields**:
  - `Sender`, `Recipient`, `Timestamp`
  - `MessageSize`, `Subject`
  - `Grade` (employee rank)
  - `Direction` (sent or received)
  - `PartnerType` (internal or external)

---

## 🧹 Data Preparation

✅ Cleaned and renamed columns for consistency  
✅ Mapped collaborator IDs to grades  
✅ Focused on **sent emails** to model directionality  
✅ Filtered and restructured for graph modeling

> Example of graph edge:  
> **Node A (Manager)** → **Node B (Staff)** | Weight = Number of emails sent

---

## 🧠 Models

### 🟢 1. Degree Centrality
Identify the most active **senders and receivers**.  
High centrality = possible communication bottlenecks.

### 🔵 2. Louvain Community Detection
Cluster users into **communication groups** or silos.  
Helps identify redundant or inefficient communication loops.

---

## 🧪 Evaluation

### ✅ Scenario 1: Time Restrictions
⏰ Block emails sent **outside work hours or on weekends**  
📉 **Result**: 8.5% reduction in total email volume

### ✅ Scenario 2: High-Volume Nodes
📬 Cap over-active senders and route messages through **collaborative tools**  
📉 **Result**: 6.05% reduction in total emails sent

### ✅ Scenario 3: Community Insights
👥 Identify mass announcements & propose **group channels (Slack, Teams)**  
📉 Reduce repetitive multi-recipient messages

---

## 📊 Key Findings

| Indicator              | Before      | After       | % Reduction |
|------------------------|-------------|-------------|-------------|
| Total Emails Sent      | 309,088     | 282,595     | **-8.5%**   |
| Emails Outside Hours   | 20,600      | 0           | **-100%**   |
| Daily Emails/Employee  | 13.44       | 12.28       | **-8.6%**   |
| Broadcast Overlap      | High        | Reduced     | ✓           |

---

## 💡 Key Insights

- **Staff** members are the central nodes in communication
- Most emails are **intra-organizational** and **cross-hierarchical**
- Several emails have **large distributions** that can be handled via shared drives or chat platforms
- Workload and stress indicators emerge clearly from **temporal and volume-based patterns**

---

## 🧾 Conclusion

Through graph analysis and communication modeling, this project:

- Identified **email bottlenecks** and overload drivers
- Proposed **policy changes** (email timing, sender limitations)
- Suggested the use of **collaboration tools** to streamline information flow

> 🧠 This combination of network science and behavioral insights provides a scalable framework to **improve digital communication** in any organization.

---

## 👥 Authors

- 👤 **Soumiya Razzouk**  
- 👤 **Hamidou Kane**  
- 👤 **Alexandre Kessler**  
📚 UE GTSMA | 📅 June 2, 2024

---

## 📁 Repository Structure

```bash
📦 zero-email-project/
├── dataset/
├── Notebook
├── Report
└──README.md

