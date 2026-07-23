# Problem Charter

**Week:** 1  
**Owner(s):** A.ASHWINI, D.Srija, T.Akshaya
**Project:** ChargeIQ — EV Station Utilization Analytics 

---

## 1. Problem Context

Explain the domain in simple language.
Electric Vehicle (EV) charging infrastructure is expanding, but utilization remains uneven. Some stations are idle while others face congestion, leading to poor customer experience and inefficient resource planning. Raw usage data alone is not enough — it must be transformed into trusted insights to support decision-making.

Prompts:

- What real-world process does this project represent?
- What kinds of data are generated?
- Why is raw data not enough?
- Who would use the final dashboard or metrics?

---

## 2. Engineering Problem

Develop a Databricks data pipeline that converts raw EV charging data into Bronze, Silver, Gold, and dashboard-ready outputs with data quality checks and streaming support.

The pipeline must:  
- Ingest multiple raw source files into Bronze.  
- Apply transformations and cleaning in Silver.  
- Perform data quality checks.  
- Generate Gold outputs with KPIs.  
- Feed Power BI dashboards and streaming simulations.  

Example format:

> The project must convert multiple raw source files into trusted Bronze, Silver, Data Quality, Gold, and dashboard-ready outputs using Databricks and Power BI.

---

## 3. Users / Stakeholders

| User / Stakeholder | What they need from the data |
| EV Owners | Reliable access to charging stations |
| Station Operators | Monitor usage and reduce congestion |
| Energy Providers | Balance grid demand |
| City Planners | Plan infrastructure expansion |
| Analysts | Compare trends and investigate failures |

| [Example: Operations Head] | [Example: View daily demand and service issues] |
| [Example: Analyst] | [Example: Compare trends and investigate failures] |

CISO:	View cyber risk and trends
SOC: Manager	Monitor alerts and false positives
Incident Response Lead:	Track response time and SLA
SOC Analyst:	Monitor live security alerts


---

## 4. Scope Inclusions

List what the team will build.

Synthetic data generation
Bronze ingestion
Silver transformation
Data quality checks
Gold metrics
Power BI dashboard
Streaming simulation
GitHub documentation

---

## 5. Scope Exclusions

List what the team will not build.
- No real EV data  
- No production deployment  
- No hacking or penetration testing  
- No copied projects  
- No unexplained AI-generated work 


Examples:

No real cybersecurity data
No production deployment
No hacking or penetration testing
No copied projects
No unexplained AI-generated work

---

## 6. Success Criteria

By the end of 12 weeks, the project is successful if:

- The pipeline can be explained end to end.
- The team can show Bronze, Silver, DQ, Gold, dashboard, and streaming evidence.
- All three students can explain the full project at a high level.
- GitHub contains weekly evidence and final submission files.
