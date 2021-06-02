# Templates 

This subdirectory contains template CSV files for inputting supply, demand, technology site, and technology candidate data. These files can then be used for creating case studies in [ADAM.](http://54.208.179.171:8000/) Each template contains a single entry as an example. 

<br>
For more information on each type of file see below.
<br>
<br>

<details> 
  <summary>Contents</summary>
  <br>
    <ol>
      <li><a href="https://github.com/mshen42/ADAM_Tutorial/tree/main/Templates#supply-file">Supply File</a></li>
      <li><a href="https://github.com/mshen42/ADAM_Tutorial/tree/main/Templates#demand-file">Demand File</a></li>
      <li><a href="https://github.com/mshen42/ADAM_Tutorial/tree/main/Templates#technology-site-file">Technology Site File</a></li>
      <li><a href="https://github.com/mshen42/ADAM_Tutorial/tree/main/Templates#technology-candidate-file">Technology Candidate File</a></li>
    </ol>  
  <br>
</details>

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

Using the given information, we can interpert the entry in the example above as a supply node, denoted as **s1**, located at **43.0731 N, 89.4012 W** which 
produces **liquid digestate waste product (p5)** at a yield of **500 tonnes per time basis** and at **zero cost** to the supplier.  

**Remember:** the time basis is defined on the first step of creating a model in ADAM. This information cannot be obtained through looking at the data files. 

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
  Supply node <b>s5</b> is located at <b>39.7687 N, 76.6797 W</b> which produces <b>Biogas (60% CH4)</b> at a yield of <b>100 cubic meters per time basis</b>, at a cost of <b>0.06 USD per cubic meter</b>.  
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

We can now interpert **d1** as a demand node located at **43.0731 N, 89.4012 W** which demands a **maximum of 1700 kWh of bio-electricity** per time basis at a price of **$0.06 USD per kWh.**
In other words, d1 is buying bio-electricity at a price of $0.06 USD per kWh and can buy a maximum of 1700 kWh of bio-electricity per time basis. 

**Remember:** the time basis is defined on the first step of creating a model in ADAM. This information cannot be obtained through looking at the data files. 

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
  The demand node, <b>d32</b>, is located at <b>38.9072 N, 77.0369 W</b> and demands <b>5,250 metric tonnes of phosphorus</b> (on a per time basis), at a cost of <b>$200 per metric tonne</b>. 
</details>
<br>


## Technology Site File 

The technology site file contains information on existing and pseudo technologies. 

<br>

Unlike existing technologies, **pseudo technologies** are not physical techology sites and thus do not require installation or operational costs. Instead, **pseudo technologies represent natural processes such as the release of nutrients into the soil**. For example, when struvite, a phosphorus-based fertilizer, is applied to cropfields, the crops do not use the struvite directly. Instead, the struvite releases phosphorus, and the phosphorus is then taken up by crops. ADAM defines this process through a pseudo technology which transforms strufite into phsophorus.

<br>
The common headers and their descriptions for the technology site file are explained below: 
<br>

| Header Symbol | Description |
| ------------- | ------------- | 
| # | Name of the technology site node (up to user preference). |
| Latitude | The latitude coordinate at which the node is located. <br> A **positive** number indicates **North**, and a **negative** number indicates **South**. |
| Longitude | The longitude coordinate at which the node is located. <br> A **positive** number indicates **East**, and a **negative** number indicates **West**. |
| Tech ID | The technology identification code that corresponds to the technology at the specified location. <br>*__note: this can be looked up in the ADAM technology database.__* |
| Capacity | The maximum amount of product that can be processed at a time (e.g. 1000 tonnes per year). <br> The time basis (i.e. daily, monthy, yearly) is chosen during the first step of creating a new model in ADAM.  <br> *__note: the type of product used as input for each technology can be looked up in the technology database__* |

<br>

Here is how it would look in a technology site file used in ADAM:
| # |	Latitude | Longitude | Tech ID | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | 
| ts1 | 41.434208 | -86.876593 | t33 | 10000 |
| ... | ... | ... | ... | ... |

We can interpert this entry as a **AD-Electricity-SLS (S, cow) technology site**, denoted **ts1**, **located at 41.434208 N, 86.876593 W** with a **capacity of processing 10,000 metric tonnes of cow manure** per time basis. 


<br>
Now try to interpert this example technology site file on your own: 

| # |	Latitude | Longitude | Tech ID | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | 
| ... | ... | ... | ... | ... |
| ts23 | 39.045753 | -76.641273 | t60 | 150000 |
| ... | ... | ... | ... | ... |

<details> 
  <summary>Check your answer here.</summary>
  <br>
  The technology site node, <b>ts23</b>, is a <b>P Release (raw cow manure) technology</b> located at <b>39.045753 N, 76.641273 W</b> with a <b>capacity of processing 150,000 metric tonnes of cow manure</b> (on a per time basis). 
</details>
<br>



## Technology Candidate File 
