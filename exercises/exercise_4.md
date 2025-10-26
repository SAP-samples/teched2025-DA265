# Understanding indexing

In this section of the workshop, we will explore the types of metadata stored by Just Ask. We will discuss scenarios where it is essential to disable the storage of specific values to protect data privacy. Additionally, we will examine when it is necessary to re-index a model or re-sync it to ensure that Just Ask updates its metadata with the new values.

  

An overview of this section:

1. Enable the 'Brand' dimension to be *access controlled*.
2. We will have two brands, ‘Even Better’ and ‘Hermanos,’ classified as restricted members. Additionally, we will assign another user, referred to as  **AIUSER1${number}**, to have read-only access to these values. This user should not be able to view any other brands.  Both ‘Even Better’ and ‘Hermanos’ are part of the corporation known as ‘Global Essence Group,’ and we are happy for the user AIUSER101 to be aware of this.
3. We will discover that user **AIUSER1${number}** has incorrect access to restricted 'Brands'. By adjusting the administration settings of the Just Ask model, we can prevent the import of dimension values, which will resolve this issue.
4. Finally, we will change a dimension value to demonstrate that we need to resynchronize the model so Just Ask is aware of the change.

<BR>
<BR>

## Set 'State' with Data Access Control restricting 2 brands for the user AIUSER1${number}  

Step 1: Exit Just Ask

![Image](img/ex3_img70.png)

<BR>
<BR>

Step 2:
  
1. Open the SAP Analytics Cloud **menu**
2. Select **Modeler**
3. From the recent file open your model **Just Ask Sales 0${number}**

![Image](img/ex4_img1.png)

<BR>
<BR>

Step 3: 
  Open the **Model Preference**

![Image](img/ex4_img2.png)

<BR>
<BR>

Step 4: 
  
1. Click **Access and Privacy**
2. **Scroll down**
3. Enable **Data Access Control** for **Brand**
4. Press **OK**

![Image](img/ex4_img3.png)

<BR>
<BR>

Step 5: 
  In the Dimensions, **edit** the **Brand Dimension table**.

![Image](img/ex4_img4.png)

<BR>
<BR>

Step 6: 
  
1. In the 'Read' column for the members 'Even Better' and 'Hermanos' enter the user ID `AIUSER1${number}` (notes: There are no quotes, and there are no spaces in the user id)
2. Press **Save**
  
The user  **AIUSER1${number}** is *not* the same as your current user.
![Image](img/ex4_img5.png)

<BR>
<BR>

### As user AIUSER1${number} observe all brands listed.

User AIUSER1${number} should not be able to list all the brands since they are restricted for this user. However, you will soon experience that this user can list all the brands.

<BR>
<BR>

Step 7: 
  
For your browser, **create** a new **guest profile**.
  
We need to log in using a different profile to observe what values this user can see. We could use the existing profile but we would then have to repeatedly log out and log in.
  
![Image](img/ex4_img6.png)

<BR>
<BR>

Step 8: 
  
1.	Enter the user id `AIUSER1${number}`
2.	Enter the password `${sac1.password}`
3.	Click **Continue**

![Image](img/ex4_img7.png)

<BR>
<BR>

Step 9: 
  Open **Just Ask**

![Image](img/ex4_img8.png)

<BR>
<BR>

Step 10: 
  
1.	Use the **model selection**
2.	Select the model **Sales 0${number}**
3.	In the search box, enter `Brand sales`
4.	Press **enter** or click **search**.

![Image](img/ex4_img9.png)

<BR>
<BR>

Step 11: 
  
1.	Observe that the only 'Brands' returned in the visualisation are the correct two values for this user. This means the data access control is working as expected.
2.	In the search box, enter `brand`
3.	Observe the Just Ask list of values shows additional values to what was returned just earlier. See '*Jumbo*' and '*Sunset*' are listed.
   
In our use case, we don’t want this user to know about these other brands. We need to instruct Just Ask not to display these values.

![Image](img/ex4_img10.png)

<BR>
<BR>

### Disable member import

Step 12:
  In the **other** browser window with user *AIUSER0${number}* logged-in, open **Just Ask**

![Image](img/ex4_img11.png)

<BR>
<BR>

Step 13: 
  Click **Manage Models** to manage the Just Ask models.

![Image](img/ex4_img12.png)

<BR>
<BR>

Step 14: 
  Open your model **Just Ask Sales ${number}**.

![Image](img/ex4_img13.png)

<BR>
<BR>

Step 15:
  
