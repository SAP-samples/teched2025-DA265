# Exercise 4 - Enhance the user experience

 

We have utilized existing models with minimal effort to Just Ask. However, there are opportunities to enhance the user experience to enable key insights with a small amount of additional effort.
  
Firstly, let’s explore some possible areas for improvement.

Step 1: Open Just Ask.

![Image](img/5050.jpg)
  

<BR>
<BR>

Step 2:
  
1. Click on the **+** icon.
2. Notice there is no country shown, even though we know from earlier that countries are in the data model. Click **State**.

![Image](img/ex3_img1.png)

<BR>
<BR>

Step 3: Observe that, for example, *USA* is listed as a state, when it’s really a country. Technically, it’s part of the 'state' dimension.

![Image](img/ex3_img2.png)

<BR>
<BR>

Step 4: 
  
1. Type `Country profit`, as this is a reasonable question.
2. Press **enter**, or click **search**
3. No action, just observe that *State* has been used instead of *Country*. But at least ‘Country’ was identified!
4. Sales were added, but you asked for Profit, which is the difference between Sales and Expenses, i.e. it’s a calculation. (=Sales – Expense)
  
Your users may also refer to units by their unit of measure 'PC' or 'PCs'. It means you can’t ask for '*country PCs*' when you mean '*country units*', for example. 

![Image](img/ex3_img3.png)
  

<BR>
<BR>

Step 5:
  
Your business refers to '*Grocery*' as '*Mid-Size Grocery*' and '*Small Grocery*'.
However, when you ask for *Grocery Sales* both these values are not selected, instead, you must manually select the missing one.

Try it:
  
1.	Type `Grocery Sales`
2.	Press **enter**, or click **search**
3.	Open the **Store** filter
4.	Select the missing **Grocery** value, so that both 'Mid-Size' and 'Small' are selected.

![Image](img/ex3_img4.png)
  

As a Just Ask administrator, we shall make several improvements to resolve the issues mentioned above.
  
It is important to work with your users to understand the questions they may or might want to ask to enable the greatest adoption. You can then make some simple improvements that can increase their adoption.
  
Firstly, we shall take a copy of the existing model and make changes to this copied model.

<BR>
<BR>

Step 6:
You *may* need to exit 'Just Ask', then
  1. Select **Home**
  2. Select **Catalog**, if it is not already selected
  3. Open the tile **Just Ask Sales master start model folder**

![Image](img/ex3_img5.png)

<BR>
<BR>

Step 7: 
  A folder containing the model used so far is shown.
  1. Select the model **Just Ask Sales master start model**
  2. Select **Copy To**

![Image](img/ex3_img6.png)

<BR>
<BR>

Step 8: 
  Select the folder **Just Ask Workshop**, so its subfolders are shown.

![Image](img/ex3_img7.png)

<BR>
<BR>

Step 9: 
  Select the folder corresponding to your user number, '**Just Ask 0${number}**'

![Image](img/ex3_img8.png)

<BR>
<BR>

Step 10:
  
1. Change the name of the model so it can easily be identified and different from the existing and include your user number. Use the name `Just Ask Sales 0${number}`
2. Change the description to also include your user number. Use the description `Just Ask workshop 0${number}`
3. Select **Copy**

![Image](img/ex3_img9.png)

<BR>
<BR>

Step 11:
  
Now we need to open that copied model.
  
We need to navigate to the folder you just saved that model to.
  
Select the parent folder **Just Ask Workshop**

![Image](img/ex3_img10.png)

<BR>
<BR>

Step 12:
  
Select the subfolder corresponding to your user number: *Just Ask 0${number}*

![Image](img/ex3_img12.png)

<BR>
<BR>

Step 13: 
  
Open the model you recently copied '***Just Ask Sales 0${number}***’

![Image](img/ex3_img11.png)

<BR>
<BR>

## Enhance the 'State' dimension so Just Ask knows about the Country
  
  
We will improve the ‘State’ dimension in our duplicated model, allowing Just Ask to display ‘Country’ as a selectable option under the ‘+’ icon. This change will help users understand that ‘Country’ is the parent of ‘State’ and will enable queries such as ‘Country sales.’


We will add a new property for each State, indicating the Country it belongs to. Since each State is already part of a Country hierarchy, we can easily copy the existing values into this new property.

<BR>
<BR>

Step 14: 
  **Edit** the State Dimension Table

![Image](img/ex3_img13.png)

<BR>
<BR>

Step 15: 
  **No action**.
1. Observe that Country is a parent hierarchy of State.
2. Scroll down and select *Create Property*. 

![Image](img/ex3_img14.png)

<BR>
<BR>

Step 16: 
  
