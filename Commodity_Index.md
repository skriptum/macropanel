# Background on the Commodity price index

We construct a country-specific commodity price index to measure how changes in world market prices affect different economies depending on what they export. The idea is to combine global commodity prices into one index per country, weighting each price by that country’s net export share and scaling it by export dependence, so it captures external price shocks rather than domestic quantity changes. The index is inspired by [Dehn (2000)](https://ora.ox.ac.uk/objects/uuid:c42f6d43-6808-4a23-8d3b-31e1905c78f8/files/sdn39x2083) or [Collier and Goderis (2012)](https://www.sciencedirect.com/science/article/pii/S0014292112000505) and builds partly upon their approaches.  

### Basic Formula

The starting point is this formula:

$$
P_{ct} = \prod_i p_{it}^{W_{ci}}
$$

The country specific index $P_{ct}$ is the product of

- $p_{it}$ = commodity price *i* at given time *t*
- $W_{ci}$ weighted by commodity weight 



The weight of each commodity *i* is

- exports for commodity (for which country is a net exporter) divided by
- by all exports of the country

$$
W_{ic} = \frac{(x-m)_{ci}}{\sum (x-m)_{ci}} \text{ for all } (x-m)_{ci} > 0
$$



### Filtering

Missing data points in series can seriously distort the index due to its nature as a product of all commodities. Therefore, we filter out country-commodity series with data gaps, if they make up less than 10% of exports (similar to other authors in the literature).



### Deflating


To account for general growth trends in world trade, we divide the index with the World Exports value in a given year (taken from the World Banks Pink Sheet) and apply a log.

$$
P^{real}_{ct} = \log \frac{P_{ct}}{e_t}
$$



### GDP-Weighting

We also weigh by share of exports in countries GDP (so that price shocks impact more export oriented countries more)

$$
x_{i} = \frac{\sum (x-m)_{ci}}{GDP} \text{ for all ...}
$$

- in the base year 1990
- for all net export commodities



Our final index then:

$$
P_{xct} = x_i * P^{real}_{ct}
$$



## Requirements 

To recreate this index, you need:

- Commodity prices for a large basket (from IMF PCPS)
- Export values for each country and commodity (from UNCTAD / CEPII)
- a lot of time and patience

Take a look at `./src/02_commodity/` to get a grasp on the code



## Risks

We never adjust the base year, so the index does not capture new resouce discoveries or quantity shocks in a country. This constraint is needed to differentiate between price effects and quantitiy effects (and it is less of a problem because of high correlations between different base years)



## List of Commodities



| Commodity Name               | Metric (Unit) |
| ---------------------------- | ------------- |
| Cocoa                        | $/mt          |
| Coffee, Arabica              | $/mt          |
| Coffee, Robusta              | $/mt          |
| Tea, Average                 | $/mt          |
| Coconut Oil                  | $/mt          |
| Palm Oil                     | $/mt          |
| Soybeans                     | $/mt          |
| Barley                       | $/mt          |
| Maize (Corn)                 | $/mt          |
| Rice (5% broken)             | $/mt          |
| Wheat (US HRW)               | $/mt          |
| Bananas (US)                 | $/mt          |
| Oranges                      | $/mt          |
| Beef                         | $/mt          |
| Chicken                      | $/mt          |
| Lamb                         | $/mt          |
| Sugar (World)                | $/mt          |
| Tobacco (US)                 | $/mt          |
| Plywood                      | $/m³          |
| Cotton (A Index)             | $/mt          |
| Rubber (TSR20, Malaysia)     | $/mt          |
| Crude Oil (Average)          | $/bbl         |
| Natural Gas (Europe)         | $/mmbtu       |
| Coal (Australia)             | $/mt          |
| Phosphate Rock               | $/mt          |
| Diammonium Phosphate (DAP)   | $/mt          |
| Triple Super Phosphate (TSP) | $/mt          |
| Urea (EE bulk)               | $/mt          |
| Potash                       | $/mt          |
| Aluminum                     | $/mt          |
| Iron Ore (CFR spot)          | $/mt          |
| Copper                       | $/mt          |
| Lead                         | $/mt          |
| Tin                          | $/mt          |
| Nickel                       | $/mt          |
| Zinc                         | $/mt          |
| Gold                         | $/troy oz     |
| Platinum                     | $/troy oz     |
| Silver                       | $/troy oz     |