1. Press the **edit icon**
2. **Expand** 'Brand', so 'Corporation' is also shown (for no reason)
3. De-select **Include**
4. Press **save**

![Image](img/ex4_img14.png)

<BR>
<BR>

Step 16: 
  Observe the warning and press **Save**

![Image](img/ex4_img15.png)

<BR>
<BR>

Step 17: 
  **Switch to the the other (guest) browser tab**, with the user **AIUSER1${number}** logged in.

<BR>
<BR>

Step 18: 
  **Reload** the entire interface to be sure that Just Ask identifies a change to the model.

![Image](img/ex4_img19.png)

<BR>
<BR>

Step 19: 
  Open **Just Ask**

![Image](img/ex4_img8.png)

<BR>
<BR>

Step 20: 
  
1. With the **model selection**
2. Select the model **Sales 0${number}** (Example screenshot is for user: *Sales 001*).

![Image](img/ex4_img20.png)

<BR>
<BR>

Step 21: 
  
1. With the **+** interface
2. **Observe** that both 'Brand' and 'Corporation' are correctly listed.
3. Select **Brand**

![Image](img/ex4_img21.png)

<BR>
<BR>

Step 22: 
  Notice that there are no brand values; this is the behaviour we intended. It means this user no longer has access to the list of brand values.

![Image](img/ex4_img22.png)

<BR>
<BR>

Step 23: 
  
1. Add the word `Sales`, so the question is `Brand Sales`
2. Press **enter** or click **search**

![Image](img/ex4_img23.png)

<BR>
<BR>

Step 24: 
  Observe the brands listed remain unchanged and correct. We’ve not been exposed to values we should not see.

![Image](img/ex4_img24.png)

<BR>
<BR>

### Changing the dimension value requires re-sync

<BR>
<BR>

Step 25: 
  **Switch to the other (no guest) browser tab**, with the user **AIUSER0${number}** logged-in

<BR>
<BR>

Step 26: 
  **Exit Just Ask**

![Image](img/ex4_img27.png)

<BR>
<BR>

Step 27: 
  
The model should be open, if not open the **Just Ask Sales 0${number}** model.
1. Change the 'Corporation' value from ***Global Essence Group*** to ***Global Essence Inc*** 
2. **Save** the model
3. Open **Just Ask**

![Image](img/ex4_img28.png)

<BR>
<BR>

Step 28: 
  
The Just Ask modeller should be open, if not open the modeller and select the model **Just Ask Sales 0${number}**.
1. **Expand** the 'Brand' to show 'Corporation'
2. Select the *View members*

![Image](img/ex4_img29.png)

<BR>
<BR>

Step 29: 
  
1. **Observe** that the values for this dimension are the old values '*Group*' and not the new values you’ve just changed them to '*Inc*'. It means Just Ask needs to be updated with new values.
2. Click **Close**

![Image](img/ex4_img30.png)

<BR>
<BR>

Step 30: 
  Click **Sync model**

![Image](img/ex4_img31.png)

<BR>
<BR>

Step 31: 
  Observe the warning and press **Sync model**.
  
Sometimes the model synchronisation takes a long time, so it's handy to have the option to cancel if you accidentally press 'sync model'.

![Image](img/ex4_img32.png)

<BR>
<BR>

Step 32: 
  Observe the notification. Feel free to explore the logs.

![Image](img/ex4_img33.png)

<BR>
<BR>

Step 33: 
  
Once complete, 
1. Open the '**Brand**' to show 'Corporation'.
2. Select '**open dimension value list**' to 'View members'

![Image](img/ex4_img34.png)

<BR>
<BR>

Step 34: 
  
1. **Observe** the now correct values for the brand; it shows 'inc' instead of 'group'.
2. Press **Close**

![Image](img/ex4_img35.png)


<BR>
<BR>

Step 35: 
  **Switch to the other (guest) browser tab**, with the user **AIUSER1${number}** logged in

<BR>
<BR>

  
Step 36: 
  
1. Use the **+** button
2. Select '**Corporation**'

![Image](img/ex4_img36.png)

<BR>
<BR>

Step 37:  
  
Both corporations are listed. We are pleased for this user to know each corporation exists, unlike all the brands.
  
All corporation values are available because the dimension members remain imported.

![Image](img/ex4_img38.png)

<BR>
<BR>

**You have now understood when you need to disable importing dimension members and when a re-sync is needed.**

<BR>
<BR>

> [!TIP|icon:fa-solid fa-check|label:Congratulations]
> You have completed exercise 4 of 4.





