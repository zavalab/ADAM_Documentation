# Input Files

<p>
    In order for ADAM to generate a solution, we must first give it information about the problem we are trying to solve. This information is provided to ADAM in the form of several key data files: the supply file, the demand file, the technology site file, and the technology candidate file. 
</p>

<p>
    In this tutorial, we will go through each of the file types, the information it is providing, and how to interpret an entry.
</p>

<p>
    Templates for each type of file are provided <a href="https://github.com/ADAM-Development/ADAM_Documentation/tree/main/Downloadable_content/Templates">here.</a>
</p>

## Supply File 

<p>
    The supply file contains data on the location, price, and yield of a product. For most models in ADAM, the supply of product is cow manure produced by Concentrated Animal Feeding Operations (CAFOs). 
</p>

<p>
The common headers and their descriptions for the supply file are explained below: 
</p>

| Header Symbol | Description |
| ------------- | ------------- | 
| # | Name of the supply node (up to user preference). |
| Latitude | The latitude coordinate at which the node is located. <br> A **positive** number indicates **North**, and a **negative** number indicates **South**. |
| Longitude | The longitude coordinate at which the node is located. <br> A **positive** number indicates **East**, and a **negative** number indicates **West**. |
| Product ID | The product identification code that corresponds to the waste product being produced. <br>*__note: this can be looked up in the ADAM product database.__* |
| Price | The amount of money that the supplier gains or spends in order to supply a product in USD per product unit (e.g. USD per tonnes). A negative price indicates that the supplier loses money by producing that product. A positive price indicates that the supplier gains money by producing that product. <br> ***note: check the ADAM product database for product units.***  |
| Capacity | The amount of product produced on a time basis (e.g. 1000 tonnes per year). <br> The time basis (i.e. daily, monthly, yearly) is chosen during the first step of creating a new model in ADAM.  <br> *__note: check the ADAM product database for product units.__* |

<br>

<p>
    Here is how it would look in a supply file used in ADAM: 
</p>

| # | Latitude | Longitude | Product ID | Price | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| s1 | 43.0731 | -89.4012 | p5 | 0 | 500 |
| ...  | ... | ...  | ... | ...  | ... |

<p>
    Using the given information, we can interpert the entry in the example above as a supply node, denoted as <b>s1</b>, located at <b>43.0731 N, 89.4012 W</b> which produces <b>liquid digestate waste product (p5)</b> at a yield of <b>500 tonnes</b> per time basis and at <b>zero cost</b> to the supplier.  
</p>

<p>
    <b>Remember:</b> the time basis is defined on the first step of creating a model in ADAM. This information cannot be obtained through looking at the data files. 
</p>

<br>
Now try to interpret this example supply file on your own: 

| # | Latitude | Longitude | Product ID | Price | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| ...  | ... | ...  | ... | ...  | ... |
| s5 | 39.7687 | -76.6797 | p25 | 0.06 | 100 |
| ...  | ... | ...  | ... | ...  | ... |

<details> 
  <summary>Click here to check your answer</summary>
    <p>
        Supply node <b>s5</b> is located at <b>39.7687 N, 76.6797 W</b> which produces <b>Biogas (60% CH4)</b> at a yield of <b>100 cubic meters per time basis</b>, at a cost of <b>0.06 USD per cubic meter</b>.  
    </p>
</details>

## Demand File 

<p>
    The demand data file contains information about the nodes that can demand any products available. These nodes can be CAFOs, technology sites, croplands, external customers, etc.CAFOs and technology sites tend to demand electricity and biogas, croplands tend to demand nutrients from waste products, and external customers demand the valuable products created by technology sites. 
</p>

<p>
    The demand file has the same file headers as the supply file with slightly different interpretations. These headers and their descriptions are explained below: 
</p>

| Header Symbol | Description |
| ------------- | ------------- | 
| # | Name of the demand node (up to user preference). |
| Latitude | The latitude coordinate at which the node is located. <br> A **positive** number indicates **North**, and a **negative** number indicates **South**. |
| Longitude | The longitude coordinate at which the node is located. <br> A **positive** number indicates **East**, and a **negative** number indicates **West**. |
| Product ID | The product identification code that corresponds to the product demanded by the node. <br>*__note: this can be looked up in the ADAM product database.__* |
| Price | The market price of the product per product unit (i.e. the price at which the consumer is purchasing the product). <br> ***note: check the ADAM product database for product units.***  |
| Capacity | The **maximum** amount of product that the node can demand on a per-time basis (e.g. 1000 tonnes per year). The actual amount of product that the demand node receives may be less than or equal to this number. <br> The time basis (i.e. daily, monthly, yearly) is chosen during the first step of creating a new model in ADAM.  <br> *__note: check the ADAM product database for product units.__* |

<br>

<p>
Here is how it would look in a demand file used in ADAM: 
</p>

| # | Latitude | Longitude | Product ID | Price | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| d1 | 43.0731 | -89.4012 | p2 | 0.06 | 1700 |
| ...  | ... | ...  | ... | ...  | ... |

<p>
    We can now interpret <b>d1</b> as a demand node located at <b>43.0731 N, 89.4012 W</b> which demands a <b>maximum of 1700 kWh of bio-electricity</b> per time basis at a price of <b>$0.06 USD per kWh</b>. In other words, d1 is buying bio-electricity at a price of $0.06 per kWh and can buy a maximum of 1700 kWh of bio-electricity per time basis. 
</p>

<p>
    <b>Remember:</b> the time basis is defined on the first step of creating a model in ADAM. This information cannot be obtained through looking at the data files. 
</p>

<p>
Now try to interpret this example supply file on your own: 
</p>

