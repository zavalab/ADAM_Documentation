<h1>Biogas From Waste Example</h1> 

<h2>Background Information</h2> 

<p>In the Biogas From Waste example, cattle farms produce manure which is then processed by technology sites. These technology sites use anaerobic digestion to produce biogas. This biogas is then purchased by customers or used by the technology site locally.</p>

<img src="Pictures\biogas_from_waste_ex\process.png">

<p>Since there are many cattle farms, technology sites, and consumers, there are many combinations of pathways that the manure and biogas can take. We would like to find out which pathway is the most economically favorable.</p>

<p>We only want to manage sites that already exist; we are not considering building new technology sites. This type of problem can be defined as a <b>management-type model</b>.
</p>

<br>

<h2>Outline</h2>

<p>In order to navigate to the biogas from waste example, click the <b>Tutorial</b> on the top right and select the <b>Biogas from Waste</b> option. The first screen you encounter is the <b>Outline Page</b>. This page provides an overview of the steps we will go over during the tutorial. 
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

<p>The consumers are any person or organization that purchases a valuable product. Similar to the supplier data, the consumer data includes the following information about each consumer: their location, the maximum amount of product they can purchase (capacity), and the unit price at which they are buying the product. In this case, the only product of value is the biogas produced by the technology sites. 
</p>

<h5>The Technology Data</h5>

<p>Technologies are any construct that can transform one product into another. In the context of biogas from waste, the technology being used is an anerobic digester uses cattle manure to produce biogas (main product) and digestate (waste product). The technology data includes the location and type of technology installed. 
</p>

<h5>The Transportation Data</h5>

<p>The transportation data includes information on the transportation costs of each product based on distance traveled. 
</p>

<br>

<h3>Preliminary - Output Data</h3>

<img src = "Pictures\biogas_from_waste_ex\prelim_output.png">

<p>After we give ADAM all of the input data, ADAM will generate output data which includes information about the flow, transporation, and value data. 
</p>

<p>The flow data shows the amount of product transported along each pathway (e.g. 10,000 tonnes/year), the transportation data shows the transportation cost of moving the product from one place to another, and the value data shows the value of the products at different locations. 
</p>

<br>

<h3>Step 1 - Model Type</h3> 

<img src="Pictures\biogas_from_waste_ex\step1.png">

<p>Now that we have gone over the input and output data for this example, we can now select the model-type and time-basis. As stated before, since we are only focusing on managing existing technologies, we select a management type model rather than a design-type model (the custom model demonstrates the design type-model).
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

<p><b>A negative price indicates that it costs money for the supplier to supply waste</b>.</p>

<br>

<h3>Step 3 - Technology Data</h3>

<img src="Pictures\biogas_from_waste_ex\step3.png">

<p>
    In step 3, we define the technology nodes. In this example, we have two technology nodes which are shown on the map as the blue markers.
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

<h3>Step 4 - Consumer Data</h3>

<img src="Pictures\biogas_from_waste_ex\step4.png">

<p>In step 4, we define the consumer (demand) data. In this example we have three demand data nodes indicated on the map as green markers. Note that the topmost node is both a supply and a demand node, indicated by a half-green and half-yellow marker. This is not exclusive to just supply and demand. A single node can act as a supply, demand, and technology node or any combination of the three. 
</p>

<p>Double-clicking on the demand node will open more detailed information about that node.
</p>

<img src="Pictures\biogas_from_waste_ex\dem_info.png">

<p>
    This consumer demands two different products: digestate and waste. Digestate is the waste product of the technology after it processes waste into biogas. The consumer demands 115,000 tonnes per year of both digestate and waste. They purchase the digestate at a price of $5 USD per tonne, and they get the waste at no cost. The consumer is able to get the waste at zero cost because the supplier loses money by producing waste so the supplier would like to get rid of the waste while sustaining as little losses as possible.  
</p>

<p>This consumer only wants the waste products, meaning that this consumer is likely a crop field which demands the nutirents from the manure. 
</p>

<br>

<h3>Step 5 - Transport Data</h3>

<img src="Pictures\biogas_from_waste_ex\step5.png">

<p>
    After defining all of the supply, demand, and technology nodes, we can now define transportation data. The graph on the left shows all possible transportation routes for waste and the graph on the right shows all transportation routes for every other product. 
</p>

<p>
    Hovering over the route until the white information box appears, then clicking on the route will display additional information. 
</p>

<img src="Pictures\biogas_from_waste_ex\trans_info.png">

<p>
    This route is between the markers labeled CAFO2 and Technology2. The distance between the markers is 6.49 km, the product being transported is waste, and the waste is being transported at a cost of 3 USD per tonne per km. The box in the lower right corner shows that the "true" distance (i.e. the distance it would take to drive from one point to another using roads) is 8.56 km. It also gives a time estimate based on an average car's speed. 
</p>

<br>

<h3>Step 6</h3>

<img src = "Pictures\biogas_from_waste_ex\step6.png">

<p>
    The final step is running the model using ADAM to find the optimal routes that each of the products should take. Hovering over and clicking on the routes will show the amount of product flow and the transportation cost that will allow each member of the system to have maximum benefits. 
</p>

<p>
    In this case, it appears that it is most favorable for each of the supply nodes to send a portion of their waste to be processed at a technology site. One of the technology sites produces digestate and biogas, and the other produces digestate and electricity. Consumer1 buys the biogas, Consumer2 buys the digestate, and Consumer3 buys the electricity. 
</p>

<img src="Pictures\biogas_from_waste_ex\run_info.png">

<p>
    Looking at the same pathway as before, there is now information about the amount of waste transported (product flow). In this case, waste is being transported across this pathway at a rate of 20,294.12 tonnes/year with a transportation cost of $395,126.52. 
</p>

<br>

