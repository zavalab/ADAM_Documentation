<h1>Interpreting the Results</h1>

<p>
    After the model has finished running, you can view the results. The results window consists of three sections: <b>Results Summary</b>, <b>Download Resutls</b>, and <b>Visualization</b>. In this tutorial, we will go over those three sections of the results and how to interpret them. 
</p>

<h2>Results Summary</h2>

<p>
    The <b>results summary</b> section gives a brief overview of the economic performance of the system; it consists of several categories: <b>total social welfare, total revenue, total supply cost, total transportation cost, total technology operational cost, total annualized investment cost</b>. The table below gives a brief description of each category and its meanings. 
</p>

| Result Category | Description |
| ------------- | ------------- | 
| Total Social Welfare | The net economic performance of the system; it can be calculated by summing up all the costs and subtracting them from the total revenue. A <b>positive</b> number indicates that the system is <b>profiting</b>, and a <b>negative</b> number indicates that the system is suffering a <b>loss</b>. |
| Total Revenue | The amount of money that the demand nodes spend to get a product. |
| Total Supply Cost | The money that the system pays the supplier for the supplier to provide the product. A <b>positive</b> number indicates that the system is losing money to the supplier. A <b>negative</b> number indicates that the system is gaining money from the supplier. |
| Total Transportation Cost | The money spent to transport the goods. |
| Total Technology Operational Cost | The money spent to operate the technology. |
| Total Annulized Investment Cost | The money spent to build the technology. |

<br>

<p>
    Now that we have reviewed the result summary categories, we can apply these definitions to interpret the Waste to Energy, Low Electricity price scenario results. 
</p>

<img src="Pictures\Dashboard_tutorials\run_model\results.png">

<p>
    The system has <b>social welfare of 505,756 million USD/year </b>which indicates that it is profiting in this scenario. The <b>revenue is zero</b> because the disposal node is not paying any money to obtain the waste product. The <b>supply cost is -975,000 million USD/year</b>. This means that the system is gaining 975,000 million USD/year from the suppliers. The <b>transportation costs are 405,201.90 million USD/year</b>. The <b>operating cost is $64,042 million/year</b>. The <b>investment cost is zero</b> because the technologies were already built. 
</p>

<p>
    The reason why ADAM categorizes the money from suppliers as a <b>negative cost</b> is due to traditional notation. In a traditional market, suppliers have to receive money before they supply a product (e.g. a dairy farmer needs to get paid in order to offer their milk to the market), but that is not true in a waste management system. Waste is an undesirable product so <b>suppliers will pay money to get rid of their waste</b>. This results in a negative supply cost since the <b>flow of money is reversed</b>. 
</p>

<h2>Download Results</h2> 

<p>
    You can also download the results in the form of CSV files. For each model, there may be different result CSV files depending on the model-type and the number of products that you have in your system. 
</p>

<p>
    The table below gives a brief overview of the different types of result files. 
</p>

| Result File | Description |
| ------------- | ------------- | 
| clearing_prices | The real prices of the products at each node. This file is only generated for <b>management-type models</b>. |
| demand_results | Contains information on the products and amount of product that is transported to each demand node. |
| flow_results | Shows the amount of product flowing from one node to another. In the <b>left column</b> are the nodes which are <b>supplying</b> the product. The <b>top row</b> is the nodes that are <b>receiving</b> the product. |
| installment_results | A list of the installed technologies and their locations. This file is only generated for <b>design-type models</b>. | 
| results_summary | A file containing the results summary of the model. |
| supply_results | A list of the supply nodes and how much product they are supplying to the system. |
| techsite_results | A list of the amount of product processed at each technology site. | 

<p>
    Now that you have been introduced to each of the file types, we will use the Waste to Energy, Low Electricity Price scenario to explain each file in more detail. For this example, you can download the result files 
<a href="https://github.com/ADAM-Development/ADAM_Documentation/tree/main/Downloadable_content/waste_to_energy_low_price_results">here</a>. 
</p>

<h3>Clearing Prices File</h3>

<p>
    The clearing prices file for the Waste to Energy case study is shown below. The <b>clearing price</b> is the <b>real price of the product at that node</b>. This is different from the supply and demand prices that we set in the model. When we defined the supply and demand prices, those were the <b>maximum prices that the supply and the demand nodes were willing to pay</b>. For example, a CAFO is willing to spend up to $5 to get rid of their waste; however, if a customer is willing to take that waste for $3, the CAFO will gladly get rid of their waste for less.
</p>

<p>
    Below are the clearing price file results for the Waste to Energy, Low Electricity Incentives case study example. 
</p>

<img src="Pictures\Dashboard_tutorials\results\clearing_prices.png">

