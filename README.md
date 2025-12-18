# Macroeconomic panel dataset

used for a panel analysis at the [United Nations Global Economic Monitoring Brach](https://policy.desa.un.org/about-us/global-economic-monitoring-branch)

Collects various variables, e.g:

- **Macro**: GDP, output gap, ...
- **Fiscal**: Government debt, Primary balance, ...
- **Labor:** Productivity growth, annual hours worked, ...
- **Inequality**: Gini, Top 10% income share, ...
- **Trade**, **Poverty**, **Investment**, **Socioeconomic**, ...
- full list of variables available further below



We construct a country-specific commodity price influence index, inspired by [Deaton and Miller (1995)](https://econpapers.repec.org/paper/fthprinfi/79.htm) and [Collier and Goderis (2012)](https://www.sciencedirect.com/science/article/pii/S0014292112000505). For further information on the index take a look at the [explanation](./data/02_commodity/README.md).

## Meta

Commented repository structure

```
├── 12 Panel Project.Rproj     # R Project File
├── README.md 
├── data
│   ├── processed              # Processed Data
│   └── raw                    # Raw Data
│       └── BACI_HS92_V202501  # BACI Trade Data
├── docs
└── src
    ├── 01_data                # Data Processing Scripts
    └── 02_commodity           # Commodity Price Index Scripts
```

To reproduce the dataset, run the scripts in `src` in the numbered order. You will need to download some raw data files manually, as indicated in the respective scripts. 


## Variables

### Descriptive

| Code           | *Variable*        | *Unit* | *Source* | *Availability* |
| -------------- | ----------------- | ------ | -------- | -------------- |
| ISO            | ISO Alpha 3 code  | /      | UN       | x              |
| country        | Country Name      | /      | UN       | x              |
| status         | Developing Status | /      | UN       | x              |
| wesp_region    | WESP Region       | /      | DESA     | x              |
| wesp_subregion | WESP Subregion    | /      | DESA     | x              |
| country_code   | UN Country Code   | /      | UN       | x              |
| LDC            | LDC Status        | Binary | FAO      | x              |
| LLDC           | LLDC Status       | Binary | FAO      | x              |
| SIDS           | SIDS Status       | Binary | FAO      | x              |



### Macro

| Code           | *Variable*       | *Unit*             | *Source* | *Availability* |
| -------------- | ---------------- | ------------------ | -------- | -------------- |
|                | GDP              | US $, nominal      | WEFM     |                |
|                | GDP              | per capita         | WEFM     |                |
|                | GDP              | per capita, PPP    | WEFM     |                |
|                | GDP              | nominal growth     | WEFM     |                |
|                | GDP              | real growth        | WEFM     |                |
|                | Real Consumption |                    | WDI      |                |
| oda_gni        | Net ODA received | % of GNI           | WB       | x              |
| output_gap_pct | Output Gap       | % of Potential GDP | IMF      | x              |



### Monetary

| Code   | *Variable*                   | *Unit*          | *Source* | *Availability* |
| ------ | ---------------------------- | --------------- | -------- | -------------- |
| cbrate | Central Bank Policy Rate     | %               | GMD      | x              |
| infl   | Inflation                    | % (yoy)         | GMD      | x              |
| CPI    | CPI                          | Index, 2010=100 | GMD      | x              |
| REER   | Real effective exchange rate | Index, 2010=100 | GMD      | x              |
| USDfx  | USD exchange rate            | 1 USD in LC     | GMD      | x              |



### Fiscal

| *Variable*                      | *Unit*   | *Source*              | *Availability* |
| ------------------------------- | -------- | --------------------- | -------------- |
| Gov debt                        | % of GDP | GMD                   |                |
| Gov deficit                     | % of GDP | GMD                   |                |
| Gov expenditure                 | US$      |                       |                |
| Gov expenditure                 | % of GDP | GMD                   |                |
| Gov revenue                     | US$      |                       |                |
| Gov revenue                     | % of GDP | GMD                   |                |
| Gov Consumption                 | US$      | World Bank            |                |
| Primary net Lending / borrowing | % of GDP | Fiscal Monitor DB IMF |                |
| Net Lending / Borrwing          | % of GDP | Fiscal Monitor DB IMF |                |



### Fiscal: Debt

| *Code*                     | *Variable*           | *Unit*   | *Source*              | *Availability* |
| -------------------------- | -------------------- | -------- | --------------------- | -------------- |
| interest_payments_gdp      | Interest Expense     | % of GDP | World Bank WDI        | x              |
| primary_fiscal_balance_gdp | Primary Balance      | % of GDP | Fiscal Monitor DB IMF | x              |
| fiscal_balance_gdp         | Gross Fiscal Balance | % of GDP | WDI                   | x              |
| net_debt_gdp               | Net Debt             | % of GDP | Fiscal Monitor DB IMF | x              |



### Labor

| *Code*                           | *Variable*                   | *Unit*                | *Source*  | *Availability* |
| -------------------------------- | ---------------------------- | --------------------- | --------- | -------------- |
| unemp                            | Unemployment Rate            | % of population       | (via GMD) | x              |
| labor_productivity_person_growth | Growth of Labor Productivity | per employed          | TCB       | x              |
| labor_productivity_hour_growth   | Growth of Labor productivity | per hour worked       | TCB       | x              |
| total_hours_worked               | Total Hours worked           | Annual hours          | TCB       | x              |
| working_age_pop_pct              | Population ages 15-64        | % of total population | WDI       | x              |



### Inequality

| *Code* | *Variable*              | *Unit*            | *Source*                  | *Availability* |
| ------ | ----------------------- | ----------------- | ------------------------- | -------------- |
|        | Gini                    | 0-1               | World Inequality Database | x              |
|        | Top 10% Income Share    | % of total income | World Inequality Database | x              |
|        | Bottom 50% Income Share | % of total income | World Inequality Database | x              |
|        | T10/B50 Ratio           |                   | Calc                      | x              |



### Trade

| *Code*      | *Variable*                    | *Unit*      | *Source* | *Availability* |
| ----------- | ----------------------------- | ----------- | -------- | -------------- |
| exports_usd | Exports of Goods and Services | current US$ | WDI      | x              |
| exports_gdp | Exports of Goods and Services | % of GDP    | WDI      | x              |
| imports_usd | Imports of Goods and Services | current US$ | WDI      | x              |
| imports_gdp | Imports of Goods and Services | % of GDP    | WDI      | x              |
|             | Trade openness                | % of GDP    | Calc     |                |



### Poverty

| *Code*            | *Variable*                                     | *Unit*          | *Source* | *Availability* |
| ----------------- | ---------------------------------------------- | --------------- | -------- | -------------- |
| pov_international | Population living below 2.15$ Poverty Line     | % of population | WB       | x              |
| pov_national      | Population living below national poverty lines | % of population | WB       | x              |
| un_multidim_pov   | Multidimensional Poverty Threshold (UNDP)      | % population    | UNDP     | x              |
| Wb_multidim_pov   | Multidimensional Poverty (WB)                  | % of pop        | WB       | x              |



### Investment

| *Code*                    | *Variable*                                        | *Unit*             | *Source* | *Availability* |
| ------------------------- | ------------------------------------------------- | ------------------ | -------- | -------------- |
| fdi_in_gdp                | FDI Inflows                                       | % of GDP           | WDI      | x              |
| gross_CF_gdp              | gross capital formation                           | % of GDP           | WDI      | x              |
| private_investment_gdp    | Gross fixed capital formation, private Sector     | % of GDP           | ICSD IMF | x              |
| government_investment_gdp | Gross fixed capital formation, general government | % of GDP           | ICSD IMF | x              |
| rnd_gdp                   | R&D expenditure                                   | % of GDP           | WDI WB   | x              |
| reseearchers_per_million  | Reseeachers in R&D                                | per million people | WDI      | x              |



### Prices

| *Code*           | *Variable*       | *Unit*   | *Source*                     | *Availability* |
| ---------------- | ---------------- | -------- | ---------------------------- | -------------- |
| oil_price_index  | Oil price Index  | 2016=100 | Primary Commodity Prices IMF | x              |
| food_price_index | Food Price Index | 2016=100 | Primary Commodity Prices IMF | x              |



### Socioeconomic

| *Code*                    | *Variable*                    | *Unit*                  | *Source* | *Availability* |
| ------------------------- | ----------------------------- | ----------------------- | -------- | -------------- |
| life_expectancy           | Life expectancy at birth      | years                   | WDI WB   | x              |
| school_enrollment_primary | School enrollment, primary    | % of relevant age group | WDI WB   | x              |
| remittances_gdp           | Personal Remittances received | $ US Dollar             | WB       | x              |



### Misc

| *Code*     | *Variable*                  | *Unit*                                       | *Source*                                                     | *Availability* |
| ---------- | --------------------------- | -------------------------------------------- | ------------------------------------------------------------ | -------------- |
| FHI_pr     | Political Rights Index      | 1-7                                          | Freedom House                                                | x              |
| FHI_cl     | civil liberties index       | 1-7                                          | Freedom House                                                | x              |
| FHI_status | Freedom Status              | Free (F), Partially Free (PF), Not free (NF) | Freedom House                                                | x              |
| eci        | Economic Complexity Index   | Ca [-3,3]                                    | OEC                                                          | x              |
| cpi        | Corruption Perception Index | 0 - 100                                      | Transparency International                                   | x              |
| hdi        | Human Development Index     | 0 - 1                                        | UNDP                                                         | x              |
| cgi        | Commodity Price index       |                                              | DIY, inspired by [Collier & Goderis](https://www.sciencedirect.com/science/article/pii/S0014292112000505) |                |

