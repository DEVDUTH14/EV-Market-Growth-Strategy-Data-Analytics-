# ⚡ EV Adoption in Washington – Data-Driven Strategy for WSDOT

**Goal:** Help the Washington State Department of Transportation (WSDOT) design a data-driven strategy to boost **new EV adoption by 25% in two years**, by identifying the *true* causal drivers of adoption instead of relying on assumptions.

## 🚀 Impact

- Proved that Washington’s EV boom is **not primarily driven** by macroeconomic trends or broad affordability.
- Reframed WSDOT’s strategic focus from **vehicles (range, price)** to the **supporting ecosystem**, especially charging infrastructure.
- Identified **16 “High-Potential Follower” counties** where strong demand is being throttled by an infrastructure deficit, providing a precise geographic playbook for investment.
- Delivered a **“Twin Engines” framework** (Economic Potential + Infrastructure) and a suite of KPIs to guide ongoing policy and budget decisions.

## 🧪 Methodology

### Data Assets

- **EV Sales:** Transaction-level new EV registrations from WA Dept. of Licensing.
- **Charging Stations:** Public charging locations with open dates.
- **Demographics:** County-level population & median household income (yearly).
- **Macroeconomics:** Monthly statewide unemployment rate.

### Data Preparation

- Pivoted to a **high-fidelity transactional dataset** to ensure analytic integrity.
- Removed **~22,000 anomalous records** (leases, fleet sales, non-consumer noise) to focus on true consumer demand.
- Built a **hierarchical imputation pipeline** for missing sale prices and electric ranges, visually validating outputs to avoid biasing the market signal.

### Feature Engineering

Key KPIs engineered for strategic insight:

- `sales_per_1000_residents` and `stations_per_1000_residents` for normalized comparisons.
- **Sale price volatility** as a proxy for **market maturity**.
- **Affordability Index** = Median EV Price / Median Household Income.
- **BEV : PHEV sales ratio** to track consumer technology preferences.

### Analytics & Modeling

- **EDA:** Time-series charts, choropleth maps, scatter plots, box plots.
- **Correlation (Pearson):** Quantified relationships between adoption, income, infrastructure, affordability, unemployment, range, and EV load per station.
- **K-Means Clustering:** Segmented counties into data-driven groups (e.g., “Pacesetters,” “Followers,” “Laggards”) and surfaced **16 high-potential, under-served counties**.
- **Normalized time-series analysis:** Compared `sales_per_1000` vs `stations_per_1000` across clusters to visually and quantitatively show where **demand is outpacing infrastructure**.

## 🔍 Key Insights

- **The EV boom is unique:** Weak correlation with unemployment and affordability disproved the idea that the boom is just a reflection of a strong economy.
- **The range race is over:** Median BEV range has plateaued around **~300 miles**, turning range into **table stakes** rather than a barrier.
- **Subsidy design is outdated:** The state’s CAFV subsidy lost influence as eligibility declined, not because subsidies don’t work, but because **criteria lag the market**.
- **Infrastructure is the “smoking gun”:** In 16 high-potential counties, strong economic potential is held back by flat `stations_per_1000` curves, clearly identifying **charging infrastructure as the primary bottleneck**.

## 📈 Planned Extensions

- Forecast EV adoption for the next **2 years** at the county level.
- Model the adoption uplift from:
  - **+5% increase in stations/1000 residents**.
  - **+1% increase in median household income**.
