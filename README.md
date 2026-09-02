# Power BI Portfolio – Januss Barila

**Business Intelligence | Data Visualisation | Dashboard Design**

---

## ⚠️ Important Note on Data Privacy

Most of my Power BI work involves **sensitive business data** – including HR metrics, financial performance, workforce analytics, and company turnover information. Due to **GDPR and data confidentiality obligations**, I cannot share full dashboards or real datasets.

Instead, this portfolio contains:
- **Templates (.pbit)** – report structures, measures, and data models (no actual data)
- **Sample visualisations** – cropped or anonymised screenshots
- **Project descriptions** – explaining the business problem, approach, and outcomes

This approach allows you to see my **design thinking, DAX logic, and modelling approach** while fully respecting data privacy.

---


# Power BI Test Assignment – Data Analyst Submission

This project was completed as a **Power BI technical test assignment**. The goal was to import, clean, model, and visualise a fictitious transactional dataset, and present key business findings in a clear, interactive dashboard.

---

## 📊 Dashboard Preview

<img width="731" height="408" alt="image" src="https://github.com/user-attachments/assets/45f91786-8ea8-489c-b27b-d48bf6d45a01" />

---

## 🛠️ What I Did

### 1. Data Preparation & Cleaning
- Removed 640 **fully duplicate rows** – kept rows where only part of the row was duplicated because one invoice can contain several valid lines.
- Removed **5 completely empty columns** and **3 columns that were 97–99% empty**.
- Replaced missing descriptive values with `"Unknown"` to keep financial data intact.
- Kept **negative amounts** – they represent adjustments, credits, or corrections.
- Created a unified reporting currency: `Amount_EUR = net_amount_currency × curr_rate`.
- Created `BillingDate` and `ServiceDate` using the **first day of each month** (since the source only provided year and month).
  
<img width="561" height="343" alt="image" src="https://github.com/user-attachments/assets/acfec419-8463-44ee-930c-8cd5ce18d8e4" />


### 2. Data Modelling
- Designed a **star schema** with `FactInvoiceDetails` at the centre and separate dimension tables for:
  - Date
  - Product
  - Country
  - Distribution Channel
  - Reach
  - Itinerary
  - Airline
  - Billing Territory
- Created a **composite ProductKey** because product number was not unique.
- Separated **Country** and **Billing Territory** to avoid duplicate keys.
- Main relationship uses **BillingDate** (active). `ServiceDate` is kept as a second, inactive relationship.
- All relationships are **one‑to‑many** with **single‑direction filtering**.
- Created a dedicated **`_Measures` table** to keep DAX logic organised.

<img width="560" height="397" alt="image" src="https://github.com/user-attachments/assets/fe84498d-1359-4f21-98ba-aba321e7e11b" />


### 3. Key Findings
- **Total revenue: ~€9.44M** across **32,141 transaction lines** and **69 invoices**.
- **2014** was the strongest full year at **~€3.45M** – 2015 was **~5.3% lower**.
- **Latvia** is the largest market at **~€1.54M**.
- **Negative adjustments** total **~€101.7K** – kept in the model as part of financial activity.
- **Delayed billing** is low overall (**~0.5%**), but increased to **~1.0%** in 2015.
- Revenue is concentrated in a small number of products and channels – I added drill‑down filters to explore this further.


<img width="562" height="397" alt="image" src="https://github.com/user-attachments/assets/13af45fb-356b-4d02-b3eb-e8f6e1fb16e0" />

---

## 📁 Files in This Repository

| File | Description |
|------|-------------|
| `PowerBI_Submission_Barila.pbit` | Power BI template (no data – structure + measures) |
| `PowerBI_Submission_Barila.pdf` | PDF summary of assumptions, modelling, and findings |
| `README.md` | This description |

---

## 🧠 Technologies Used

- **Power BI Desktop** – data modelling, DAX, visualisation
- **Power Query** – data cleaning and transformation
- **DAX** – measures, time intelligence, business logic
- **Star schema** – dimensional modelling

---

## 🚀 How to Use

1. Download the `.pbit` file.
2. Open it in **Power BI Desktop**.
3. Connect to your own data source (the original CSV).
4. Refresh the model and explore the dashboard.

---

## 👤 About the Author

I'm **Januss Barila** – a Business & Data Analyst with 6+ years of experience across analytics, operations, and management. I turn fragmented data into clear reporting, useful tools, and practical improvements.

- **LinkedIn:** [linkedin.com/in/yanush-barila](https://linkedin.com/in/yanush-barila)
- **GitHub:** [github.com/JanussBarila](https://github.com/JanussBarila)
- **Portfolio:** [github.com/JanussBarila/Power-bi-portfolio](https://github.com/JanussBarila/Power-bi-portfolio)

---

## 📜 License

MIT – feel free to use and adapt.


P.S. Everyday template:

<img width="358" height="362" alt="image" src="https://github.com/user-attachments/assets/340ba7cf-d09f-4697-ade1-a88bda6c4387" />


