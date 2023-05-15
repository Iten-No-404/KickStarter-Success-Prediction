# KickStarter-Success-Prediction
This project is all about predicting whether a start-up project will succeed before it’s released based on data collected on it from the KickStarter website and basic information about the project like the project name, country of origin, category, etc... This project is a fulfilment to the CMP4011 BD project.
##  Brief Problem Description:
The idea briefly is predicting whether a startup project will succeed before it’s released based on data collected on it from the KickStarter website and basic information about the project like the project name, country of origin and category. It also contains more important data such as the number of backers, the goal, and the amount of money pledged.
## Project Pipeline
  <p align="center">
      <img src="https://github.com/Iten-No-404/KickStarter-Success-Prediction/blob/main/images/pipeline.PNG"  class="center"></img>
 </p>
  
### Data preprocessing :
*  Removing the columns usd_pledged_real and usd_goal_real as they provided no useful information. 
*  Dropping rows containing null values in the columns name, category, and country as there was no practical way to impute or predict the missing values.
*   The usd_pledged column as it was the only column left with nulls, we replaced all null values in that column with 0. 
*   The country column. There were invalid entries in this column like ‘N, 0””’, ‘0’, ‘failed’. 
### Data visualization/exploration :
* <div> <p align ="left"> We began our EDA phase by inspecting our target variable,<br> whether a kickstarter campaign succeeded or failed.<br>
  We can see from the pie chart that about 60% of all campaigns failed.<br> So we already have a slight imbalance in our data.

  </p>
  <p align="center" >
      <img src="https://github.com/Iten-No-404/KickStarter-Success-Prediction/blob/main/images/piechart.PNG" ></img>
  </p>
  </div>
* we can clearly see that the top 3 categories are “Film & Video”, “Music”, and “Publishing”, followed closely by “Games”, “Technology”,  and “Design”.

   <p align="center">
      <img src="https://github.com/Iten-No-404/KickStarter-Success-Prediction/blob/main/images/topcategories.PNG"></img>
  </p>
 * Looking at successful and failed campaigns, we can see that the numbers follow about the same distribution as all categories, with some categories swapping places.
 * Looking at average USD amount pledged for successful and failed campaigns. Technology seems to consistently be one of the highest pledged categories despite not being in the top 3 categories in the previous section
   <p align="center">
      <img src="https://github.com/Iten-No-404/KickStarter-Success-Prediction/blob/main/images/usd%26categories.PNG"></img>
    </p>
 *  We can see something very clear with a cursory look: Successful campaigns are quite humble. This is apparent through the goal of each category. e can see that the scale isn’t all that different. Failed campaigns for some categories seem to have more backers than their successful counterparts
  <p float="left">
  <img src="https://github.com/Iten-No-404/KickStarter-Success-Prediction/blob/main/images/goal.PNG" width="500" />
  <img src="https://github.com/Iten-No-404/KickStarter-Success-Prediction/blob/main/images/backers.PNG" width="500" /> 
</p>
 Look at how goals and pledged amounts behave for successful campaigns. We can clearly see the humbleness of goals in action again. While the pledged amount seems to have a wild variation with a few extreme outliers.
<p align="center">
<img src="https://github.com/Iten-No-404/KickStarter-Success-Prediction/blob/main/images/boxplot.PNG">
</img>
</p>

### Model & Classifier training:
* Linear SVM
* Logistic Regression
* Random Forest
* Decision Tree 
* Naive Bayes using Map-Reducer Spark	
### Results 
| Model | Accuracy on Validation Set |
| --- | --- |
| Logistic Regression | 76.81% |
| Linear SVM | 73.6% |
| Naive Bayes | 78.5% |
| Random Forest | 84.9% |
| Decision Tree | 85.5% |
### Best Results 
* Decision Tree classifier on test set: 84.12%
## Collaborators
<!-- readme: collaborators -start -->
<table>
<tr>
    <td align="center">
        <a href="https://github.com/Hero2323">
            <img src="https://avatars.githubusercontent.com/u/58619697?v=4" width="100;" alt="Abdelrahman Jamal"/>
            <br />
            <sub><b>Abdelrahman Jamal</b></sub>
        </a>
    </td>
    <td align="center">
        <a href="https://github.com/Iten-No-404">
            <img src="https://avatars.githubusercontent.com/u/56697800?v=4" width="100;" alt="Iten-No-404"/>
            <br />
            <sub><b>Iten Elhak</b></sub>
        </a>
    </td>
    <td align="center">
        <a href="https://github.com/radwaahmed2132000">
            <img src="https://avatars.githubusercontent.com/u/56734728?v=4" width="100;" alt="radwaahmed2132000"/>
            <br />
            <sub><b>Radwa Ahmed</b></sub>
        </a>
    </td>
    <td align="center">
        <a href="https://github.com/KnockerPulsar">
            <img src="https://avatars.githubusercontent.com/u/12754772?v=4" width="100;" alt="Tarek Yasser"/>
            <br />
            <sub><b>Tarek Yasser</b></sub>
        </a>
    </td></tr>
</table>
<!-- readme: collaborators -end -->

