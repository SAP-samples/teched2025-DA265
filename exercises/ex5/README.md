# Exercise 5 - Understanding Indexing

In this section of the workshop, we will explore the types of metadata stored by Just Ask. We will discuss scenarios where it is essential to disable the storage of specific values to protect data privacy. 

Additionally, we will examine when it is necessary to re-index a model or re-sync it to ensure that Just Ask updates its metadata with the new values.

## Updating model dimension values

### Step 1: Open Brand Dimension

> The model should already be open from an earlier exercise. If not, please open your copied model 'DA256 Sales' from the root of 'My Files'
1. Select the **Model Structure**
2. No action. Validate that the model is the correct model 'DA265 Sales'
2. Click on the **Edit Dimension Table** for the ***Brand*** dimesnion

![Image](img/7129.jpg)
  

<BR>
<BR>
<BR>
<BR>

### Step 2: Rename 'Global Essence Group' to 'Global Essence Inc', open Just Ask
  
1. Rename the 'Corporation' value for 'Even Better' from '**Global Essence Group**' to `Global Essence Inc`
2. Rename the 'Corporation' value for 'Hermanos' from '**Global Essence Group**' to `Global Essence Inc`
3. Click **Save**.
4. Open Just Ask by clicking on the **Just Ask** icon.

![Image](img/7130.jpg)
  

<BR>
<BR>
<BR>
<BR>

### Step 3: Old values shown by Just Ask

1. Click on the **Just Ask** logo to show the home page
2. Click on the **+** icon and select **Corporation**
3. Observe the list of values shown include the old value 'Global Essence Group' and not the updated value 'Global Essence Inc'

> Screenshot taken between steps 2 and 3

It means that we need to re-index the model for these new values to be shown within the Just Ask interface.

![Image](img/7131.jpg)
  

<BR>
<BR>
<BR>
<BR>

## Re-sync model

### Step 4: ssss
  
1. Select **Manage Models**
2. Select the **TechEd (DA265 Sales)** model


![Image](img/7132.jpg)
 

<BR>
<BR>
<BR>
<BR>

### Step 5: Sync-model

1. Click **Sync model**
  
Re-syncing the model will re-index the values. It will also re-read the data structures and any other changes you've made, such as adding calculated measures. 

![Image](img/7133.jpg)
  

<BR>
<BR>
<BR>
<BR>

### Step 6: Confirm
  
Your business refers to '*Grocery*' as '*Mid-Size Grocery*' and '*Small Grocery*'.
However, when you ask for *Grocery Sales* both these values are not selected, instead, you must manually select the missing one.

Try it:
  
1.	Type `Grocery Sales`
2.	Press **enter**, or click **search**
3.	Open the **Store** filter
4.	Select the missing **Grocery** value, so that both 'Mid-Size' and 'Small' are selected.

![Image](img/7134.jpg)
  

<BR>
<BR>
<BR>
<BR>







## Summary




Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)
