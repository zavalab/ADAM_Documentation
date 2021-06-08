<h1>Biogas From Waste Example</h1> 

<h2>Background Information</h2> 

<p>In the Biogas From Waste example, cattle farms produce manure which is then processed by technology sites. These technology sites use anaerobic digestion to produce biogas. This biogas is then purchased by customers.</p>

<img src="Pictures\biogas_from_waste_ex\process.png">

<p>Since there are many cattle farms, technology sites, and consumers, there are many combinations of pathways that the manure and biogas can take. We would like to find out which pathway is the most economically favorable.</p>

<p>We only want to manage sites that already exist; we are not considering building new technology sites. This type of problem can be defined as a management-type model. </p>

<br>

<h2>Walkthrough</h2>

<h3>Outline</h3>

<p>In order to navigate to the biogas from waste example, click the <b>Tutorial</b> on the top right and select the <b>Biogas from Waste</b> option. The first screen you encounter is the <b>Example Outline Page</b>. This page provides an overview of the steps we will go over during the tutorial. 
</p>

<p>You may select any of the icons to jump to that part of the tutorial. For first-time users, we reccomend selecting the <b>Preliminary - Input Data</b> step.
</p>

<img src="Pictures\biogas_from_waste_ex\overview.png">

<br>

<h3>Preliminary - Input Data</h3> 

<p>The first page of the tutorial gives you information about the input data needed for ADAM. This input data consists of supply data, demand data, technology data, and transportation data.</p>

<img src="Pictures\biogas_from_waste_ex\prelim.png">

<h5>The Supplier Data</h5>

<p>In the case of biogas to waste, the suppliers are CAFOs which produce cattle manure. The supplier data includes several pieces of information about each CAFO: their location, the amount of manure produced (capacity), and the cost of the waste to the supplier. 
</p>

<h5>The Consumer Data</h5>

<p>The consumers are any person or organization that purchases a valuable products. Similar to the supplier data, the consumer data includes the following information about each consumer: their location, the maximum amount of product they can purchase (capacity), and the unit price at which they are buying the product. In this case, the only product of value is the biogas produced by the technology sites. 
</p>

<h5>The Technology Data</h5>

<p>Technologies are any construct that can transform one product into another. In the context of biogas from waste, the technology being used is an anerobic digester uses cattle manure to produce biogas (main product) and digestate (waste product). The technology data includes the location and type of technology installed. 
</p>

<h5>The Transportation Data</h5>

<p>The transportation data includes information on the transportation costs of each product based on distance traveled. 
</p>

<br>

<h3>Step 1 - Model Type</h3> 

<img src="Pictures\biogas_from_waste_ex\step1.png">

<p>Now that we have gone over the input data for this example, we can now select the model-type and time-basis. As stated before, since we are only focusing on managing existing technologies, we select a management type model rather than a design-type model (the custom model demonstrates the design type-model).
</p>

<p>The time basis is set to <b>Year</b>. When defining the capacities, make sure the units are consistent with the time basis selected. 
</p>

<br>

<h3>Step 2 - Supplier Data</h3>

<img src="Pictures\biogas_from_waste_ex\step2.png">

<p>
    After defining the model type and time basis, we can now add supplier data. In this example, there are three suppliers (CAFOs) which are indicated by the yellow markers on the map.
</p>

<p>
    By double-clicking on any of the markers, you can get more detailed information about each node. An example of the detailed information is shown below. 
</p>

<img src="Pictures\biogas_from_waste_ex\sup_info.png">

<p>
    Here we see that this supply node is located at a longitude and latitude of 43.1263, -89.5514. It produces waste at a capacity of 65,000 tonnes per year (the "per year" was defined in step 1) at a cost of $5 USD per tonne of waste produced. 
</p>

<p>A negative price indicates that the supplier is losing money by supplying waste. 
</p>

<br>

<h3>Step 3</h3>

<img src="Pictures\biogas_from_waste_ex\step3.png">

<p>
    In step 3, we define the location, capacity, technology type, and operating cost for each technology node. In this example, we have two technology nodes which are shown on the map as the blue markers.
</p>

<p>
    Similar to the supply nodes, double-clicking on the technology nodes will give you more information about that node. An example of the detailed information is shown below. 
</p> 

<br>

<img src="Pictures\biogas_from_waste_ex\tech_info.png">

<p>
    From this detailed information, we can determine that this is an anaerobic digestion type technology located at a longitude and latitude of 43.1729, -89.5036. It is able to process up to 60,000 tonnes of waste per year (again the "per year" was defined in step 1) at a cost of $6 USD per tonne of waste processed.
</p>

<p>
    The diagram below the detailed information shows the inputs and outputs of the technology. For every 1 tonne of waste, the anaerobic digestion technology produces 1500 cubic ft of biogas and 0.95 tonnes of digestate. 
</p>

<br>

<h3>Step 4</h3>

<img src="Pictures\biogas_from_waste_ex\step4.png">

<br>

<h3>Step 5</h3>
<br>

<h3>Step 6</h3>

<br>

<h3>Output Data</h3>