1. For the ID, enter `Country_`
2. For the description enter `Country`
3. Press **Create**
We must use a different ID from the existing so adding an underscore _ makes the property different enough.

![Image](img/ex3_img15.png)

<BR>
<BR>

Step 17: 
  
1. Switch the display to **grid mode**.
2. Select all the values and press **CTRL-C** (to copy the values)

![Image](img/ex3_img16.png)

<BR>
<BR>

Step 18:
  
1. In the new property, press **CTRL+V** (to paste the values)
2. Press **Back**

![Image](img/ex3_img17.png)

<BR>
<BR>

## Create a new measure calculation for Profit

Just Ask can't create new calculations on the fly, but it can use existing ones in the model. Profit has been identified as something an information consumer would like to use in natural language questions. So, we shall define profit as a measure of '*Sales – Expense*' for Just Ask to use.  

<BR>
<BR>

Step 19:
  
Select **Calculations** or press **Switch to Calculation Management**

![Image](img/ex3_img18.png)

<BR>
<BR>

Step 20: 
  Click **Add Calculated Measure**

![Image](img/ex3_img19.png)

<BR>
<BR>

Step 21: 
  
1. For the Name, enter `Profit`
2. For the Description, enter `Profit`
3. In the calculations enter the 3 characters `[sa`
4. A pop-up box will appear and select **\[Sales\]**

![Image](img/ex3_img20.png)

<BR>
<BR>

Step 22:
  
1. Once, \[Sales\] has been selected as shown, type the 4 characters `-[ex`
2. A pop-up box will appear and select **\[Expense\]**

![Image](img/ex3_img21.png)

<BR>
<BR>

Step 23: 
  **No action**
  
Validate the formula is valid and no errors are shown. If errors are shown, delete and repeat the above.

![Image](img/ex3_img22.png)

<BR>
<BR>

Step 24: 
  
1. **Scroll down** within this new calculation
2. Change the Unit Type to **Currency**

![Image](img/ex3_img23.png)

<BR>
<BR>

Step 25: 
  Click **Save**

![Image](img/ex3_img24.png)
  

You have now completed all the changes at the model level. They were:
  
- Adding a new property to ‘State’ for ‘Country’. This will allow the ‘+’ button to show Country as a hierarchy of State’. It will also allow for questions like ‘Country Sales’.
- Adding a new measure calculation ‘Profit’.

<BR>
<BR>

## Just Ask Model Administration

Some administration tasks are needed to improve the ease of use for Just Ask consumers. These tasks include:
  
- Indexing the model.
- Adding *synonyms* to measure names and dimension member values. 
- Setting a default *measure*.
- Creating a few *rules*.
- Other minor administration tasks.

  
### Indexing the model
  
We need to index the model so that Just Ask can learn about its metadata and so that users can consume it without necessarily knowing it exists.

<BR>
<BR>

Step 26: Open **Just Ask**.

![Image](img/ex1_img4.png)

<BR>
<BR>

Step 27: 
  As a user with Just Ask 'Administration' rights you have access to the 'Manage Models' interface.
  
Select **Manage Models**.

![Image](img/ex3_img25.png)

<BR>
<BR>

Step 28: On the *All Models* page, your copied model will not be shown because it’s not yet indexed.
  
Click **Add Model** so Just Ask can index your copied model.

![Image](img/ex3_img26.png)

<BR>
<BR>
  
Step 29:

1. Change the filter
2. And select **Owned by me**
3. In the search box enter `just ask`
4. Your model will then appear to select. Select your **model** to start the indexing process.

![Image](img/ex3_img27.png)

<BR>
<BR>

Step 30: 
  **No action.**

Observe the model is indexed. It won't take very long for our model, but it could take a little while for a very large model.
  
In a workshop environment, it may also take longer than expected, so you may need to be patient and re-try.


![Image](img/ex3_img28.png)
  

Congratulations!!! You’ve now indexed the model. It's very easy.

<BR>
<BR>


### Add synonyms

Although we created a measure called 'profit', our users could ask for something like 'profitable states'. And whilst Just Ask can interpret many phases, it can’t identify 'profitable' as something that should involve 'profit'.

<BR>
<BR>

Step 31: 
  
Click the word **profit** under Synonyms for the measure 'Profit'.

![Image](img/ex3_img29.png)

<BR>
<BR>

Step 32: 
  
1. Enter the word `profitable`
2. Click **Add**
3. Click **Save**

![Image](img/ex3_img30.png)
  

Although Just Ask can identify 'Units' as meaning 'Unit', it cannot recognize that users might use this unit of measure as the business term for the unit.  

<BR>
<BR>


Step 33: Click the word **unit** under Synonyms for the measure 'Unit'.

