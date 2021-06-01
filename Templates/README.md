# Templates 

This subdirectory contains template CSV files for inputting supply, demand, technology site, and technology candidate data. These files can then be used for creating case studies in [ADAM](http://54.208.179.171:8000/)

## Supply File 

The supply file contains data on the location, price, and yield of a waste product. 
For models in ADAM, the supply of waste product is cow manure produced by Concentrated Animal Feeding Operations (CAFOs). <br>

The template supply file will look similar to the example below: 

| # | Latitude | Longitude | Product ID | Price | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| s1 | 43.0731 | -89.4012 | p5 | 0 | 500 |
| ...  | ... | ...  | ... | ...  | ... |

<br>
A description of the information that goes under each heading can be found below:
<br>

| Header Symbol | Description |
| ------------- | ------------- | 
| # | ID code for the supply node (i.e. name of the supply node) |
| Latitude | The latitude coordinate at which the node is located. <br> A **positive** number indicates **North**, and a **negative** number indicates **South**. |
| Longitude | The longitude coordinate at which the node is located. <br> A **positive** number indicates **East**, and a **negative** number indicates **West**. |
| Product ID | The product identification code that corresponds to the waste product being produced. <br>*__note: This information can be looked up in the ADAM product database.__* |
| Price | The price of the waste product |
| Capacity | The amount of waste product produced on a time basis (e.g. 1000 tonnes per year). <br> The time basis (i.e. daily, monthy, yearly) is chosen during the first step of creating a new model in ADAM.  <br> *__note: check the ADAM product database for which units to use for each product.__* |

<br>

<p>Using this, we can interpert the entry in the example as a __supply node (denoted "s1")__ located at __43.0731 N, 89.4012 W__ which produces __liquid digestate waste product 
(p5)__ at a yield of __500 tonnes per time basis__.</p>



