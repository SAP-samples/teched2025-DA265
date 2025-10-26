

# Exercise 1: Use case 1: Information Consumer

As an information consumer, you want to understand how sales in your organization compare to those in the various countries where you operate.
  

Step 1: Access the [SAP Workzone](https://six-joule-sac-teched25.launchpad.cfapps.eu10.hana.ondemand.com/site?siteId=0ec917b6-0536-46a8-9bff-df00dd211f8a#Shell-home).

<BR>
<BR>

Step 2: Log in with user and password as displayed next to the TechEd laptop.

<BR>
<BR>
<BR>
<BR>

Step 3: The screenshots will show the user **AIUSER001** and **AIUSER101**, naturally the screen for your user is likely to be different.

<BR>
<BR>
<BR>
<BR>

Step 4: Click on **Catalog**. This will open a pre-defined set of resources that are easier to discover.
  

![Image](1001.jpg){ width: 200px; }

<BR>
<BR>

Step 5: Identify the 'Sales Summary' item and click on **Open** 
  

> [!WARNING]
> If you see a 'request' button instead of an 'open' button, log out and sign in with a different user. The new username should be **AIUSER0${number}**


![Image](img/ex1_img2.png)

<BR>
<BR>

Step 6: **No action in this step**. Take a moment to observe the dashboard and feel free to interact with it. Use the dashboard to answer some straightforward questions, such as *What are the sales by state?* or *What are the year-to-date (YTD) sales?* These questions may not be easily obtained with the current dashboard. You'll need the power of AI to assist you.
  
![Image](img/ex1_img3.png)
  
<BR>
<BR>

Step 7: Click on the **light bulb icon** on the top right-hand side to open 'Just Ask'.

![Image](img/ex1_img4.png)

<BR>
<BR>

Step 8:
1. In the search box type `give me sales`
2. Press **enter** or click **search**

![Image](img/ex1_img5.png)

<BR>
<BR>

Step 9: **No action in this step**. Observe that you are instantly shown the total sales in $ and by millions (m).
A very simple question, but you’d like to see how your sales are performing across different states.

![Image](img/ex1_img6.png)

<BR>
<BR>

Step 10:
  
1. Type `give me sales by state`
2. Press **enter** or click **search**

![Image](img/ex1_img7.png)

<BR>
<BR>

Step 11: The visualisation is interactive, just like it is within an SAP Analytics Cloud story.
  

You can instantly compare the performance of one state against another.
1.	Click on **Washington**, then
2.	Click on **Ontario** to show the difference in sales performance.
3.	Observe the pop-up showing the variance.

![Image](img/ex1_img8.png)

<BR>
<BR>

Step 12: A table provides an easier way to see the hierarchy of states across countries.  
  
1. Click on **Table**
2. Click on **Mexico** and **USA** to show the Sales at the country level.
  
It would be nice to visualise these values which we shall do very shortly…

![Image](img/ex1_img9.png)

<BR>
<BR>

Step 13: The results so far, are across all time. You’re keen to see year-to-date sales.
  
1. Type `give me sales ytd by state`
2. Press **enter** or click **search**

> [!NOTE]
> The figures in the screenshots may vary as 'year-to-date' semantics change throughout the year. Just Ask knows the current time, and the screenshots were taken in January 2025.
  
  

![Image](img/ex1_img10.png)

<BR>
<BR>

Step 14:
  
1. Click on ‘**Date**’ to show the date range.
2. Observe the date selection has automatically selected the current year. Just Ask is aware of the current time.

![Image](img/ex1_img11.png)

<BR>
<BR>

Step 15: Combining the ‘YTD’ and the ‘top-level’ shown just a moment ago with the table so we can visualise that table from earlier, but with YTD values
  
1. Type `give me sales ytd by state drill on top level`
2. Press **enter** or click **search**

![Image](img/ex1_img12.png)

<BR>
<BR>

Step 16: And the chart continues to be interactive, for example:
  
1. Click on **Canada**
2. Click on **Drill Down on State** pop-up
3. Explore this dataset, click on **Analyze Data** which will open a new browser tab. 

![Image](img/ex1_img13.png)

<BR>
<BR>

Step 17:
  
1. If *Available Objects* are **not** shown, click to **Expand**
2. If *Available Objects* are **not** shown, click **Available Objects**
3. No action. Observe that the entire context of the question has been passed with all filters pre-selected to ensure you can continue your exploration without the need to re-select
4. Add **Store** as a *row*. It's easy to extend and tailor your visualisation.
5. Close the browser tab.

![Image](img/ex1_img14.png)

<BR>
<BR>

Step 18: You’re keen to see of the USA is performing.
  
1. Type `give me sales ytd by state drill on country USA`
2. Press **enter** or click the **search**

![Image](img/ex1_img15.png)

<BR>
<BR>

Step 19: **No action in this step**. Observe the drill level has been set
  
1. Click on **...**
2. Select **Drill**
3. Select **State** and see **Country** is the drill option set for you.

![Image](img/ex1_img16.png)

<BR>
<BR>

Step 20: Now you’d like to see how sales are compared to forecast.
  
1. Type `give me trend sales actual and forecast`
2. Press **enter** or click **search**

![Image](img/ex1_img17.png)

<BR>
<BR>

  
Step 21: **No action in this step**. Observe the Version has been set
  
1. Click on **Version**
2. Observe that both Actual and Forecast versions have been selected for you.
3. As you asked for *trend*, a time-series chart is shown, allowing you to easily change the time span as needed.

![Image](img/ex1_img18.png)

<BR>
<BR>

Step 22: Whilst a time-series chart is handy, you’re a quarterly-driven sales organisation, and you’re only interested in the *quarterly* summary. 
  
1. Type `give me trend sales actual and forecast by quarter`
2. Press **enter** or click **search**

![Image](img/ex1_img19.png)

<BR>
<BR>

Step 23: No action in this step.

  

Observe the Drill has been set
  
1. Click on **...**
2. Click **Drill – Date**
3. Observe *Quarter* has been selected for you as the drill level and the time-series chart x-axis now shows quarters, rather than days.

![Image](img/ex1_img20.png)

<BR>
<BR>

Step 24: Now, you’d like to understand how sales are performing against expense, i.e. you just want to 'expenses'
  

1. Type `give me trend sales and expense for actual and forecast by quarter`
2. Press **enter** or click **search**

![Image](img/ex1_img21.png)

<BR>
<BR>

Step 25: No action in this step.

  
Observe that expenses, for both actual and forecast, have been added for you.

![Image](img/ex1_img22.png)

<BR>
<BR>

Step 26: Now you’d like to turn your attention to the performance by store (type).
  


1. Type `Show me sales by store as a pie chart`
2. Press **enter** or click **search**

![Image](img/ex1_img23.png)

<BR>
<BR>

Step 27: No action in this step.  
  
Observe you can ask for the visualisation as you desire, in this case, a pie chart. Clicking on a slice shows a pop-up window with more details.

![Image](img/ex1_img24.png)

<BR>
<BR>

Step 28: Now as a heatmap
  
1. Type `give me the sales by state and store as heatmap`
2. Press **enter** or click **search**

![Image](img/ex1_img25.png)

<BR>
<BR>

Step 29: No action in this step.

  
Observe you may interact will all charts, including simple functions such as excluding.
  
1. Click on a **value**
2. Click on the **X** to exclude this State/Store 

![Image](img/ex1_img26.png)

<BR>
<BR>

Step 30: Now you need AI to help identify your top-performing products
  
1. Type `top 3 product by sales and state`
2. Press **enter** or click **search**
        
![Image](img/ex1_img27.png)

<BR>
<BR>

Step 31: No action in this step.

  
Observe the ranking option has been selected for you
  
1. Click on **...**
2. Click on **Rank**
3. Click on **All Dimensions**
4. Observe **Top 3** has been selected for you. 

![Image](img/ex1_img27_img_p2.png)

<BR>
<BR>

Step 32: Your attention is now on the number of units sold and you want to compare 2025 units with the previous year:
  
1. Type `Compare 2025 units with previous year`
2. Press **enter** or click **search**

![Image](img/ex1_img28.png)

<BR>
<BR>

Step 33: No action in this step.
  

Observe the variance comparison has been selected for you with the current year also automatically selected
  
1. Click on **...**
2. Click on **Applied to Chart**
3. Observe the **Variance**

![Image](img/ex1_img29.png)

<BR>
<BR>

Step 34: Now, you want to see how the current month compares.
  
1. Type `compare actual units with forecast for this month`
2. Press **enter**, or click **search**

![Image](img/ex1_img30.png)

<BR>
<BR>

Step 35: No action in this step. Observe the current month has been selected for you. (Screenshot taken in January 2025)
  
1. Click on **Date**
2. Expand **all**
3. Expand current year **2025**
4. Expand current **Half** *H1* (or *H2*)
5. Observe the current month is selected for you. (screenshot taken in January 2025)

![Image](img/ex1_img31.png)

<BR>
<BR>

Step 36: You’re now curious about last year's unit sales, but you’re only interested where unit sales exceed 1 million
  
1. Type `Show me units for brand and corporation by state higher 1M for last year`
2. Press **enter** or click **search**

![Image](img/ex1_img32.png)

<BR>
<BR>

Step 37: No action in this step. Just Ask can understand units of measure. Observe the filter has restricted units to values >= 1000000 ( 1 million )
  
1. Click on **Date , ...** filter
2. Observe the Unit filter

![Image](img/ex1_img33.png)

<BR>
<BR>

Step 38: You’ve returned your focus to the expense and sales forecast comparison. This time, for next month’s values
  
1. Type `what's the expenses and sales by brand next month forecast`
2. Press **enter** or click **search**
        
![Image](img/ex1_img34.png)

<BR>
<BR>

Step 39: No action in this step.

  

  
Observe the filter has restricted units to values >= 1000000 ( 1 million )
  
1. Click on **Date , ...** filter
2. No action, just observe the Unit filter

![Image](img/ex1_img35.png)
  

<BR>
<BR>

Step 40: A scatterplot chart isn’t as helpful for comparison, so a bar chart is needed.
  
1. Type `what's the expenses and sales by brand and corporation next month forecast as bar chart`
2. Press **enter** or click **search**

![Image](img/ex1_img36.png)
  

<BR>
<BR>

Step 41: No action in this step.

  

Observe the complexities of the filtering and variance comparison have all been done for you.

<BR>
<BR>

 
SAP Analytics Cloud generates visualizations that are certified by the International Business Communication Standards (IBCS). This is the reason the forecast is presented in this specific format. Just Ask will consistently strive to create visualizations that adhere to IBCS guidelines. To learn more about IBCS, visit https://www.ibcs.com/software/sap-analytics-cloud/.

![Image](img/ex1_img37.png)
  

<BR>
<BR>

  
## Exercise 1.2: Consume (dynamically created) related questions:
  
  
Dynamically generated questions serve as prompts, helping you explore related inquiries.

  
  
1. Observe (no action) the bottom right-hand corner has several pre-defined questions relating to the model in use.  You will use these soon, not now.
2. The top right-hand corner has several dynamically created questions you can ask. Select one of these.

  
  
Optionally repeat step 2 several times.

![Image](img/ex1_img38.png)


<BR>
<BR>


> [!TIP|icon:fa-solid fa-check|label:Congratulations]
>  You have completed exercise 1 of 4.




## Summary

You've now ...

Continue to - [Exercise 2 - Exercise 2 Description](../ex2/README.md)