![Image](img/ex3_img31.png)

<BR>
<BR>

Step 34: 
  
1. Enter `PC`
2. Click **Add**
3. Enter `PCs`
4. Click **Add**
5. Click **Save**

Screenshot taken between steps 3 and 4

![Image](img/ex3_img32.png)

<BR>
<BR>


Step 35: No action.
  
Validate that the synonyms added are correct.

![Image](img/ex3_img33.png)
  

Our business users, you may recall, would like to ‘grocery’ to refer to both ‘mid-size’ and ‘small’ groceries and they would like to avoid the need to repeatedly correct the filter that Just Ask creates for them.

<BR>
<BR>

Step 36: 
  Click on **View** under 'View members' to open the dimension value list.

![Image](img/ex3_img34.png)

<BR>
<BR>

Step 37: 
  Click on the edit synonyms for 'Mid-Size Grocery'

![Image](img/ex3_img35.png)

<BR>
<BR>

Step 38: 
  
1. Enter the word `grocery`
2. Click **Add**
3. Click **Save**

![Image](img/ex3_img36.png)

<BR>
<BR>

Step 39: Click on **View** under 'View members' (again) to open the dimension value list.

![Image](img/ex3_img37.png)

<BR>
<BR>

Step 40: This time, click on the **edit** synonyms for 'Small Grocery'

![Image](img/ex3_img38.png)

<BR>
<BR>

Step 41: 
  
1. Enter the word `grocery`
2. Click **Add**
3. Click **Save**

![Image](img/ex3_img39.png)

<BR>
<BR>

Step 42: Click on **View** under 'View members' (yet again) to open the dimension value list

![Image](img/ex3_img40.png)

<BR>
<BR>

Step 43: 
  Observe that 'grocery' is used twice for two different values. This means 'grocery' will be used to mean both values, just as the business users want it to be.
  
Click **Close**.

![Image](img/ex3_img41.png)

<BR>
<BR>


### Setting default measure (and adding alias)

In case users don’t specify a measure we shall define a default one.
  
To help Just Ask identify the right model to use we shall add a model alias.

<BR>
<BR>

Step 44: 
  
1. Select **Settings**
2. Enter an alias corresponding to your user number `Sales 0${number}`
3. Change the default measure to **Sales**
4. Press **Save**

![Image](img/ex3_img42.png)

<BR>
<BR>


### Adding rules

Rules can help Just Ask to present the correct visualisation. 
  
In our case, the business users have told us:
  
- Whenever they use the measure *unit* they always want to see this over time, or by time.
- Whenever the dimension *State* is used, then ‘Country’ should also be included.
  
Thanks to rules, we help our users and reduce repeated effort on their part.

<BR>
<BR>

Step 45:
  
1. Select **Rules**
2. Click **Add Rules**

![Image](img/ex3_img43.png)

<BR>
<BR>

Step 46: 
This is part 1 of 3:
  
1. In the 'rule name' enter `add date when using unit`
2. In the 'When Search Contains' Select **Any of Measures (OR)**
3. Select **Unit**
4. Press **Next**

![Image](img/ex3_img44.png)

<BR>
<BR>

This is part 2 of 3:
  
1. In the Include Measure or Dimension, click **Add**
2. Under 'Select an object' select **Date**
3. Press **Next**

![Image](img/ex3_img45.png)

<BR>
<BR>

This is part 3 of 3:
  
1. **No action**. Observe the summary is correct
2. Press **Save**

![Image](img/ex3_img46.png)

<BR>
<BR>

Step 47: 
  Similarly add the next rule, but this is for State. Click **Add Rules**

![Image](img/ex3_img47.png)

<BR>
<BR>

This is part 1 of 3:
  
1.	In the 'rule name' enter `When dimension State is used include country`
2.	In the 'When Search Contains' Select **Selected Dimensions (AND)**
3.	Select **State**
4.	Press **Next**

![Image](img/ex3_img48.png)

<BR>
<BR>

This is part 2 of 3:
  
1.	In the 'Include Measure or Dimension', click **Add**
2.	Under 'Select an object' select **Country**
3.	Press **Next**

![Image](img/ex3_img49.png)

<BR>
<BR>

This is part 3 of 3:
  
1.	**No action**. Observe the summary is correct
2.	Press **Save**

![Image](img/ex3_img50.png)

<BR>
<BR>

Step 48: 
  Observe the summary is correct.

![Image](img/ex3_img51.png)

<BR>
<BR>

Step 49:
  
Now we have created these rules, as well as the synonyms, we can test them:
  
1. In the 'Test Rules' search box, enter the question `profitable states`
2. Press **enter**, or click **search**
3. No action. Observe the notification that rules have been applied.
4. No action. Observe that Country has been added because we asked for *State*.
  
