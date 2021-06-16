<h2>Running the Model Without Making Any Changes</h2>

<p>
    After making a copy of the case study, you can run the model to see more detailed results. In this tutorial, we will go over how to run the model after copying it from a case study. 
</p>

<h2>1) Generate Transportation Routes</h2>

<p>
    Clicking on the case study in your model list will take you to an overview of the model. 
</p>

<img src="Pictures\Dashboard_tutorials\run_model\copied_model.png">

<p>
    The steps in the progress bar are as follows: (1) Define model type, (2) Add supply data, (3) Add technology data, (4) Add demand data, (5) Add transportation data, (6) Run model. For more information about each step, please refer to the tutorial. 
</p>

<p>
    Notice that the model status is <b>Data Required</b>. That is because only steps 1 - 4 are completed for a copied model. You may click through the completed steps to view the model data, but in order to run the model, you must complete step 5. Do this by selecting <b>Generate Transportation Routes</b>. The other options will be explained in the next tutorial.
</p>

<img src="Pictures\Dashboard_tutorials\run_model\step5.png">

<br> 

<p>
    Make sure that you select all the transportation routes in the data layers before saving. 
</p>

<img src="Pictures\Dashboard_tutorials\run_model\transport_routes.png">

<h2>2) Run the Model</h2>

<p>
    After this, you can go to step 6 and run the model.
</p>

<img src="Pictures\Dashboard_tutorials\run_model\run.png">

<br>

<p>
    Once the status changes from <b>Running</b> to <b>Completed</b> you can view the model results. 
</p>

<img src="Pictures\Dashboard_tutorials\run_model\running.png">

<img src="Pictures\Dashboard_tutorials\run_model\progress_bar.png">

<h2>3) View Results</h2>

<p>
    The results will show a summary of the economic performance of the system, along with a section for downloading the results (in the form of csv files), and a link to the visualization tool. Note that the system includes the supply, demand, technology, and transportation data. 
</p>

<h3>Results Summary</h3>

<p>
    The <b>results summary</b> has several categories: <b>total social welfare, total revenue, total supply cost, total transportation cost, total technology operational cost, total annulized investment cost</b>. 
</p>

<img src="Pictures\Dashboard_tutorials\run_model\results.png">

<p>
    The <b>total social welfare is the net economic performance of the system</b>. It can be calculated by summing up all the costs and subtracting it from the total revenue. A positive number indicates that the system is profiting, and a negative number indicates that the system is suffering a loss. In this case, the system has a social welfare of +505,756 million USD/year which indicates that it is profiting in this scenario. 
</p>

<p>
    The <b>total revenue is the amount of money that the demand nodes give to the system to get a product</b>. In this case, it is zero because the disposal node is not paying any money to obtain the waste product. 
</p>

<p>
    The <b>total supply cost is the money that the system pays the supplier in order for the supplier to provide the product</b>. For example, a dairy farmer needs to get paid in order to offer their milk to the market. In a waste management scenario, the opposite is true. Waste is an undesireable product so suppliers will pay the system in order to get rid of their waste. This results in a negative supply cost since the system is actually profiting from the supply of waste. In this case, the supply cost is -975,000 million USD/year. This means that the system is gaining 975,000 million USD/year from the suppliers.
</p>

<p>
    The <b>total transportation cost is the money spent to transport the goods</b>. In this case, the transportation costs are 405,201.90 million USD/year. 
</p>

<p>
    The <b>total operational cost is the money spent to operate the technology</b>. In this case, the operating cost is $64,042 million USD/year. 
</p>

<p>
    The <b>investment cost is the money spent to build the technology</b>. In this case it is zero because the technologies were already built. 
</p>

<h3>Download Results</h3> 

<p>
    You can also download the results in the form of csv files for more detailed information. There may be a different number of csv files depending on the number of products that you have in your system; however, all models will have a clearing_prices.csv, demand_results.csv, results_summary.csv, supply_results.csv, techsite_results.csv.
</p>

<img src="Pictures\Dashboard_tutorials\run_model\results_download.png">

<p>
    For more information on each of the result files and the data they contain, please refer to the 
<a href="/ADAM_Documentation/dashboard_result_files.html">Result Files Tutorial</a>.
</p>

<h3>Visualization Tool</h3>

<p>
    Going to the visualization tool allow you to see the product pathways of the system. 
</p>

<br>
<br>

<a href="/ADAM_Documentation/dashboard_edit_model.html">Next: Editing the Model</a>