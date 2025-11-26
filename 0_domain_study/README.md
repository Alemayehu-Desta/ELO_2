# Domain Study: Foreign Direct Investment (FDI)

## Background

Foreign Direct Investment (FDI) plays a transformative role in the economic development of low- and middle-income countries. It brings capital, technology transfer, managerial expertise, and integration into global value chains—resources that many developing economies cannot generate domestically at sufficient scale. Over the last two decades, governments across Africa, Asia, Latin America, and Eastern Europe have increasingly positioned FDI as a central pillar of their development and industrialization strategies.

Global FDI flows have become more volatile. Competition for investment has intensified, governance quality has gained new importance, infrastructure gaps remain persistent, and human capital shortages continue to constrain industrial growth. At the same time, emerging sectors such as ICT, clean energy, and advanced manufacturing demand capabilities that not all countries possess. These dynamics have widened disparities between countries that attract sustained FDI and those that struggle.

Understanding why certain countries succeed while others lag is therefore crucial. This domain study provides the conceptual and empirical foundation needed to analyze the determinants of FDI and construct a rigorous, transparent FDI Attractiveness & Risk Score (FARS) for developing and middle-income economies.

---

## Problem Statement

Middle-income and developing countries face a critical question:

**What mix of economic conditions, governance quality, infrastructure readiness, and human-capital capacity enables them to attract consistent, high-quality foreign investment?**

Despite a large body of research, there remains no unified, open-source, data-driven framework that brings these factors together into a coherent, comparable scoring system.

Existing analyses are often fragmented—some focus on institutions, others on infrastructure, others on macroeconomic fundamentals. Investors and policymakers must piece together insights manually, making it difficult to benchmark countries or understand which reforms would yield the greatest improvement in competitiveness.

This project addresses this gap using data science tools by synthesizing academic literature, institutional reports, and empirical evidence to identify the most influential drivers of FDI and translate them into a composite index tailored to developing economies.

---

## Research Questions

### **Main Research Question**

**What combination of economic, governance, infrastructure, and human-capital factors best explain why some middle-income and developing countries attract more foreign direct investment than others?**

### **Supporting Questions**

* Which countries currently rank highest in FDI attractiveness, and what distinguishes them?
* What structural factors contribute most strongly to variations in FDI inflows across countries and sectors?
* How would improvements in infrastructure, governance, or human capital alter a country’s investment outlook?
* Are the determinants of FDI different across sectors such as manufacturing, ICT, and renewable energy?

---

## Geographic Scope

This analysis focuses on **Low-Income (LIC)**, **Lower-Middle-Income (LMIC)**, and **Upper-Middle-Income (UMIC)** economies according to the **World Bank 2023 income classification**. These economies rely heavily on FDI as an engine for industrialization, employment creation, and integration into global markets.

**High-Income Countries (HICs)** are excluded from model estimation to avoid structural distortions. High-income economies possess deep capital markets, stable institutions, and advanced infrastructure that fundamentally change the nature of FDI inflows. Including them would obscure the dynamics most relevant for developing countries.

A small group of **benchmark high-income economies** (e.g., Singapore, Ireland, Netherlands) may be included for comparison in dashboards but **not** in the core modeling.

---

## Time Scope

The study covers **2010–2023**, a period that includes:

* A decade of pre-pandemic globalization and structural transformation (2010–2019)
* The COVID-19 shock and the subsequent disruption of global investment flows (2020–2023)

To improve stability and reduce noise in the data, **multi-year averages** (e.g., 3-year windows) are used when appropriate.

---

## Literature Review

Research on FDI determinants highlights a consistent set of drivers across decades and regions:

### **Economic Fundamentals**

Market size (GDP), growth prospects, and trade openness are among the most reliable predictors of FDI. Countries with expanding domestic markets and strong export potential consistently attract higher inflows.

### **Governance and Institutional Quality**

Rule of law, regulatory quality, political stability, and control of corruption play a central role. Investors avoid jurisdictions where contracts are difficult to enforce or where policy unpredictability increases risk.

### **Infrastructure and Logistics**

Electricity reliability, transportation efficiency, and digital connectivity significantly influence the feasibility of operations. Infrastructure gaps are frequently cited as binding constraints for FDI in Africa, South Asia, and parts of Latin America.

### **Human Capital and Labor Costs**

Education levels, workforce skills, and competitive labor costs shape sector-specific competitiveness—particularly in manufacturing, ICT, and services.

### **Policy Environment and Openness**

Investment incentives, trade integration, streamlined regulations, and predictable tax regimes increase a country’s attractiveness.

Across studies, one insight is clear: **no single factor explains FDI inflows on its own**. Rather, investment decisions reflect a combination of complementary strengths.

---

## How Domain Knowledge Informs the Project

This domain research forms the foundation for:

* Designing the pillars and indicators of the **FDI Attractiveness & Risk Score (FARS)**
* Selecting appropriate datasets (WDI, UNCTAD, WGI, ILO, LPI, IEA, etc.)
* Structuring the data pipeline and model validation steps
* Building a dashboard that communicates insights clearly and effectively

Without this grounding, the index would lack interpretability and relevance for the policymaking and investment communities.

---

## Resources and References

A curated list of academic papers, institutional reports, and data sources is included below. These links provide an empirical and theoretical basis for understanding global FDI dynamics.

### **Institutional Data Sources**

* **UNCTAD World Investment Reports** — [https://unctad.org/publications/world-investment-report](https://unctad.org/publications/world-investment-report)
* **UNCTADstat (FDI flows & stocks)** — [https://unctadstat.unctad.org](https://unctadstat.unctad.org)
* **World Bank World Development Indicators (WDI)** — [https://data.worldbank.org](https://data.worldbank.org)
* **Worldwide Governance Indicators (WGI)** — [https://info.worldbank.org/governance/wgi/](https://info.worldbank.org/governance/wgi/)
* **IMF Data (BOP, macro indicators)** — [https://www.imf.org/en/Data](https://www.imf.org/en/Data)
* **Transparency International CPI** — [https://www.transparency.org/en/cpi](https://www.transparency.org/en/cpi)
* **ILO & ILOSTAT** — [https://ilostat.ilo.org](https://ilostat.ilo.org)
* **Logistics Performance Index (LPI)** — [https://lpi.worldbank.org/](https://lpi.worldbank.org/)
* **IEA Energy Data** — [https://www.iea.org/data-and-statistics](https://www.iea.org/data-and-statistics)
* **IRENA Renewable Energy Data** — [https://www.irena.org/Data](https://www.irena.org/Data)

### **Academic & Policy References**

* Dunning, J. H. *The Eclectic Paradigm of International Production.*
* Alfaro, L., et al. *FDI and Economic Growth.*
* OECD. *FDI in Figures.*
* World Bank. *Global Investment Competitiveness Report.*
* UNCTAD. *World Investment Report* (annual editions).

---

This domain study provides the conceptual grounding for the next stages of the project, including dataset selection, indicator engineering, and model development. A strong understanding of the FDI landscape ensures that the final index is valid, interpretable, and genuinely useful for policymakers and investors.
