# Templates 

This subdirectory contains template CSV files for inputting supply, demand, technology site, and technology candidate data. These files can then be used for creating case studies in [ADAM.](http://54.208.179.171:8000/) Each template contains a single entry as an example. 

For more information on each type of file see below.
<br>
<br>

## Supply File 

The supply file contains data on the location, price, and yield of a waste product. 
For most models in ADAM, the supply of waste product is cow manure produced by Concentrated Animal Feeding Operations (CAFOs). 
<br>

<br>
The common headers and their descriptions for the supply file are explained below: 
<br>

| Header Symbol | Description |
| ------------- | ------------- | 
| # | Name of the supply node (up to user preference). |
| Latitude | The latitude coordinate at which the node is located. <br> A **positive** number indicates **North**, and a **negative** number indicates **South**. |
| Longitude | The longitude coordinate at which the node is located. <br> A **positive** number indicates **East**, and a **negative** number indicates **West**. |
| Product ID | The product identification code that corresponds to the waste product being produced. <br>*__note: this can be looked up in the ADAM product database.__* |
| Price | The price of the waste product in USD per product unit (e.g. USD per tonnes). <br> ***note: check the ADAM product database for product units.***  |
| Capacity | The amount of waste product produced on a time basis (e.g. 1000 tonnes per year). <br> The time basis (i.e. daily, monthy, yearly) is chosen during the first step of creating a new model in ADAM.  <br> *__note: check the ADAM product database for product units.__* |
<br>


Here is how it would look in a supply file used in ADAM: 

| # | Latitude | Longitude | Product ID | Price | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| s1 | 43.0731 | -89.4012 | p5 | 0 | 500 |
| ...  | ... | ...  | ... | ...  | ... |

Using the given information, we can interpert the entry in the example above as a supply node (which is denoted "s1" for simplicity) located at 43.0731 N, 89.4012 W which 
produces liquid digestate waste product (p5) at a yield of 500 tonnes per time basis and at zero cost to the supplier.  

**Remember:** time is defined on the first step of creating a model in ADAM, so there is no way to know the time basis from the supply file alone.

<br>
Now try to interpert this example supply file on your own: 

| # | Latitude | Longitude | Product ID | Price | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| ...  | ... | ...  | ... | ...  | ... |
| s5 | 39.7687 | -76.6797 | p25 | 0.06 | 100 |
| ...  | ... | ...  | ... | ...  | ... |

<details> 
  <summary>Check your answer here.</summary>
  <br>
  Supply node s5 is located at 39.7687 N, 76.6797 W which produces Biogas (60% CH4) at a yield of 100 cubic meters per time basis, at a cost of 0.06 USD per cubic meter.  
</details>
<br>

## Demand File 

The demand data file contains information about the nodes that can demand any products available. These nodes can be CAFOs, technology sites, croplands, external customers, etc.
CAFOs and technology sites tend to demand electricity and biogas, croplands tend to demand nutrients from waste products, and external customers demand the valuable products 
created by technology sites. 

<br>
The demand file has the same file headers as the supply file with slightly different interpertations. These headers and their descriptions are explained below: 
<br>

| Header Symbol | Description |
| ------------- | ------------- | 
| # | Name of the demand node (up to user preference). |
| Latitude | The latitude coordinate at which the node is located. <br> A **positive** number indicates **North**, and a **negative** number indicates **South**. |
| Longitude | The longitude coordinate at which the node is located. <br> A **positive** number indicates **East**, and a **negative** number indicates **West**. |
| Product ID | The product identification code that corresponds to the product demanded by the node. <br>*__note: this can be looked up in the ADAM product database.__* |
| Price | The market price of the product per product unit (i.e. the price at which the node is purchasing the product). <br> ***note: check the ADAM product database for product units.***  |
| Capacity | The **maximum** amount of product that the node can demand on a per time basis (e.g. 1000 tonnes per year). The actual amount of product that the demand node receives may be less than or equal to this number. <br> The time basis (i.e. daily, monthy, yearly) is chosen during the first step of creating a new model in ADAM.  <br> *__note: check the ADAM product database for product units.__* |

<br>

Here is how it would look in a demand file used in ADAM: 
| # | Latitude | Longitude | Product ID | Price | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| d1 | 43.0731 | -89.4012 | p2 | 0.06 | 1700 |
| ...  | ... | ...  | ... | ...  | ... |

We can now interpert d1 as a demand node located at 43.0731 N, 89.4012 W which demands a maximum of 1700 kWh of bio-electricity per time basis at a price of $0.06 USD per kWh.
In other words, d1 is buying bio-electricity at a price of $0.06 USD per kWh and can buy a maximum of 1700 kWh of bio-electricity per time basis. 
**Remember:** time is defined on the first step of creating a model in ADAM, so there is no way to know the time basis from the supply file alone.

<br>
Now try to interpert this example supply file on your own: 

| # | Latitude | Longitude | Product ID | Price | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| ...  | ... | ...  | ... | ...  | ... |
| d32 | 38.9072 | -77.0369 | p24 | 200 | 5250 |
| ...  | ... | ...  | ... | ...  | ... |

<details> 
  <summary>Check your answer here.</summary>
  <br>
  The demand node, d32, is located at 38.9072 N, 77.0369 W and demands 5,250 metric tonnes of phosphorus (on a per time basis), at a cost of $200 per metric tonne. 
</details>
<br>


## Technology Site File 

The technology site file contains information on existing and pseudo technologies. 

<br>

**Pseudo technologies** are not physical techology site and thus do not require installation or operational costs. Instead, pseudo technologies represent natural processes such as fertilizers releasing nutrients into the soil. For example, when struvite, a phosphorus-based fertilizer, is applied to cropfields, the crops do not use the struvite directly. Instead, the struvite releases phosphorus, and the phosphorus is then taken up by crops. In order to represent this process in ADAM, a pseduo technology that transforms struvite to phosphorus is defined. 

<br>
The common headers and their descriptions for the technology site file are explained below: 
<br>

| Header Symbol | Description |
| ------------- | ------------- | 
| # | Name of the technology site node (up to user preference). |
| Latitude | The latitude coordinate at which the node is located. <br> A **positive** number indicates **North**, and a **negative** number indicates **South**. |
| Longitude | The longitude coordinate at which the node is located. <br> A **positive** number indicates **East**, and a **negative** number indicates **West**. |
| Tech ID | The technology identification code that corresponds to the technology at the specified location. <br>*__note: this can be looked up in the ADAM technology database.__* |
| Capacity | The maximum amount of product that can be processed at a time (e.g. 1000 tonnes per year). <br> The time basis (i.e. daily, monthy, yearly) is chosen during the first step of creating a new model in ADAM.  <br> *__note: check the ADAM product database for product units.__* |
<br>

