## Modelling and Predicting Annual Precipitation for Climate Change Analysis in Pakistan
Climate change is supercharging the evaporation process in the water cycle. It has affected the intensity and frequency of precipitation as warmer oceans increase the amount of water that evaporates into the air. Pakistan is home to over 7,200 glaciers, more than anywhere outside the poles. Rising temperatures, linked to climate change, are likely making many of them melt faster and earlier, adding water to rivers and streams that are already swollen by rainfall. The onset of heavy rain has the effect of flash flooding as water levels are risen. 
This tutorial will walk you through an analysis of annual precipitation over the years. The modelled behavior is indicative of the impact of climate change in Pakistan. Using Azure ML a simple yet concise  model has been derived.

Let’s walk you through the procedure:
1.	Log in to https://studio.azureml.net/ and on the dashboard click the + new button to create a new (blank) project.

2.	Upload your dataset containing the annual precipitation data via datasets and + new and add it to your project.
 ![image](https://user-images.githubusercontent.com/40885002/209472561-a93fd2cc-727b-4eca-a6f0-28e464b2a334.png)

3.	Now head over to the Experiments section right above Datasets and Web services. Drag and drop tabs into this workspace to create a mini map as shown:
  ![image](https://user-images.githubusercontent.com/40885002/209472570-40fa1679-6b4c-4a45-9dc8-e741004b3e06.png)

4.	Right Click on the dataset tab and click visualize. This data depicts data for factors affecting climate change in Pakistan including rainfall in the last column for 56 years from 1960 to 2016. You can analyse the year and corresponding mean annual rainfall. You can see as follows
  ![image](https://user-images.githubusercontent.com/40885002/209472576-19f662a6-42ec-44d9-9db9-add13526d633.png)
 
5.	Now click on ‘Select Columns in Dataset’ tab and Launch Column Selector to choose the columns from the dataset that the model will be trained on. These will be Year and Rainfall. The rest are filtered out for now. 
  ![image](https://user-images.githubusercontent.com/40885002/209472581-90cb6998-aab5-419f-9b87-7d0115f31d5b.png)

  ![image](https://user-images.githubusercontent.com/40885002/209472583-7ad4ec6f-6a27-4ead-a588-041df8479125.png)
  
6.	We would like to split our data reserving 65% for the training set and 35% for the test set by clicking on the ‘Split Data’ tab.
  ![image](https://user-images.githubusercontent.com/40885002/209472596-7613f4cb-144d-494c-89fa-c6ae22399701.png)

7.	The algorithm that we have used to train the model is Boosted Decision Tree Regression. You may experiment with different algorithms.
8.	Now click on the ‘Train Model’ tab to select the column that we would like ot get prediction on. This will be the Rainfall Mean() column. 
 ![image](https://user-images.githubusercontent.com/40885002/209472599-a6c37487-0096-4242-84e8-487384e2e108.png)
 
9.	Click on the ‘Score task’ tab to visualize the model. The Scored Labels column shows the predicted annual rainfall whereas the Rainfall Mean() column shows the actual rainfall.
 ![image](https://user-images.githubusercontent.com/40885002/209472604-ce5ede1b-b3f6-4c5e-a532-fd5d34d04ba6.png)

10.	Finally, we evaluate our model. The coefficient of determination tells us our model accuracy. Currently it is shown to be ~50%.
 ![image](https://user-images.githubusercontent.com/40885002/209472612-05015b4b-ca0d-4bd6-b6b9-4f204e5b70ad.png)

11.	Now click on set up as web service below followed by deploy web service in the prompt and remove the RainFall Mean() column from input dataset task.
 ![image](https://user-images.githubusercontent.com/40885002/209472617-e014d547-b40e-4a9f-b62f-d95d9e1b58da.png)
![image](https://user-images.githubusercontent.com/40885002/209472621-19533a10-edb4-4ab4-b41b-c10eed8b32c9.png)

12.	On successful deployment click on test button. You will be prompted to enter a year for predicting the rainfall. 

Kudos, you made it! :star2:





