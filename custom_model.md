<h1>Custom Model Example</h1>

<h2>Background information</h2>

<p>
  In a custom model, you can provide your own information about the supply, demand, and technologies of your system. Unlike the biogas from waste example (which is a management-type model), a custom model is a <b>design-type model</b>. Rather than simply managing technology sites that already exist, a design-type model will determine whether to build a technology at a certian site. Additionally, it will calculate the performace of the system, including the technologies that were worth building. 
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

<p>The flow data shows the amount of product transported along each pathway (e.g. 10,000 tonnes/year), the transportation data shows the transportation cost of moving the product from one place to another, and the value data shows the value of the products at different locations. 
</p>

<p>
</p>

<br>

<h3>Step 1 - Model Type</h3> 

<br>

<h3>Step 2 - Supply Data</h3> 

<p>
    Click and drag points.  
</p>

<video width="840" controls>
  <source src="Pictures\custom_model\supply_drag.mp4">
Your browser does not support the video.
</video>

<p>
    Edit the capacity and price of the points. 
</p>

<video width="840" controls>
  <source src="Pictures\custom_model\supply_edit.mp4">
Your browser does not support the video.
</video>

<br>

<h3>Step 3 - Technology Data</h3> 

<video width="840" controls>
  <source src="Pictures\custom_model\tech_drag.mp4">
Your browser does not support the video.
</video>

<video width="840" controls>
  <source src="Pictures\custom_model\tech_edit.mp4">
Your browser does not support the video.
</video>

<br>

<h3>Step 4 - Comsumer Data</h3> 

<video width="840" controls>
  <source src="Pictures\custom_model\demand_drag.mp4">
Your browser does not support the video.
</video>

<video width="840" controls>
  <source src="Pictures\custom_model\demand_edit.mp4">
Your browser does not support the video.
</video>

<br>

<h3>Step 5 - Transportation Data</h3> 

<video width="840" controls>
  <source src="Pictures\custom_model\transport_view.mp4">
Your browser does not support the video.
</video>

<br>

<h3>Step 6 - Run Model</h3> 

<img src="Pictures\custom_model\results.png">
