# GEMB Panel

Collecting various data sources for a macro research project





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

| Code           | *Variable*          | *Unit*             | *Source* | *Availability* |
| -------------- | ------------------- | ------------------ | -------- | -------------- |
|                | GDP                 |                    | WEFM     |                |
|                | GDP per capita      |                    | WEFM     |                |
|                | GDP per capita, PPP |                    | WEFM     |                |
|                | GDP, nominal growth |                    | WEFM     |                |
|                | GDP, real growth    |                    | WEFM     |                |
|                | Real Consumption    |                    | WEFM     |                |
| oda_gni        | Net ODA received    | % of GNI           | WB       | x              |
| output_gap_pct | Output Gap          | % of Potential GDP | IMF      | x              |



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
| Gov debt                        | % of GDP |                       |                |
| Gov deficit                     | % of GDP |                       |                |
| Gov expenditure                 | US$      |                       |                |
| Gov expenditure                 | % of GDP |                       |                |
| Gov revenue                     | US$      |                       |                |
| Gov revenue                     | % of GDP |                       |                |
| Gov Consumption                 | US$      | World Bank            |                |
| Primary net Lending / borrowing | % of GDP | Fiscal Monitor DB IMF |                |
| Net Lending / Borrwing          | % of GDP | Fiscal Monitor DB IMF |                |



### Fiscal: Debt

|                            | *Variable*           | *Unit*   | *Source*              | *Availability* |
| -------------------------- | -------------------- | -------- | --------------------- | -------------- |
| interest_payments_gdp      | Interest Expense     | % of GDP | World Bank WDI        | x              |
| primary_fiscal_balance_gdp | Primary Balance      | % of GDP | Fiscal Monitor DB IMF | x              |
| fiscal_balance_gdp         | Gross Fiscal Balance | % of GDP | WDI                   | x              |
| net_debt_gdp               | Net Debt             | % of GDP | Fiscal Monitor DB IMF | x              |



### Labor

|                                  | *Variable*                   | *Unit*                | *Source*  | *Availability* |
| -------------------------------- | ---------------------------- | --------------------- | --------- | -------------- |
| unemp                            | Unemployment Rate            | % of population       | (via GMD) | x              |
| labor_productivity_person_growth | Growth of Labor Productivity | per employed          | TCB       | x              |
| labor_productivity_hour_growth   | Growth of Labor productivity | per hour worked       | TCB       | x              |
| total_hours_worked               | Total Hours worked           | Annual hours          | TCB       | x              |
| working_age_pop_pct              | Population ages 15-64        | % of total population | WDI       | x              |



### Inequality

| *Variable*              | *Unit*            | *Source*                  | *Availability* |
| ----------------------- | ----------------- | ------------------------- | -------------- |
| Gini                    | 0-1               | World Inequality Database | x              |
| Top 10% Income Share    | % of total income | World Inequality Database | x              |
| Bottom 50% Income Share | % of total income | World Inequality Database | x              |
| T10/B50 Ratio           |                   | Calc                      | x              |



### Trade

| Code        | *Variable*                    | *Unit*      | *Source* | *Availability* |
| ----------- | ----------------------------- | ----------- | -------- | -------------- |
| exports_usd | Exports of Goods and Services | current US$ | WDI      | x              |
| exports_gdp | Exports of Goods and Services | % of GDP    | WDI      | x              |
| imports_usd | Imports of Goods and Services | current US$ | WDI      | x              |
| imports_gdp | Imports of Goods and Services | % of GDP    | WDI      | x              |
|             | Trade openness                | % of GDP    | Calc     |                |



### Poverty

| Code              | *Variable*                                     | *Unit*          | *Source* | *Availability* |
| ----------------- | ---------------------------------------------- | --------------- | -------- | -------------- |
| pov_international | Population living below 2.15$ Poverty Line     | % of population | WB       | x              |
| pov_national      | Population living below national poverty lines | % of population | WB       | x              |
| un_multidim_pov   | Multidimensional Poverty Threshold (UNDP)      | % population    | UNDP     | x              |
| Wb_multidim_pov   | Multidimensional Poverty (WB)                  | % of pop        | WB       | x              |



### Investment

|                           | *Variable*                                        | *Unit*             | *Source* | *Availability* |
| ------------------------- | ------------------------------------------------- | ------------------ | -------- | -------------- |
| fdi_in_gdp                | FDI Inflows                                       | % of GDP           | WDI      | x              |
| gross_CF_gdp              | gross capital formation                           | % of GDP           | WDI      | x              |
| private_investment_gdp    | Gross fixed capital formation, private Sector     | % of GDP           | ICSD IMF | x              |
| government_investment_gdp | Gross fixed capital formation, general government | % of GDP           | ICSD IMF | x              |
| rnd_gdp                   | R&D expenditure                                   | % of GDP           | WDI WB   | x              |
| reseearchers_per_million  | Reseeachers in R&D                                | per million people | WDI      | x              |



### Prices

|                  | *Variable*       | *Unit*   | *Source*                     | *Availability* |
| ---------------- | ---------------- | -------- | ---------------------------- | -------------- |
| oil_price_index  | Oil price Index  | 2016=100 | Primary Commodity Prices IMF | x              |
| food_price_index | Food Price Index | 2016=100 | Primary Commodity Prices IMF | x              |



### Socioeconomic

| Code                      | *Variable*                    | *Unit*                  | *Source* | *Availability* |
| ------------------------- | ----------------------------- | ----------------------- | -------- | -------------- |
| life_expectancy           | Life expectancy at birth      | years                   | WDI WB   | x              |
| school_enrollment_primary | School enrollment, primary    | % of relevant age group | WDI WB   | x              |
| remittances_gdp           | Personal Remittances received | $ US Dollar             | WB       | x              |





### Misc

| Code       | *Variable*                  | *Unit* | *Source*                   | *Availability* |
| ---------- | --------------------------- | ------ | -------------------------- | -------------- |
| FHI_pr     | Political Rights Index      |        | Freedom House              | x              |
| FHI_cl     | civil liberties index       |        | Freedom House              | x              |
| FHI_status | Freedom Status              |        | Freedom House              | x              |
| eci        | Economic Complexity Index   |        | OEC                        | x              |
| cpi        | Corruption Perception Index |        | Transparency International | x              |
| hdi        | Human Development Index     |        | UNDP                       | x              |



TODO:

Collier & Goderi