You may also have observed that 'Profitable' is using the new measure you recently created called 'Profit'.

![Image](img/ex3_img52.png)

<BR>
<BR>

Step 50:
  
1. In the 'Test Rules' search box, enter the question `PCs brand`
2. Press **enter**, or click **search**
3. No action. Observe the notification that rules have been applied.
4. No action. Observe that 'Date' has been added because we asked for 'Units'. And 'Units' have been used because you referred to them by the term 'PCs'.

![Image](img/ex3_img53.png)

<BR>
<BR>

Step 51:
  
1. In the 'Test Rules' search box, enter the question `Grocery sales`
2. Press **enter**, or click **search**
3. Click on **Store** to open the pop-up window.
4. No action. Observe that both mid-sized and small grocery stores are selected saving your users from repeatedly re-selecting the one previously missed.

![Image](img/ex3_img54.png)

<BR>
<BR>

Step 52: 
  Exit this model and return to all the models.
  
Click **Models**.

![Image](img/ex3_img55.png)

<BR>
<BR>

### Adding model labels

Model lables can help Just Ask identify the right model, when there are many available. Its good practice to use them.

<BR>
<BR>

  
Step 53:
  
1. Select **Model Labels**
2. Click **Create Label**

![Image](img/ex3_img56.png)

<BR>
<BR>

Step 54:
  
1. Enter `Sales 0${number}`
2. Press **Save**.
  
If you accidently use a label called 'Sales', you will not be able to save it, as one of this name already exists.

![Image](img/ex3_img57.png)

<BR>
<BR>

Step 55: 
  Edit the label 'Sales0${number}'.

![Image](img/ex3_img58.png)

<BR>
<BR>

Step 56: 
1. Use the drop-down box to select your model **Just Ask Sales 0${number}**.
2. Press **Save**

![Image](img/ex3_img59.png)

<BR>
<BR>

Step 57: 
  Exit the manage models, by selecting **Manage Models**.

![Image](img/ex3_img60.png)
  

### Validate model behaviour

You have completed the necessary changes to both the model and the Just Ask model administration. Now, it's time to validate and compare your new model with the original to assess the benefits of your investment.

<BR>
<BR>

Step 58: 
  
1. Open Just Ask, and select your model from the list of indexed models **Sales 0${number}**. Example here shown is for 'Sales 001'
2. Observe the label used.

![Image](img/ex3_img61.png)

<BR>
<BR>

Step 59:
  
1. Click on ***+***
2. **Scroll down**
3. Click **Country**, which is now shown and is a parent of 'State'

![Image](img/ex3_img62.png)

<BR>
<BR>

Step 60: The drop-down box now shows values for 'Country' (previously, it did not). Select **USA**.

![Image](img/ex3_img63.png)

<BR>
<BR>

Step 61: 
  
1. The drop-down box now shows the measure for 'Profit' (previously, it did not). Select **Profit**.
2. Press **enter**, or click **search**.

![Image](img/ex3_img64.png)

<BR>
<BR>

Step 62:
  
1. With your model still selected enter `Country Profit` or use the **+** interface to select the same.
2. Press enter or click search.

![Image](img/ex3_img65.png)

<BR>
<BR>

Step 63:
  
1. Observe that 'Profit per Country' is now possible, thanks to the new calculated measure and the custom property added to the 'State' dimension.
2. Save this question, by clicking **country profit** under 'Save question'.

![Image](img/ex3_img66.png)

<BR>
<BR>

Step 64:
  
Now we shall ask the same question of the original model to compare the previous step
  
1. Use the model selection
2. Select the original **Just_Ask_Sakes_master_start** model
3. **De-select** your new model 'Sales 0${number}'
4. With the same search, `Country Profit`, press **enter**, or click **search**

![Image](img/ex3_img67.png)

<BR>
<BR>

Step 65:
  
1. Observe the notification that 'Sales' was added, and therefore profit wasn’t recognised.
2. Observe that 'State' was used in place of 'Country'. Just Ask knowns that 'Country' is part of the 'State' dimension because it’s the meta-data name of a parent-child hierarchy within the dimension. However, it's not identified as a unique dimension as we would like it to be for our use case.

![Image](img/ex3_img68.png)

<BR>
<BR>

### Consume saved question

We can consume the question we saved just earlier. In practice, you should have a good handful before letting your users access.

Step 66: 
  
1. Return to the home page of **Just Ask**
2. Open the **Sample Questions**
3. Open the model **Sales 0${number}**
4. Optionally open your **saved question**.

![Image](img/ex3_img69.png)

<BR>
<BR>

## Summary

You've now ...

Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)
