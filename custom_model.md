<h1>Custom Model Example</h1>

<h2>Background information</h2>

<p>
  In a custom model, you can provide your own information about the supply, demand, and technologies of your system. For this example, we will be exploring a different type of model: <b>a design-type model</b>. Rather than simply managing technology sites that already exist, a design-type model will determine whether to build a technology at a certian site. Additionally, it will calculate the performace of the system, including the technologies that were worth building. 
</p>

<br>

<h2>Outline</h2>

<p>In order to navigate to the custom model example, click the <b>Tutorial</b> on the top right and select the <b>Custom Model</b> option. The first screen you encounter is the <b>Outline Page</b>. This page provides an overview of the steps we will go over during the tutorial. 
</p>

<p>You may select any of the icons to jump to that part of the tutorial. For first-time users, we reccomend selecting the <b>Preliminary - Input Data</b> step.</p>

<img src = "Pictures\custom_model\outline.png">

<br> 

<h3>Preliminary - Input Data</h3> 

<img src="Pictures\custom_model\input_dat.png">

<p>
  Similar to the biogas from waste example, the inputs for the custom model are supply data, customer data, technology data, and trasportation data. The only difference is the information included in the technology data.
</p>

<p>
 In the biogas from waste example, the technology data only included information about existing technology sites. This makes sense since the biogas from waste model is a management-type model; however, for a design-type model, we must also consider <b>technology candidates</b>, sites where technologies could potentially be built. 
</p>

<p>
  All other inputs are the same as the biogas from waste example except the suppliers and customers are generic; the suppliers do not need to be CAFOs which supply cattle waste and the consumers do not need to be the same as the ones in the biogas from waste example. 
</p>

<br>

<a href="/ADAM_Documentation/biogas_from_waste.html">See Biogas from Waste Example Here</a>
<br>
<a href="/ADAM_Documentation/input_files.html">More information on the input files</a>


<br>

<h3>Preliminary - Output Data</h3> 

<img src="Pictures\custom_model\output_dat.png">

<p>
  The outputs of the custom model includes flow data, transportation data, value data, and design data. 
</p>

<p>The flow data shows the amount of product transported along each pathway, the transportation data shows the transportation cost of moving the product from one place to another, the value data shows the value of the products at different locations, and the design data shows the technologies that should be installed at each location. 
</p>

<br>

<h3>Step 1 - Model Type</h3> 

<img src="Pictures\custom_model\step1.png">

<p>
  For the first step of creating a model, we must define the model-type and time-basis. As stated before, this example will go over a design-type model. The time-basis is left as year which is the default setting.
</p>

<br>

<h3>Step 2 - Supply Data</h3> 

<p>
  The supply data of a custom model can be anything that supplies a product (usually a waste product). In this example three CAFOs acting as supply nodes are provided; you can click and drag the nodes or edit the data as you wish. 
</p>

<p>
    Click and drag points.  
</p>

<video width="840" controls>
  <source src="Pictures\custom_model\supply_drag.mp4">
Your browser does not support the video.
</video>

<br>

<p>
    We can edit the capacity and price of the points. Remember that capacity refers to the amount of product that the supply node produces, and the price refers to the cost of the product to the supplier. 
</p>

<p>
  The video below shows the capacity of CAFO1 being changed from 65,000 to 50,000 tonnes of manure per year; the price is changed from costing the CAFO $5 per tonne to $10 per tonne. Remember that a <b>negative price indicates cost</b>. 
</p>

<video width="840" controls>
  <source src="Pictures\custom_model\supply_edit.mp4">
Your browser does not support the video.
</video>

<br>

<h3>Step 3 - Technology Data</h3> 

<p>
  The technology data includes <b>technology sites</b>, which are locations that have pre-existing technologies, and <b>technology candidates</b>, which are locations where a technology could be built. 
</p>

<p>In this example, there are two technology sites (blue) and one technology candidate (red). You can click and drag these points to different locations.
</p>

<video width="840" controls>
  <source src="Pictures\custom_model\tech_drag.mp4">
Your browser does not support the video.
</video>

<br> 

<p>
  You can also double-click to edit the capacities of the technology sites. The technology candidate node cannot be edited.In the video below, Technology1's capacity is changed from 60,000 to 80,000 tonnes of waste. This means that Technology1 can now process 20,000 more tonnes of waste than it could before.  
</p>

<video width="840" controls>
  <source src="Pictures\custom_model\tech_edit.mp4">
Your browser does not support the video.
</video>

<br>

<h3>Step 4 - Comsumer Data</h3> 

<p>
  The consumers in this model are any person, place, or thing that demands a product and are indicated by the green nodes. You can click and drag the nodes to different locations. 
</p>

<video width="840" controls>
  <source src="Pictures\custom_model\demand_drag.mp4">
Your browser does not support the video.
</video>

<br>

<p>
  Similar to the other steps we have encountered, you can also double-click the nodes to edit the demand information about each consumer. In the video below, Consumer4's capacity is changed from 30,000 to 60,000 gallons of biomethane per year, and it's price is changed from $3,000 to $3,500 per gallon. This means that Consumer4 now demands a maximum of 60,000 gallons of biomethane per year and is willing to buy the biomethane at a price of $3,500 per gallon. 
</p>

<video width="840" controls>
  <source src="Pictures\custom_model\demand_edit.mp4">
Your browser does not support the video.
</video>

<br>

<h3>Step 5 - Transportation Data</h3> 

<p>
  The transportation data gives information on the product that is being transported, the transportation cost, and the distance that the product is transported. 
</p>

<p>
  You can hover over each transportation route to see detailed information and click to see the estimated time and the distance for that pathway. The "true distance" refers to the distance that the vehicle travels in order to get from one point to another. "Distance" simply refers to the distance between one point to another if you were to travel in a straight line. 
</p>

<p>
  The video below demonstrates how to display the pathway details on the left and right graphs. It can be a bit tricky to find out exactly where to hover over the route to display the information. 
</p>

<video width="840" controls>
  <source src="Pictures\custom_model\transport_view.mp4">
Your browser does not support the video.
</video>

<br>

<h3>Step 6 - Run Model</h3> 

<p>
  After you have completed steps 1 through 5, you will have the option to run the model. Using the data that you have provided, ADAM will then find the optimal routes that the products will take, and it will determine whether or not the technology should be installed at the technology candidate location. 
</p>

<img src="Pictures\custom_model\run.png">

<p>
  Running the model may take a few minutes. Please do not refresh or exit out of the page while it is running. 
</p>

<p>An example of the results is shown below. The left graph shows that two out of the three CAFOs should send their waste to a technology site. Since there is a pathway going to the technology candidate node, this means that building the technology and processing waste there is worth doing. 
</p>

<p>
  The right graph shows the product pathways from the technology sites to the consumers. Hovering over the pathways would quantitatively show the amount of product that is being transported across that pathway and the total transportation cost of moving that amount of product. 
</p>


<img src="Pictures\custom_model\results.png">

<p>
  Please try moving and editing points on your own to get familiar with ADAM! 
</p>
