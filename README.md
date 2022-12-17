<h1 id="space-titanic-competition" align="center">🚀 Space Titanic Competition 🚀</h1>

<p align="center">Predict which passengers are transported to an alternate dimension</p>

<br>
    
**Competition: [Spaceship Titanic](https://www.kaggle.com/competitions/spaceship-titanic)**

----

<h1 id="problem-description">📝 Problem Description</h1>

<p>Welcome to the year 2912, where your data science skills are needed to solve a cosmic mystery. We've received a transmission from four lightyears away and things aren't looking good.</p>

<p>The Spaceship Titanic was an interstellar passenger liner launched a month ago. With almost 13,000 passengers on board, the vessel set out on its maiden voyage transporting emigrants from our solar system to three newly habitable exoplanets orbiting nearby stars.</p>

<p>While rounding Alpha Centauri en route to its first destination—the torrid 55 Cancri E—the unwary Spaceship Titanic collided with a spacetime anomaly hidden within a dust cloud. Sadly, it met a similar fate as its namesake from 1000 years before. Though the ship stayed intact, almost half of the passengers were transported to an alternate dimension!</p>

<center>
    <img 
         src="https://storage.googleapis.com/kaggle-media/competitions/Spaceship%20Titanic/joel-filipe-QwoNAhbmLLo-unsplash.jpg" 
         width="auto"
         height="auto"
    />
</center>

<br />
<br />

<b>To help rescue crews and retrieve the lost passengers, you are challenged to predict which passengers were transported by the anomaly using records recovered from the spaceship’s damaged computer system. Help save them and change history!</b>

----

<h1 id="files-descriptions">📁 Files Descriptions</h1>

<br/>

> **train.csv** - personal records for about two-thirds (~8700) of the passengers, to be used as training data;

> **test.csv** - personal records for the remaining one-third (~4300) of the passengers, to be used as test data. The task is to predict the value of Transported for the passengers in this set;

> **sample_submission.csv** - a submission file in the correct format.

----

<h1 id="variables">❓ Variables</h1>

<br/>

> **PassengerId** - A unique Id for each passenger. Each Id takes the form gggg_pp where gggg indicates a group the passenger is travelling with and pp is their number within the group. People in a group are often family members, but not always;

> **HomePlanet** - The planet the passenger departed from, typically their planet of permanent residence;

> **CryoSleep** - Indicates whether the passenger elected to be put into suspended animation for the duration of the voyage. Passengers in cryosleep are confined to their cabins;

> **Cabin** - The cabin number where the passenger is staying. Takes the form deck/num/side, where side can be either P for Port or S for Starboard;

> **Destination** - The planet the passenger will be debarking to;

> **Age** - The age of the passenger;

> **VIP** - Whether the passenger has paid for special VIP service during the voyage.
RoomService, FoodCourt, ShoppingMall, Spa, VRDeck - Amount the passenger has billed at each of the Spaceship Titanic's many luxury amenities;

> **Name** - The first and last names of the passenger;

> **RoomService, FoodCourt, ShoppingMall, Spa, VRDeck** - Amount the passenger has billed at each of the Spaceship Titanic's many luxury amenities.

> **🌟 Transported 🌟** - Whether the passenger was transported to another dimension. This is the target, the column you are trying to predict.

----

<h1 id="target">🌟 Target</h1>

<br/>

> **Transported** - Whether the passenger was transported to another dimension. This is the target, the column you are trying to predict.

> This feature can have two possible values: `true` (the passenger has been transported to another dimension 😢) and `false` (the passenger has not been transported to another dimension 😌). For instance:

<br />

<table>
    <tr>
        <th>Transported</th>
        <th>Meaning</th>
    </tr>
    <tr>
        <td>True</td>
        <td>Passenger Transported to Another Dimension</td>
    </tr>
    <tr>
        <td>False</td>
        <td>Passenger Not Transported to Another Dimension</td>
    </tr>
</table>

----

<h1 id="metric">📏 Metric</h1>

<br/>

This competition applies `Classification Accuracy` as the main metric to evaluate the results.

As far as the passengers have two possible outcomes to have been transported to another dimension, being `true` and `false`, this competition is a `Binary Classification Problem`.

In Binary Classification Problems, our models can have four predictions:

<br />

> **True Positive (TP)** - the model predicted `true`, and the real outcome is `true`; ✔️

> **True Negative (TN)** - the model predicted `false`, and the real outcome is `false`; ✔️

> **False Positive (FP)** - the model predicted `true`, and the real outcome is `false`; ❌

> **False Negative (FN)** - the model predicted `false`, and the real outcome is `true`; ❌

<br />

With this in mind, Classification Accuracy is calculated adding the True Positives and True Negatives, anbd dividing the result by the sum between True Positives, True Negatives, False Positives and False Negatives. Which means: 

$(TP + TN) / (TP + TN + FP + FN)$

So, consider that the real dataset has `150 True outcomes` and `150 False outcomes` and that my model has predicted `100 True Positives`, `100 True Negatives`, `50 False Positives` and `50 False Negatives`, the model's accuracy will be:

$(TP + TN) / (TP + TN + FP + FN)$

$(100 + 100) / (100 + 100 + 50 + 50)$

$200 / 300 == 2 / 3 =~ 0.67 == 67$%

----

<h1 id="limitations">🛑 Limitations</h1>

<br/>

Well, at least up to December 2022, humanity has not make up a Spaceship to transport people around the universe neither the Applied Physics has proved been possible to go through another dimentions, so the entire dataset is composed by fake datas.

With all of this in mind, we can assume that the model may not be accurated in the real life when it's needed!!

----

<h1 id="goals">🎯 Goals</h1>

<br/>

> **Goal 1** - create XGBoost Classifier Model;

> **Goal 2** - create a Deep Learning Model;

> **Goal 3** - get an accuracy greather than or equal 75%;

----

<h1 id="setup">⚙️ Setup</h1>

<br/>

**Tools**

> Python Version 3.7+;

> Jupyter;

> Jupyter Notebook.

<br />

**Packages**

> Numpy;

> Matplotlib;

> Seaborn;

> Pandas;

> PyOD;

> Scikit Learn;

> XGBoost;

> TensorFlow;

> Shap;

> Pdpbox;

> Pickle.

----

<h1 id="aknowledges">🎉 Aknowledges</h1>

<br/>

> Photos by [Joel Filipe](https://unsplash.com/@joelfilip?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText), [Richard Gatley](https://unsplash.com/@uncle_rickie?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) and [ActionVance](https://unsplash.com/@actionvance?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on Unsplash.

<br />

----

<br/>
<h1>📫 Reach Me 📫</h1>
<br/>

> **Email:** **[csfelix08@gmail.com](mailto:csfelix08@gmail.com?)**

> **Linkedin:** **[linkedin.com/in/csfelix/](https://www.linkedin.com/in/csfelix/)**

> **Instagram:** **[instagram.com/c0deplus/](https://www.instagram.com/c0deplus/)**

> **Portfolio:** **[CSFelix.io](https://csfelix.github.io/)**

> **Kaggle:** **[DSFelix](https://www.kaggle.com/dsfelix)**

> **Kaggle Kernel:** **[Spaceship Titanic](https://www.kaggle.com/code/dsfelix/spaceship-titanic-competition)**
