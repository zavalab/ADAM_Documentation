<h1>Making a New Model from Scratch</h1>

<p>
    After understanding all of the files needed to make a model in ADAM, lets now go over how to use those files to create a new model.  
</p>

<h2>Creating a new Model</h2>

<p>
    First, navigate to your model list by selecting <b>Manage Models</b> on the dashboard homepage. Next select <b>New Model</b>. 
</p>

<img src="Pictures\Dashboard_tutorials\new_model\model_list.png">

<p>
    You will be prompted to enter the model name and description. The description of the model should provide a brief overview on the purpose of the model or what problem it is attempting to solve. 
</p>

<img src="Pictures\Dashboard_tutorials\new_model\enter_info.png">

<p>
    After selecting <b>Yes</b>, the model will be added to your model list.
</p>

<img src="Pictures\Dashboard_tutorials\new_model\new_model.png">

<h2>Entering information in the Model</h2>

<p>
    Clicking on the model will bring you into a progress bar screen with a row of buttons labeled from step 1 through 6 and another row of buttons with various options. 
</p>

<img src="Pictures\Dashboard_tutorials\new_model\progress_bar.png">

<p>
    The first row of buttons is where you will go to enter information about the model. The second row of buttons gives you options for what you can do with the model. It is best to use these options once the model data is complete. 
</p>

<h2>Step 1 - Model Type</h2>

<p>
    Begin inputing data by selecting <b>Step 1</b>. You will be taken to a page where you can define the model type and the time basis. 
</p>

<img src="Pictures\Dashboard_tutorials\new_model\step1.png">

<p>
    The default model type is a <b>Supply Chain Design</b> type model, and the default time basis is <b>Year</b>. A design type model is used when your data contains technology candidates, and you would like to determine whether to build a technology or not.
</p>

<p>
    The time basis is up to you. Just keep in mind that you will need to have your data in terms of that time basis; additionally, the results will be in the selected time units.
</p>

<p>
    In this example, we will leave it as the default settings. Clicking <b>Confirm</b> will bring you to the next step.
</p>

<h2>Step 2 - Suppy Data</h2>

<p>
    Step 2 is where you can add supply data to the model. Use the first three options to upload data. For a review on how each option works, please refer to the 
<a href="/ADAM_Documentation/dashboard_input_data.md">Adding Data to a Model Tutorial</a>.
</p>

<img src="Pictures\Dashboard_tutorials\new_model\step2.png">

<p>
    For this example, we will be using the files located at 
<a href="https://github.com/mshen42/ADAM_Documentation/tree/main/Downloadable_content/Example">this link</a>. After uploading the example supply file, the model should look like this: 
</p>

<img src="Pictures\Dashboard_tutorials\new_model\step2_data.png">

<p>
    Then click <b>Next</b> to save the supply data and proceed to the next step. 
</p>

<h2>Step 3 - Technology Data</h2>

<p>
    In step 3, we will upload our technology data using the same method as before. When uploading the technology data, make sure to toggle the <b>Type</b> to match the file. 
</p>

<img src="Pictures\Dashboard_tutorials\new_model\step3_type.png">

<p>
    ADAM only allows you to upload one file at a time so first select <b>Technology Site Data</b> as the type and upload the example technology site file, then select <b>Upload Data</b> again and repeat the process with the technology candidate file. 
</p>

<p>
    If you uploaded the example files correctly, the model should look like this: 
</p>

<img src="Pictures\Dashboard_tutorials\new_model\step3.png">

<p>
    Then, click <b>Next</b> in order to save the technology data and proceed to the next step. 
</p>

<h2>Step 4 - Demand Data</h2>

<p>
    Similar to the supply and technology data, we will upload a csv file containing the demand data in step 4. After uploading the example, the model should look like this:
</p>

<img src="Pictures\Dashboard_tutorials\new_model\step4.png">

<p>
    Then click <b>Next</b> to save the demand data and proceeed to the next step. 
</p>

<h2>Step 5 - Transport Data</h2>

<p>
    Step 5 is adding the transportation data to the model. For models with many nodes (over 200), you should select the <b>Skip</b> option. Otherwise, select <b>Generate Transportation Routes</b>. This will generate every possible pathway for each product. Make sure to select all the data layers before saving. 
</p>

<p>
    The digestate pathways overlap the bio-electricity pathways so in order to view the bio-electricity pathways, you may have to toggle some of the data layers. 
</p>

<img src="Pictures\Dashboard_tutorials\new_model\step5.png">

<p>
    The <b>Read Transportation Data</b> option is used when you have previously generated transportation routes and have saved them. This option is slightly faster than generating new transportation routes. 
</p>

<p>
    After generating transportation routes, you can now use the distance filter option. This allows you to limit the tranportation pathways to those within a certian distance range. Clicking <b>Fit</b> will apply the selected distance filter, and clicking <b>Recover all Routes</b> will remove the distance filter. 
</p>

<img src="Pictures\Dashboard_tutorials\new_model\dist_filter.png">

<p>
    After applying the transportation routes, click <b>Save Changes</b> in order to save. 
</p>

<h2>Step 6 - Run Model</h2> 

<p>
    Now that all of the input data is uploaded, the model is now complete. The final step is running the model. 
</p>

<img src="Pictures\Dashboard_tutorials\new_model\step6.png">

<p>
    Once the status is <b>Completed</b>, you may view the results. For more information on how to interpert the results, please refer to the
<a href="/ADAM_Documentation/dashboard_results.html">Interpreting the Results Tutorial</a>.
</p>

<img src="Pictures\Dashboard_tutorials\new_model\completed.png">

<h2>The Other Options</h2>

<p>
    Besides the <b>View Model Results</b> option, there are also several other options that you can select. Below, there is a short description of the option and their functions. 
</p>

<ul>
    <li><b>Clear Model Data</b> - clears all data in the model</li>
    <li><b>Delete Model</b> - deletes the model from the model list</li>
    <li><b>Load Model</b> - loads data from another model into this model</li>
    <li><b>Download Model Data</b> - allows you to download all of the input data (supply, technology, demand) in the form of csv files</li>
    <li><b>Get P-Graph</b> - allows you to view the process graph for this system</li>
</ul>