<p>
    The column on the left indicates the node at which the transaction is taking place, the top row is the products being traded, and the numbers in the center are the prices at which the transactions are taking place. 
</p>

<p>
    You can interpret each of the prices in this way: <b>if [product] were to be traded at [node], then the transaction price would be [price]</b>. For example, the interpretation of the -5.45 price in cell B4 of the excel sheet would be the following: if p1 were to be traded at n3, then the transaction price would be -$5.45 per unit of p1. <b>A negative price indicates reverse money flow (i.e. the seller loses money, while the buyer gains money)</b>.
</p>

<p>
    You can also relate this interpretation to the type of node. For example, n1 is a supply node that is supplying product p1 at a price of -$3.32 per unit of p1. Additionally, if n1 also demanded p2, -$0.10 would be the price at which n1 would buy p2. If the node in question does not supply or demand the products listed, the prices would just represent the prices of the product if they were sold at that location. 
</p>

<h3>Demand Results File</h3>

<p>
    The demand results file contains information on the type of product and the amount of product that the demand node receives for the solved system.  
</p>

<img src="Pictures\Dashboard_tutorials\results\demand_results.png">

<p>
    In this example, we can see that demand node d3 (also denoted as node n6) receives 115,000 units of p1 in the optimal system. 
</p>

<h3>Flow Results File</h3>

<p>
    The results zip file may contain multiple flow results files depending on the number of products in your system. In the Waste to Energy case, there are three flow result files, one for each of the three products being transferred: cow manure (p1), bio-electricity (p2), and digestate (p3). 
</p>

<p>
    The flow results for p1 are shown below: 
</p>

<img src="Pictures\Dashboard_tutorials\results\flow_results.png" >

<p>
    The <b>left column</b> indicates the node that is <b>supplying</b> the product, and the <b>top row</b> indicates the node that is <b>receiving</b> the product. This flow results file is indicating that n1 is supplying 65,000 units of p1 to n6, n2 is supplying 35,000 units of p1 to n6, and n3 is supplying 15,000 units of p1 to n6. 
</p>

<h3>Installment Results File</h3>

<p>
    Since the installment results file is only generated for design-type models, the Waste to Energy example does not have an installment results file. Instead, we will show an example installment results file from another model. 
</p>

<img src="Pictures\Dashboard_tutorials\results\installment_results.png">

<p>
    In this example, nodes n1, n2, and n3 all have installed technology t1. The capacity indicates how much input material is being processed at that technology site. 
</p>

<h3>Results Summary File</h3>

<p>
    The results summary file contains an overview of the economic performance of the system. This is the same information displayed when you first click <b>View Results</b>. 
</p>

<p>
    An example of the Waste to Energy result summary is shown below. For the interpretation of this file, see the <b>Results Summary section</b> of this tutorial. 
</p>

<img src="Pictures\Dashboard_tutorials\results\results_summary.png">

<h3>Supply Results File</h3>

<p>
    The supply results file contains information on each supply node and the amount of product that they are supplying in an optimal system. 
</p>

<img src="Pictures\Dashboard_tutorials\results\supply_results.png">

<p>
    In the Waste to Energy example, supply node, s1, supplies 65,000 units of cow manure (p1) at a price of -$5 per unit. The negative price indicates reverse money flow (i.e. the supplier pays the customer). 
</p>

<h3>Technology Site Results File</h3>

<p>
    The technology site results file shows how much product is processed at each technology site in the optimal system. 
</p>

<p>
    In the waste to energy (low electricity price), there were no tech site results. The example below is from a different model. 
</p>

<img src="Pictures\Dashboard_tutorials\results\tech_site.png">

<p>
    These results indicate that the tech site, t1, processed 10,000 units of input material.
</p>

<h2 id="vis_model_results">Visualization Tool</h2>

<p>
    Clicking the button under the <b>Visualization</b> section will take you to the visualization tool where you will see an empty map along with two buttons labeled <b>Visualize Model Data</b> and <b>Visualize Model Results</b>.
</p>

<p>
     Selecting <b>Visualize Model Data</b> will display the nodes from the model onto the map.
</p>

<img src="Pictures\Dashboard_tutorials\results\vis_data.png">

<p>
    Selecting <b>Visualize Model Results</b> will display the transportation results. The grey nodes indicate nodes that do not participate in the system. You can toggle which transportation paths to view by checking and unchecking the data layers under transportation results. 
</p>

<img src="Pictures\Dashboard_tutorials\results\vis_results.png">

<p>
    You can also view the price gradients for each product. Red areas indicate high prices and blue areas indicate low prices. 
</p>

<img src="Pictures\Dashboard_tutorials\results\vis_price.png">

<br>
<br>

<a href="/ADAM_Documentation/dashboard.html">Return to Dashboard Tutorials</a>