| # | Latitude | Longitude | Product ID | Price | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| ...  | ... | ...  | ... | ...  | ... |
| d32 | 38.9072 | -77.0369 | p24 | 200 | 5250 |
| ...  | ... | ...  | ... | ...  | ... |

<details> 
  <summary>Click here to check your answer</summary>
    <p>
        The demand node, <b>d32</b>, is located at <b>38.9072 N, 77.0369 W</b> and demands <b>5,250 metric tonnes of phosphorus</b> (on a per time basis), at a cost of <b>$200 per metric tonne</b>. 
    </p>
</details>

## Technology Site File 

<p>
    The technology site file contains information on existing and pseudo technologies. These technologies allow for one product to be transformed into another. 
</p>

<p>
    Unlike existing technologies, <b>pseudo technologies</b> are not physical technology sites and thus do not require installation or operational costs. Instead, <b>pseudo technologies represent natural processes such as the release of nutrients into the soil</b>. For example, when struvite, a phosphorus-based fertilizer, is applied to crop fields, the crops do not use the struvite directly. Instead, the struvite releases phosphorus, and the phosphorus is then taken up by crops. ADAM defines this process through a pseudo technology that transforms struvite into phosphorus.
</p>

<br>

<p>
The common headers and their descriptions for the technology site file are explained below: 
</p>

| Header Symbol | Description |
| ------------- | ------------- | 
| # | Name of the technology site node (up to user preference). |
| Latitude | The latitude coordinate at which the node is located. <br> A **positive** number indicates **North**, and a **negative** number indicates **South**. |
| Longitude | The longitude coordinate at which the node is located. <br> A **positive** number indicates **East**, and a **negative** number indicates **West**. |
| Tech ID | The technology identification code that corresponds to the technology at the specified location. <br>*__note: the technology codes can be looked up in the ADAM technology database.__* |
| Capacity | The maximum amount of product that can be processed at a time (e.g. 1000 tonnes per year). <br> The time basis (i.e. daily, monthly, yearly) is chosen during the first step of creating a new model in ADAM.  <br> *__note: the type of product used as input for each technology can be looked up in the technology database__* |

<br> 

<p>
Here is how it would look in a technology site file used in ADAM:
</p>

| # |   Latitude | Longitude | Tech ID | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | 
| ts1 | 41.434208 | -86.876593 | t33 | 10000 |
| ... | ... | ... | ... | ... |

<p>
    We can interpert this entry as a <b>AD-Electricity-SLS (S, cow) technology site</b>, denoted <b>ts1</b>, located at <b>41.434208 N, 86.876593 W</b> with a <b>capacity of processing 10,000 metric tonnes of cow manure</b> per time basis. 
</p>

<br>

<p>
    Now try to interpret this example technology site file on your own: 
</p>

| # |   Latitude | Longitude | Tech ID | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | 
| ... | ... | ... | ... | ... |
| ts23 | 39.045753 | -76.641273 | t60 | 150000 |
| ... | ... | ... | ... | ... |

<details> 
  <summary>Click here to check your answer</summary>
  <p>
    The technology site node, <b>ts23</b>, is a <b>P Release (raw cow manure) technology</b> located at <b>39.045753 N, 76.641273 W</b> with a <b>capacity of processing 150,000 metric tonnes of cow manure</b> (on a per time basis). 
  </p>
</details>

## Technology Candidate File 

<p>
    The technology candidate file provides information on the possible technologies that can be installed at a certain location. This information will be used by ADAM in the model solving process to determine which technologies (if any) to build at each location. 
</p>

<p>
The common headers and their descriptions for the technology candidate file are explained below: 
</p>

| Header Symbol | Description |
| ------------- | ------------- | 
| # | Name of the technology candidate node (up to user preference). |
| Latitude | The latitude coordinate at which the node is located. <br> A **positive** number indicates **North**, and a **negative** number indicates **South**. |
| Longitude | The longitude coordinate at which the node is located. <br> A **positive** number indicates **East**, and a **negative** number indicates **West**. |
| Tech ID | The technology identification code that corresponds to the technology that **could** be installed. <br>*__note: the technology codes can be looked up in the ADAM technology database.__* |

<br>
<p>
Here is how it would look in a technology candidate file used in ADAM:
</p>

| # |   Latitude | Longitude | Tech ID |
| ------------- | ------------- | ------------- | ------------- |
| tc1 | 43.61586956 | -95.8516807 | t15 |
|...| ...| ...| ...|

<p>
This entry, <b>tc1</b>, is saying that <b>it is possible for t15 to be installed at location 43.61586956 N, 95.8516807 W.</b><br>
<b>Note:</b> a single location can take on many different technology candidates.
</p>

<br>

<p>
Now try to interpret this example technology candidate file on your own: 
</p>

| # |   Latitude | Longitude | Tech ID |
| ------------- | ------------- | ------------- | ------------- |
|...| ...| ...| ...|
| tc6 | 43.61586956 | -95.8516807 | t15 |
| tc7 | 43.61586956 | -95.8516807 | t16 |
| tc8 | 43.61586956 | -95.8516807 | t23 |
| tc9 | 39.045753 | -76.641273 | t15 |
|...| ...| ...| ...|

<details> 
  <summary>Click here to check your answer</summary>
  <p>
    Location <b>43.61586956 N, 95.8516807 W</b> is a candidate for installing technologies <b>t15, t16, and t23</b>. <br>
    Location <b>39.045753 N, 76.641273 W</b> is a candidate for installing technology <b>t15</b>. <br><br>
    To check the corresponding technologies to the technology IDs, please check the ADAM technology database.<br> 
  </p>
</details>

<br>
<br>

<a href="dashboard.html">Return to Dashboard Tutorials</a>

