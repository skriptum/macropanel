# Commodity Price Index



Constructing a commodity price index like [Dehn (2000)](https://ora.ox.ac.uk/objects/uuid:c42f6d43-6808-4a23-8d3b-31e1905c78f8/files/sdn39x2083) or [Collier and Goderis (2012)](https://www.sciencedirect.com/science/article/pii/S0014292112000505)



### Calculation


$$
W_{ic} = \frac{(x-m)_{ci}}{\sum (x-m)_{ci}} \text{ for all } (x-m)_{ci} > 0
$$
The weight of each commodity *i* is

- net exports for commodity (for which country is a net exporter)
- by all exports of the country

All in a given base year

$$
P_{ct} = \prod_i p_{it}^{W_{ci}}
$$

The country specific index $DM{ct}$ is the product of

- $P_it$ = commodity price *i* at given time *t*
- $W_{ci}$ weighted by commodity weight 



Then deflate by
$$
P^{real}_{ct} = \log \frac{P_{ct}}{e_t}
$$

- e = world exports value



also weigh by share of exports in countries GDP (shocks impact more export oriented countries more)
$$
x_{i} = \frac{\sum (x-m)_{ci}}{GDP} \text{ for all ...}
$$

- in the base year 1990
- for all net export commodities



Then:
$$
P_{xct} = x_i * P^{real}_{ct}
$$


### Data

- Commodity prices for a large basket -> IMF PCPS
- Export values for each country and commodity -> UNCTAD
- a lot of time



### Risks

Adjustment of base year only every 10 years (or never) does not caputre resource discoveries / quantity shocks

=> only price shocks, but guards from endogeneity concerns

TODO: show correlation between the different base years in the exports