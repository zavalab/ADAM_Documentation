<h1>Interpreting the Results</h1>

<p>
    After the model has finished running, you can view the results. The results window consists of three sections: <b>Results Summary</b>, <b>Download Resutls</b>, and <b>Visualization</b>. 
</p>

<p>
    In this tutorial, we will go over the various sections of the results and how to interpret them. 
</p>

<h2>Results Summary</h2>

<p>
    The <b>results summary</b> section gives a brief overview on the economic performance of the system; it consists of several categories: <b>total social welfare, total revenue, total supply cost, total transportation cost, total technology operational cost, total annulized investment cost</b>. The table below gives a brief description of each category and their meanings. 
</p>

| Result Category | Description |
| ------------- | ------------- | 
| Total Social Welfare | The net economic performance of the system; it can be calculated by summing up all the costs and subtracting it from the total revenue. A <b>positive</b> number indicates that the system is <b>profiting</b>, and a <b>negative</b> number indicates that the system is suffering a <b>loss</b>. |
| Total Revenue | The amount of money that the demand nodes spend to get a product. |
| Total Supply Cost | The money that the system pays the supplier in order for the supplier to provide the product. A <b>positive</b> number indicates that the system is losing money to the supplier. A <b>negative</b> number indicates that the system is gaining money from the supplier. |
| Total Transportation Cost | The money spent to transport the goods. |
| Total Technology Operational Cost | The money spent to operate the technology. |
| Total Annulized Investment Cost | The money spent to build the technology. |

<br>

<p>
    Now that we have reviewed the result summary categories, we can apply these definitions to interpret this example results. 
</p>

<img src="Pictures\Dashboard_tutorials\run_model\results.png">

<p>
    The system has a social welfare of 505,756 million USD/year which indicates that it is profiting in this scenario. The revenue is zero because the disposal node is not paying any money to obtain the waste product. The supply cost is -975,000 million USD/year. This means that the system is gaining 975,000 million USD/year from the suppliers. The transportation costs are 405,201.90 million USD/year. the operating cost is $64,042 million USD/year. The investment cost is zero because the technologies were already built. 
</p>

<p>
    The reason why ADAM categorizes the money from suppliers as a negative cost rather than a positive revenue is because in a traditional market, suppliers have to receive money before they supply a product. For example, a dairy farmer needs to get paid in order to offer their milk to the market; however, in a waste management scenario, the opposite is true. Waste is an undesireable product so suppliers will pay the system in order to get rid of their waste. This results in a negative supply cost since the system is actually profiting from the supply of waste.
</p>

<h2>Download Results</h2> 

<p>
    You can also download the results in the form of csv files for more detailed information. For each model, there may be different result csv files depending on the model-type and the number of products that you have in your system.
</p>

| Result File | Description |
| ------------- | ------------- | 
| clearing_prices | |
| demand_results | |
| flow_results | |
| installment_results | | 
| results_summary | |
| supply_results | |
| techsite_results | | 



<img src="Pictures\Dashboard_tutorials\run_model\results_download.png">

<p>
    For more information on each of the result files and the data they contain, please refer to the 
<a href="/ADAM_Documentation/dashboard_result_files.html">Result Files Tutorial</a>.
</p>

<h2>Visualization Tool</h2>

<p>
    Going to the visualization tool allow you to see the product pathways of the system. 
</p>