# Manufacturing Supply Chain Analytics – Power BI Dashboard


## Project Overview

Developed a comprehensive Manufacturing Supply Chain Analytics solution in Power BI to monitor production efficiency, supplier performance, logistics operations, transportation costs, and quality control across multiple manufacturing plants. The dashboard provides interactive operational insights to support faster and more informed business decisions.

---

## Business Objective

The objective of this project is to build an end-to-end manufacturing analytics platform that helps organizations track operational performance, optimize production processes, monitor supplier reliability, reduce logistics costs, and improve quality management using data-driven insights.

---

## Datasets Used

The project integrates multiple manufacturing and supply chain datasets:

* mfg_plants.sql
* mfg_materials.csv
* mfg_suppliers.sql
* mfg_purchase_orders.csv
* mfg_production.csv
* mfg_quality.csv
* mfg_warehouse_stock.sql
* mfg_transport_shipments.csv


---

## Data Modeling

Implemented a Star Schema data model for optimized reporting and analytics.

### Fact Tables

* Production
* Purchase Orders
* Quality
* Shipments

### Dimension Tables

* Plants
* Suppliers
* Materials
* Date

---

## Dashboard Pages

### 1. Operations Overview

Key operational monitoring dashboard containing:

* KPI Cards:

  * Total Production
  * Defect Percentage
  * Inventory Level
* Production Trend Analysis
* Production by Plant
* Material Consumption Analysis

#### Slicers

* Plant
* Material Category
* Year

---

### 2. Production Efficiency

Focused on analyzing plant productivity and operational efficiency.

#### Visuals

* Production vs Target
* Plant Performance Comparison
* Machine Utilization Metrics

#### Interactive Features

* Toggle Button:

  * Quantity View
  * Cost View

---

### 3. Supplier Performance

Supplier analytics dashboard for procurement monitoring and vendor evaluation.

#### Visuals

* Supplier Rating
* Cost per Supplier
* On-Time Delivery Percentage

#### Slicers

* Supplier
* Country

---

### 4. Quality Analytics

Quality control dashboard for monitoring defects and operational failures.

#### Visuals

* Defect Rate by Plant
* Quality Trend Analysis
* Failure Reason Breakdown

#### Insights

* Identify plants with the highest defect rates
* Analyze recurring quality issues and operational risks

---

### 5. Logistics & Distribution

Logistics monitoring dashboard for transportation and shipment analysis.

#### Visuals

* Shipment Cost Trend
* Destination Map
* Transport Cost Analysis

#### Interactive Features

* Toggle Button:

  * Shipment Volume
  * Shipment Cost

---

## Advanced DAX Calculations

### Production Yield

```DAX
Production Yield =
DIVIDE([Good Units], [Total Produced])
```

### Defect Percentage

```DAX
Defect Percentage =
AVERAGE(Quality[DefectRate])
```

### Material Cost

```DAX
Material Cost =
SUMX(
    PurchaseOrders,
    PurchaseOrders[Quantity] *
    RELATED(Materials[StandardCost])
)
```

### Inventory Turnover

```DAX
Inventory Turnover =
DIVIDE(
    [Material Consumption],
    AVERAGE(WarehouseStock[StockQty])
)
```

---

## Row Level Security (RLS)

### Role: Plant Manager

Implemented Row Level Security to ensure plant managers can only access their respective plant data.

```DAX
PlantID = USERPRINCIPALNAME()
```

---

## Report Design Features

* Orange theme operations dashboard
* KPI cards for quick operational monitoring
* Persistent plant slicers for easy filtering
* Bookmark navigation for better user experience
* Tooltip pages for detailed defect analysis

---

## Deliverables

* Power BI PBIX File
* Data Model Documentation
* KPI Metrics Documentation
* Supplier Performance Dashboard
* Production Analytics Dashboard

---

## Tools & Technologies

* Power BI
* SQL
* SSMS
* Power Query
* DAX
* Data Modeling
* Star Schema
* Row Level Security (RLS)

---

## Project Outcome

The dashboard enables manufacturing teams and operational managers to monitor production efficiency, evaluate supplier performance, optimize logistics operations, track inventory movement, and improve quality control through interactive visual analytics and KPI-driven reporting.

