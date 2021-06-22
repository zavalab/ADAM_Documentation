<h1>Editing the Model</h1>

<p>
    Now that you have learned how to make a copy and run a case study, we will now go over how to edit the information in the case study. Knowing how to edit a case study allows you to make alterations to the case study as you please.
</p>

<p>
    This tutorial will go over each step in the model and demonstrate the changes you can make to the model. 
</p>

<h2>Step 1 - Model Type</h2>

<p>
    Step 1 is where the model type and time basis are defined. For a copied model, you should leave the model type and time basis as is. Running a model as a management-type model will give different result files than running the model as a design-type model. As a rule of thumb, design-type models have technology candidates whereas management-type models do not. 
</p>

<img src="Pictures\Dashboard_tutorials\edit_model\step1.png">

<p>
    Since the waste to energy example does not have technology candidates, it is a management-type model. 
</p>

<h2>Steps 2, 3, 4 - Adding Supply, Technology, and Demand Data</h2>

<p>
    For steps 2-4, you can double-click the nodes from the case study to edit their information. 
</p>

<img src="Pictures\Dashboard_tutorials\edit_model\step2.png">

<p>
    In addition to editing existing nodes, you may also add new data. <b>Upload Data</b> is used when you have a CSV file containing data points you would like to add. Otherwise, you can add a singular node by selecting <b>Manual Entry</b> and then filling out the required information. <b>Load from Model</b> allows you to select other models from your model list and import their data into this model. 
</p>

<p>
    For more detailed information on adding new data, please go to 
<a href="/ADAM_Documentation/dashboard_input_data.html">this tutorial</a>.
    
</p>

<p>
    If you upload the wrong file, you can use <b>Clear Data</b> to clear all supply data from the model. If you want to delete a single node, you can right-click on the node. The final option, <b>Look for a Feedstock</b>, allows you to look through the product database and see detailed information about each product. 
</p>

<h2>Step 5 - Transport Data</h2>

<p>
    Step 5 is adding the transportation data to the model. For a copied model, there is no transportation data; you will have to add that yourself. For models with many nodes (over 200), you should select the <b>Skip</b> option. Otherwise, select <b>Generate Transportation Routes</b>. This will generate every possible pathway for each product. Make sure to select all the data layers before saving. 
</p>

<img src="Pictures\Dashboard_tutorials\edit_model\step5.png">

<p>
    In this case, the model has less than 200 nodes, so we select <b>Generate Transportation Routes</b>. Selecting all the data layers indicates that we want to consider every possible pathway in the calculation. 
</p>

<p>
    The <b>Read Transportation Data</b> option is used when you have previously generated transportation routes and have saved them. This option is slightly faster than generating new transportation routes. 
</p>

<p>
    After generating transportation routes, you can now use the distance filter option. This allows you to limit the transportation pathways to those within a certain distance range. Clicking <b>Fit</b> will apply the selected distance filter, and clicking <b>Recover all Routes</b> will remove the distance filter. 
</p>

<img src="Pictures\Dashboard_tutorials\edit_model\step5_filter.png">

<br>
<br>

<a href="/ADAM_Documentation/dashboard_new_model.html">Next: Making your own model from scratch</a>