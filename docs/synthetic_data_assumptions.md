# Synthetic Data Assumptions

**Week:** 2  
**Purpose:** Document how educational data is created.

---

## 1. Synthetic Data Boundary

This project uses **synthetic EV charging infrastructure and operational data** created solely for educational and learning purposes. The dataset does **not** represent any real charging network, company, customer, vehicle owner, government agency, manufacturer, or utility provider. All station names, charger IDs, maintenance records, charging sessions, and streaming events are fictional and generated for data engineering practice.

---

## 2. Domain Assumptions

| Area | Assumption |
|------|------------|
| Geography / Scope | Fictional EV charging stations across major Indian cities (Hyderabad, Bengaluru, Pune, etc.) |
| Time Period | January 2026 – April 2026 |
| Source Systems | Station Master, Charger Management System, Charging Session System, Maintenance Management System, Streaming Event Producer |
| Event Types | Charging session, maintenance event, charger status update, fault, recovery |
| Reference Data | Stations, chargers, connector types, vehicle classes, tariff bands |

---

## 3. Data Volume Assumptions

| File | Approximate Rows | Reason |
|------|-----------------:|--------|
| `stations.csv` | 180 | Represents EV charging station master data |
| `chargers.json` | 1,200 | Multiple chargers available at each station |
| `sessions.parquet` | 300,000 | Large historical charging session dataset for analytics |
| `maintenance.csv` | 18,000 | Maintenance and fault history for chargers |
| `charger_status_event_drop_01.json` | Streaming events | Simulates real-time charger status updates |
| `charger_status_event_drop_02.json` | Streaming events | Simulates incremental streaming events with duplicates and late arrivals |

---

## 4. Controlled Data Quality Issues

| Issue Type | Approx. Share | Why Include It |
|------------|---------------|----------------|
| Duplicate IDs | 0.2%–0.5% | Tests duplicate detection and deduplication |
| Missing Values | 1%–3% | Tests completeness validation |
| Invalid Reference Keys | 0.5%–1% | Tests referential integrity between stations and chargers |
| Negative / Impossible Values | 0.1%–0.5% | Tests validation rules for energy, power, and capacity |
| Timestamp Inconsistencies | 0.1%–0.3% | Tests event sequencing and chronological validation |

---

## 5. Manual Verification

Before using the generated data, the team must verify that:

- Row counts match the expected dataset sizes.
- Primary and foreign key fields are present and valid.
- Date, timestamp, and numeric values are within realistic ranges.
- Controlled data quality issues exist but do not dominate the dataset.
- Source files have sufficient structural differences to require Bronze-to-Silver standardization.
- Streaming event files follow the expected event order and schema.
