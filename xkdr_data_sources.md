# Data Sources Referenced by XKDR Forum (xkdr.org)

Extracted from 59 research papers, blog articles (The Leap Journal), discourse items, and the XKDR systems page. Sources are deduplicated and organized by category.

---

## 1. CMIE (Centre for Monitoring Indian Economy) Databases

### CMIE Prowess
- **Link:** Commercial subscription (https://www.cmie.com/)
- **What:** Comprehensive corporate database for Indian firms -- balance sheets, income statements, financial ratios, entity types, industry sector, ownership, listing status.
- **Use cases:** Financial distress prediction models, distance-to-default analysis, firm-level research. Used in papers on Altman bankruptcy models, rating downgrades, and insolvency reforms.

### CMIE Consumer Pyramids Household Survey (CPHS)
- **Link:** Commercial subscription (https://www.cmie.com/)
- **What:** Panel dataset surveying ~200,000 Indian households three times per year since 2014, capturing income, consumption, and financial data at monthly frequency.
- **Use cases:** Household savings behavior (Average Propensity to Consume), electricity expenditure patterns across cities, financial inclusion measurement, income-consumption dynamics.

### CMIE States of India
- **Link:** Commercial subscription (https://www.cmie.com/)
- **What:** Macro-economic indicators for 37 states/UTs and 724 districts -- fiscal data (debt, GSDP, interest payments, revenue receipts).
- **Use cases:** Debt sustainability analysis for states, cross-state fiscal comparisons, Tamil Nadu public finance analysis.

### CMIE Economic Outlook
- **Link:** Commercial subscription (https://www.cmie.com/)
- **What:** Macroeconomic database covering trade, GDP, and other indicators for India.
- **Use cases:** Trade data analysis (e.g., Indian imports from Russia), macroeconomic trend analysis.

---

## 2. Satellite and Remote Sensing Data

### VIIRS Nighttime Lights (Earth Observation Group)
- **Link:** https://eogdata.mines.edu/products/vnl/
- **What:** Monthly satellite imagery of nighttime light radiance from the VIIRS instrument aboard Suomi-NPP/NOAA-20 satellites. Available from April 2012 at 15-arc-second resolution (~500m). Measures radiance in nW/cm2/sr.
- **Use cases:** Proxy for economic activity, property tax buoyancy analysis, economic impact of the Russia-Ukraine war, cloud bias correction in satellite data. Multiple XKDR papers and the NighttimeLights.jl package are built around this data.

### DMSP-OLS Nighttime Lights
- **Link:** Available via NOAA Earth Observation Group
- **What:** Annual satellite imagery of nighttime lights from the Defense Meteorological Satellite Program (1992-2013, now discontinued). 30-arc-second resolution.
- **Use cases:** Historical economic activity analysis. Predecessor to VIIRS; referenced in foundational nighttime lights papers.

### NASA POWER Data (Solar Irradiance)
- **Link:** https://power.larc.nasa.gov/data-access-viewer/
- **What:** Satellite-derived solar irradiance data (All Sky Surface Shortwave Downward Irradiance) by location and time.
- **Use cases:** Solar panel capacity estimation and energy generation analysis for agricultural solarisation in Tamil Nadu.

### NRSC Evapotranspiration Data (via data.gov.in)
- **Link:** https://data.gov.in
- **What:** National Remote Sensing Centre evapotranspiration values based on satellite and ground observations.
- **Use cases:** Estimating crop irrigation requirements for agricultural solarisation analysis.

---

## 3. Judicial and Legal Data

### XKDR Legal System Dataset (Case Life-Cycle Data)
- **Link:** https://xkdr.github.io/legal-system-dataset-frontend/
- **What:** Life-cycle data for 5,653 commercial cases (Bombay HC) and 7,346 IBC cases (NCLT Mumbai), covering Jan 2022-Dec 2024. Includes filing dates, hearing dates, connected matters, time to disposal.
- **Use cases:** Court performance evaluation, litigation duration analysis, court reform baseline measurement. Open dataset with downloadable ZIP files and Jupyter notebooks.

### e-Courts Database
- **Link:** https://services.ecourts.gov.in/ecourtindia_v6/
- **What:** Public database of court records across Indian district courts -- case filing details, hearing dates, disposal status, order copies.
- **Use cases:** Random sampling of disposed cases for court reform baselines, litigant-perspective evaluation of courts, MACT litigation analysis. XKDR hand-collected 200+ cases from 7 states.

### National Judicial Data Grid (NJDG)
- **Link:** https://njdg.ecourts.gov.in/
- **What:** Aggregated judicial statistics showing pending case status across Indian courts, published by Department of Justice.
- **Use cases:** Validating hand-collected case samples, understanding pre-trial bottlenecks (72% of pending cases stuck before trial), counting cases methodology critique.

### Bombay High Court Case Records
- **Link:** Bombay High Court public website
- **What:** Life-cycle data of 236,953 cases filed at the Original Side (Jan 2017-Dec 2024), with 142 case-type classifications and CNR numbers.
- **Use cases:** Demonstrating methodological problems with standard case-counting (NJDG inflates counts by treating sub-cases as distinct filings).

### FRG Insolvency Cases Dataset (NCLT/NCLAT)
- **Link:** http://ifrogs.org/dms/IBC/nclt_data.html
- **What:** Hand-collected dataset of firms in bankruptcy under IBC, based on NCLT/NCLAT orders. Contains 6,678 cases (as of June 2018) with case ID, bench, filing/disposal dates, admission status.
- **Use cases:** Identifying defaulted firms for financial distress prediction models.

### Development Data Lab (DDL) Judicial Data Portal
- **Link:** https://www.devdatalab.org/judicial-data
- **What:** Public judicial dataset of cases from India's subordinate courts, scraped from e-courts portal. Over 43 million case records (2010-2020).
- **Use cases:** Identifying most commonly invoked civil and criminal laws, court workload analysis.

### 24x7 ONCourts Public Dashboard (Kerala)
- **Link:** https://oncourts.kerala.gov.in/dashboard
- **What:** Real-time case statistics dashboard for the Kerala court reform pilot in Kollam.
- **Use cases:** Monitoring court performance post-intervention.

---

## 4. Government Fiscal and Economic Data

### CityFinance Portal (MoHUA)
- **Link:** https://www.cityfinance.in/home
- **What:** Self-reported municipal finance data at the Urban Local Body (ULB) level, maintained by Ministry of Housing and Urban Affairs. Covers property tax demand/collection, exemptions, and other fiscal variables.
- **Use cases:** Constructing balanced panels of 2,470 ULBs across 23 states for property tax buoyancy analysis.

### GSDP / National Accounts (MoSPI)
- **Link:** https://mospi.gov.in
- **What:** State-level GDP (GSDP) in nominal and real terms, national GDP, GVA by sector.
- **Use cases:** Primary explanatory variable for property tax buoyancy regressions, fiscal analysis baseline.

### RBI State Finances: A Study of Budgets
- **Link:** Published annually by RBI
- **What:** Annual publication on the fiscal position of state governments -- debt, revenue, expenditure.
- **Use cases:** State-level debt sustainability analysis, fiscal comparisons.

### RBI Report on Municipal Finances
- **Link:** Published periodically by RBI
- **What:** Finances of municipal corporations -- revenue composition, expenditure, intergovernmental transfers. Covers 232 municipal corporations.
- **Use cases:** Tracking property tax as share of municipal own-tax revenue (53-63%).

### Karnataka State Fiscal Documents
- **Link:** Public domain PDFs from Government of Karnataka
- **What:** 7-volume annual fiscal disclosure (2020-21, ~1,000+ pages) with hierarchical tabular fiscal data (Major Head > Sub-Major Head > Minor Head > Sub Head > Detailed Head > Object Head).
- **Use cases:** Developing LLM-based information extraction pipelines for fiscal data.

### India Open Government Data Portal
- **Link:** https://data.gov.in
- **What:** India's National Data Sharing and Accessibility Policy (NDSAP) portal publishing government datasets across domains.
- **Use cases:** Evapotranspiration data, various government datasets for research.

### CAG State Accounts Reports
- **Link:** https://cag.gov.in/
- **What:** Comptroller and Auditor General audit reports for states, covering guarantees and off-budget borrowings.
- **Use cases:** Documenting electricity sector debt guarantees in Tamil Nadu (70-90% of outstanding guarantees).

### DEA Status Paper on Government Debt
- **Link:** https://dea.gov.in/
- **What:** Official status paper on government debt at national level.
- **Use cases:** National debt-to-GDP ratio comparisons.

---

## 5. Power Sector Data

### PFC Report on Performance of Power Utilities
- **Link:** https://www.pfcindia.com/
- **What:** Annual performance metrics of state power utilities -- units sold, average cost of supply, revenue, AT&C losses.
- **Use cases:** Consumer category-wise tariffs, cross-state discom comparison, TANGEDCO performance ranking (49/51).

### TANGEDCO / TANTRANSCO Annual Reports
- **What:** Financial statements of Tamil Nadu's electricity generation, distribution, and transmission corporations.
- **Use cases:** Borrowing profiles, decadal trend of losses, liability analysis for electricity reform research.

### TNERC Tariff Orders
- **Link:** http://www.tnerc.gov.in/
- **What:** Tamil Nadu Electricity Regulatory Commission orders setting electricity rates, benchmark costs for solar panels.
- **Use cases:** Tariff data for consumer categories, agriculture electricity pricing, solar panel cost benchmarks.

### PRAAPTI Portal
- **Link:** https://praapti.in
- **What:** Government portal tracking payment delays by discoms to power generators.
- **Use cases:** Monitoring TANGEDCO payment improvement (12 months to 2 months delay).

### IEX (Indian Energy Exchange) Market Snapshot
- **Link:** https://www.iexindia.com/marketdata/market_snapshot.aspx
- **What:** Real-time and historical electricity market prices from India's power exchange.
- **Use cases:** Documenting power shortages and market prices for solar surplus sales analysis.

### CEA All India Electricity Statistics
- **Link:** https://cea.nic.in/
- **What:** Comprehensive national statistics on electricity generation, installed capacity, energy sources.
- **Use cases:** Non-fossil fuel share of installed capacity (35.8%), national energy context.

---

## 6. Agricultural and Land Data

### Agriculture Census 2015-16
- **Link:** https://agcensus.dacnet.nic.in/
- **What:** National census of agricultural landholdings -- district-wise data on number and size of operational holdings.
- **Use cases:** Distribution of landholding in Erode district for solarisation analysis.

### Minor Irrigation Census 2017-19
- **Link:** https://micensus.gov.in/
- **What:** Census of minor irrigation sources (wells, tubewells) across India.
- **Use cases:** Identifying primary irrigation sources and average well depths for solar pump sizing.

### FAO Irrigation and Drainage Paper 56
- **Link:** https://www.fao.org/3/X0490E/x0490e0a.htm
- **What:** FAO methodology for calculating crop water needs, including reference crop evapotranspiration and crop coefficients.
- **Use cases:** Estimating irrigation requirements for paddy, groundnut, and maize in Tamil Nadu.

### MNRE Solar Irrigation Pump Sizing Guidelines
- **Link:** https://mnretestui2.hkapl.in/#/sip-sizing-tools
- **What:** MNRE specifications for appropriate irrigation pump and solar panel capacity based on solar insolation and water requirements.
- **Use cases:** Selecting solar pump models and panel capacity for agricultural solarisation.

---

## 7. Health and Drug Procurement Data

### CDSCO Drug Quality Reports
- **Link:** https://cdsco.gov.in/
- **What:** Drug quality testing results, classification of drugs as Not of Standard Quality (NSQ) or spurious.
- **Use cases:** Pre-qualification for drug procurement, quality assurance in government drug purchases.

### XLN (Xtended Licensing, Laboratory & Legal Node)
- **Link:** https://xlnindia.gov.in/
- **What:** Central database for drug manufacture licensing and quality assurance. Only partly functional with ~4 states contributing.
- **Use cases:** Studying substandard drug quality reporting and consolidation gaps.

### National Drug Survey 2014-16
- **Link:** https://main.mohfw.gov.in/documents/reports/drugs-survey-report
- **What:** Survey on spurious and NSQ drugs. Key finding: 10% NSQ rate for government-procured drugs vs 3% in retail.
- **Use cases:** Motivating procurement process improvement research.

---

## 8. Financial Markets and Corporate Data

### NSE/BSE Market Data
- **What:** Stock exchange data for listed Indian companies.
- **Use cases:** Distance-to-default calculations, market surveillance analysis.

### SIPRI Arms Transfers Database
- **Link:** https://www.sipri.org/databases/armstransfers
- **What:** International transfers of major conventional arms since 1950, covering suppliers and recipients.
- **Use cases:** Tracking Indian arms imports (documenting declining Russian share) for FIMI analysis.

---

## 9. Insurance and Motor Vehicle Data

### General Insurance Council (GIC) Yearbook
- **Link:** https://www.gicouncil.in/
- **What:** Industry-level insurance statistics including incurred claims ratios for motor insurance.
- **Use cases:** MACT litigation analysis (78% incurred claims ratio for motor insurance).

### Insurance Information Bureau (IIB) Motor Annual Report
- **Link:** https://admin.iib.gov.in/
- **What:** Detailed motor insurance claims data including settlement amounts and patterns.
- **Use cases:** Showing 93% of own-damage claims settle under INR 50,000 while TP payouts run much higher.

---

## 10. Media and Information Data

### Reporters Without Borders - Media Ownership Monitor: India
- **Link:** https://rsf.org/en/media-ownership-monitor-who-owns-media-india
- **What:** 2019 study mapping media ownership in India -- audience shares, ownership structures, concentration levels across print, TV, and online.
- **Use cases:** Media concentration analysis (4 Hindi outlets capture 76.45% of Hindi readership).

### Data Leads - Media Ownership Monitor: India
- **Link:** http://india.mom-gmr.org/en/
- **What:** Corporate ownership patterns, cross-ownership, and media market structure data for India.
- **Use cases:** Evidence on media concentration causes and cross-media regulation gaps.

---

## 11. International and Geopolitical Data

### Freedom House Reports
- **Link:** https://freedomhouse.org/
- **What:** Annual reports on internet freedom, media influence, and authoritarian expansion across countries.
- **Use cases:** India's internet freedom ranking, Chinese/Russian media influence operations documentation.

### EEAS FIMI Threat Report
- **Link:** https://www.eeas.europa.eu/
- **What:** EU's report on Foreign Information Manipulation and Interference threats.
- **Use cases:** Defining FIMI framework and offensive operations taxonomy.

### Meta Coordinated Inauthentic Behaviour Reports
- **Link:** https://about.fb.com/
- **What:** Monthly reports on coordinated inauthentic behaviour operations on Facebook/Instagram.
- **Use cases:** Documenting Russian vaccine disinformation campaigns targeting India.

---

## 12. XKDR Open-Source Software Tools

### NighttimeLights.jl
- **Link:** https://github.com/xKDR/NighttimeLights.jl
- **What:** Julia package for cleaning and processing VIIRS monthly nighttime lights data.

### Survey.jl
- **Link:** Julia package for complex survey data analysis (stratification, clustering, weights).

### DtD.jl
- **What:** Julia package for Distance-to-Default calculations.

### CRRao.jl
- **What:** Julia package for statistical modeling.

### TSx.jl
- **What:** Julia package for time series analysis.

### eventstudies (R)
- **What:** R package for event study analysis.

### fxregime (R)
- **What:** R package for FX regime analysis.

### Aqui (Air Quality Monitor)
- **Link:** https://github.com/ayushpatnaikgit/aqui
- **What:** Open-source DIY air quality monitor (SDS011 + ESP32) for citizen-led PM2.5 data collection.

---

## 13. Other Government/Regulatory Data

### GeM (Government e-Marketplace)
- **What:** Central government procurement platform data.
- **Use cases:** Analysis of union government procurement footprint.

### IRDAI Motor Insurance Data
- **Link:** https://irdai.gov.in/
- **What:** Regulatory documents on motor insurance -- tariff orders, obligations, handbook.
- **Use cases:** MACT litigation analysis, insurance market regulation.

### State Procurement Agency Documents (Gujarat, Bihar, Punjab, Rajasthan)
- **What:** Procurement manuals, tender documents, blacklisting policies from state drug procurement agencies (GMSCL, RMSCL, BMSIC, PHSC).
- **Use cases:** Comparative analysis of 13 design elements across 4 states' procurement processes.

### OECD Local Tax Distribution Data
- **What:** Cross-country data on distribution of local taxes (income, property, goods) across 37 OECD countries.
- **Use cases:** International comparison of property tax role in local government finance.

---

## 14. Additional Data Sources (from later-completing agents)

### GHSL Building Volume Data (European Commission JRC)
- **Link:** https://ghsl.jrc.ec.europa.eu/
- **What:** Global built-up volume grids derived from Sentinel-2, Landsat, and global DEM data. Provides building volume in cubic meters at ~90m resolution, multitemporal (1975-2030).
- **Use cases:** Property tax potential estimation -- Sum of Building Volume (SoBV) alone explains >80% of variation in property tax demand across ULBs in Karnataka.

### Mahabhulekh Portal (Maharashtra Land Records)
- **Link:** https://mahabhulekh.maharashtra.gov.in
- **What:** Digitised 7/12 extract textual land records for rural Maharashtra -- parcel-level ownership, area, land type, usage, crops.
- **Use cases:** De jure mapping of women's land ownership. XKDR extracted ~37 lakh records across 3 districts using browser automation.

### NCAER Land Records and Services Index (N-LRSI)
- **Link:** NCAER (https://www.ncaer.org/)
- **What:** Index measuring land record digitisation progress across 33 Indian states -- textual records, cadastral maps, registration computerisation.
- **Use cases:** Studying whether land record quality affects household credit access. States with better LRSI have higher formal borrowing.

### MCA-21 Database (Ministry of Corporate Affairs)
- **Link:** https://www.mca.gov.in/
- **What:** Electronic filing system for all registered companies in India (~1.1 million firms). Contains financial statements, corporate filings.
- **Use cases:** MSME analysis, comparing financing patterns of small vs large firms.

### NSE Tick-by-Tick Trading Data (TAO)
- **Link:** Proprietary (National Stock Exchange of India)
- **What:** Microsecond-level orders and trades data from NSE equity and derivatives segments -- prices, quantities, order types, algorithmic trading flags.
- **Use cases:** Market microstructure research, Order-to-Trade Ratio fee effectiveness analysis, market surveillance.

### FIMMDA Government Securities Yield Data
- **Link:** http://www.fimmda.org
- **What:** Government of India treasury bill prices and yields.
- **Use cases:** Risk-free rate calculations for Distance-to-Default models.

### RBI Handbook of Statistics on Indian Economy
- **Link:** https://dbie.rbi.org.in/
- **What:** Multiple tables: Table 113 (ownership of government securities), Table 109 (interest rates), Table 116 (maturity patterns), Table 44 (CRR/SLR rates).
- **Use cases:** Analysis of who lends to the Indian state -- mandatory vs voluntary investment in government bonds by banks, insurance, pension funds.

### EPFO, PFRDA, IRDAI Annual Reports
- **What:** Investment data for Employees' Provident Fund, National Pension System, and insurance firms showing portfolio allocation across asset classes.
- **Use cases:** Tracking mandatory government bond purchases by institutional investors, estimating coercive vs voluntary lending to the Indian state (~95% coercive).

### Detailed Demands for Grants (DDGs) / CGA Accounts
- **Link:** Individual ministry websites / https://cga.nic.in/
- **What:** Object-head-wise expenditure data from 33 Union government civil ministries. DDGs contain budgeted vs actual procurement spending.
- **Use cases:** Estimating Union government procurement footprint (11-12% of GDP), analyzing "spending gaps" between budgeted and actual procurement.

### Novel Downloadable Datasets (XKDR-produced)
- **Financial Inclusion Measurement Survey:** https://dvararesearch.com/wp-content/uploads/2024/05/Financial-Inclusion-Measurement_Dataset.csv -- 300 household survey on financial inclusion (inputs, outputs, outcomes).
- **Union Ministry Procurement Dataset:** https://papers.xkdr.org/WP22-092023/unionministryprocurement.csv -- Ministry-level procurement data for 33 ministries (2014-2021).
- **Legal System Dataset:** https://xkdr.github.io/legal-system-dataset-frontend/ -- Case lifecycle data for commercial and IBC cases.

### Crime Victimisation Survey Data (India)
- **What:** Several CVS efforts referenced: CHRI/Vishwas Setu (2015, Mumbai/Delhi), IDFC/SATARC (2017, 4 cities), Karnataka CVS (2018-19, statewide), Status of Policing in India Reports.
- **Use cases:** Measuring actual crime vs reported crime, non-reporting patterns, police response quality.

### Google Earth Engine
- **Link:** https://earthengine.google.com/
- **What:** Cloud geospatial analysis platform for accessing satellite imagery at scale (VIIRS, DMSP-OLS, FAO GAUL boundaries).
- **Use cases:** Processing nighttime lights data for economic activity analysis at national/regional scale.

### Global Data Lab -- Subnational Human Development Database
- **Link:** https://globaldatalab.org
- **What:** Socioeconomic indicators at subnational level across countries, including GNI per capita in PPP terms.
- **Use cases:** Ground-truth validation for nighttime lights as GDP proxy at Indian state level.

### Harmonized Global Nighttime Light Dataset (Li et al.)
- **Link:** https://doi.org/10.6084/m9.figshare.9828827.v7
- **What:** Annual harmonized DMSP-OLS + VIIRS nighttime lights (1992-2021) in consistent time series.
- **Use cases:** Long-run economic activity analysis bridging the DMSP and VIIRS satellite eras.

---

*Report compiled from analysis of all 59 research papers, 15+ blog articles, 6 op-ed series, discourse items, and systems pages on xkdr.org. 44 sub-agents processed all content. Some papers (particularly policy commentary and legal analysis papers) contained no original data sources.*
