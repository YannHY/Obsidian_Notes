---
tags: [Documentation, Google, Sheets, training]
author: [Yann Houry]
date: 17-05-2022
---

[Google Docs](https://docs.google.com/document/d/1Cjkib5-dfWNP6w6YveAVRpjcI9K6D4nhEObRmGyQI9o/edit#)

## Exercises
- [File's link](https://docs.google.com/spreadsheets/d/1oQzxDOxmBLhL8qTLgl2QDc2XxQNWh83XmBIUehuL25Q/edit)
- [File's link with solutions](https://docs.google.com/spreadsheets/d/1DLt2jv2I9jiHSGck2-Z0wlX9QxY886MYZURa_b4-31A/edit?usp=sharing)

### Exercise 1 TICK/DATA VALIDATION
1. Create a pop-up calendar date picker.
2. Create a drop-down menu (list of items).
3. Insert a box to tick.
4. Use conditional formatting both for the drop-down menu and the boxes to tick.

### Exercise 2 Explore Tool
1. Select your data.
2. Click on Explore Tool (located on the bottom-left corner)
3. Add a chart.
4. Choose a format for your data.
5. Ask a question or insert a formula.

### Exercise 3 SPLIT & CONCATENATE
1. Split a list of names
2. Copy and paste the values
3. Concatenate first names and last names

### Exercise 4 SORT, AVERAGE, SUM
1. Sort column 1 *Location* alphabetically (A - Z).
2. Calculate the average number of visitors to all 7 wonders of the world.
3. Calculate the total number of visitors to all 7 wonders of the world.

### Exercise 5 UNIQUE, SORT
1. Returns unique rows discarding duplicates.
2. Sort the authors in the ascending order (A to Z) combining UNIQUE and SORT functions.

### Exercise 6 FILTER, CONDITIONAL FORMATTING
1. Create a filter to display only grades below 10.
2. Use conditional formatting so the highest grades are highlighted in green and the lower are in red.
3. Create a filter only for yourself.

### Exercise 7 DATE
1. Insert the date using the keyboard shortcut.
2. Duplicate the date in 7 columns.
3. Now do the same but using `=DATE()`.
4. Enter the date manually (say in A9). In the next cell, type `=A9+7`.

### Exercise 8 IF
1. We have four grades (20, 9, 17, 7).
2. If the grade is above 10, we display a cheerful emoji otherwise we insert a sad emoji.

### Exercice 9 IF AND/OR
1. Create a table with three columns and 2 rows.
2. Put the number 8 and 1 in every row and then each of the following formulas:
	1. If C5 = 1 and B5 < 5, display Yes else No.
	2. If C5 = 1 or B5 < 5, display Yes else No.

### Exercice 10 NESTED IF
You want to assess student participation.

To do that, using Data validation (this has already been done for you), you created a dropdown menu (Very good participation, Good participation, Attentive but not involved, Not working).

Create a nested if to award 2 points if the student participates very well, 1 point if the participation is good, 0.5 if the student is attentive but not participating else nothing.

### Exercice 11 COUNTIF
#### Part 1
In this table, you have a list of expenses.
Count the number of times you had coffee.

#### Part 2
Your student has 6 grades.
Count the amount of grades below 10.

### Exercice 12 SUMIF
In your expense list, only count the cost of the cab.

## Documentation
### DATA VALIDATION/TICK/CONDITIONAL FORMATTING
#### Data validation
##### Insert a pop-up calendar date picker
Avoid any errors by inserting a pop-up calendar date picker.

Go to `Data` > `Data validation`. In `Criteria`, select `Date`. Click Save.

Now, when you double click a cell, a pop-up calendar appears.

<iframe width="560" height="315" src="https://www.youtube.com/embed/Bc7ip1uXqd0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

##### Insert a drop-down menu
Go to `Data` > `Data validation`. In `Criteria`, select `List of items`. Insert a list of items separated by commas. Click Save.

Alternatively, you may create your list on a separate sheet. That way, it may be easier to read or to update it, especially if you have a long list. 

Then, in `Data validation`, write a formula like 
````
=LIST!B2:B
````
(meaning your list is on the LIST sheet in column B).

You can even hide the sheet (click on the little arrow and choose `Hide sheet`).

#### Tick
Go to `Insert` > `Tick box`.

#### Conditional Formatting
Go to `Format` > `Conditional formatting` .

You can choose to apply a single colour or a colour scale.

If you pick "Single colour", choose the range, the format rules and the formatting style:

1. Single colour
2. Apply to range
3. Format rules = Text is exactly (Yes or No)
4. Formatting style = pick green for Yes, red for No
5. Add another rule (if you need to)

[Use conditional formatting rules in Google Sheets](https://support.google.com/docs/answer/78413?hl=en&co=GENIE.Platform%3DDesktop)

##### Conditional Formatting For Tick Boxes
1. Single colour
2. Apply to range
3. Format rules = Custom formula is
4. 
````
=B9:B37=TRUE
````
or
````
=B9:B37=FALSE
````
5. Formatting style = pick green for true, red for false
6. Add another rule (if you need to)

### Explore Tool
> Most of us work with loads of data on our spreadsheets. Wouldn’t it be nice to have an assistant that can intuitively help us with our work, so that we can speed it up? The Explore feature in Google Sheets does exactly that. It intelligently gathers the context that we are working upon, and gives us the right suggestions that might be suitable for the purpose. And its insightful suggestions include tips for formatting, charting, pivot tables etc. If we can’t find something, we can even ask for answers. ([Link](https://blog.sheetgo.com/google-sheets-features/explore-feature-google-sheets/))

<iframe width="560" height="315" src="https://www.youtube.com/embed/jr-NRP2MYVc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### SPLIT
Go to `Data` > `Split text to columns`.

Use the space separator if you want to split first and last names.

Or use the [Split function](https://www.benlcollins.com/spreadsheets/split-function/): `=SPLIT(A2," ")`.

> In the case of Last, First you want the last name in one cell and the first name in another cell. What is preventing you from doing that is a comma AND A SPACE!!! It’s so easy to miss realizing the space between the names. If the name is in A2 then in B2 (or any blank cell) I start with an equals sign and put =SPLIT( and then click on A2 so it automatically is added to my formula. Put a comma. IN QUOTATIONS put the delineator. In this case it is “, ” [...]. [Google Sheets: Split Up Student Names](https://alicekeeler.com/2021/07/03/google-sheets-split-up-student-names/)

Want to copy and paste the values? `cmd (or ctrl) + shift + v` (or right click > `Paste special` > `Values only`).

### CONCATENATE
[Concatenate data from multiple cells](https://www.howtogeek.com/447559/how-to-concatenate-data-from-multiple-cells-in-google-sheets/)

`=CONCATENATE(B2," ",C2)`

### SORT
#### Option 1
1. Highlight the group of cells you'd like to sort.
2. If your sheet includes a header row, [freeze the first row](https://support.google.com/docs/answer/9060449) (`View` > `Freeze`).
3. Click `Data` > `Sort range` > `Advanced range sorting options`.
4.  If your columns have titles, click `Data has header row`.
5.  Select the column you'd like to be sorted first and choose a sorting order. To add another sorting rule, click `Add another sort column`.
6.  Click `Sort`.

#### Option 2
[Documentation](https://support.google.com/docs/answer/3093150)

````
=SORT(A2:B8, 2, TRUE)
````

- Range of cells A2 to B8
- Sort column is 2
- Set to TRUE, the data will be sorted in the ascending order.

<iframe width="560" height="315" src="https://www.youtube.com/embed/FVDvbG9nPrw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### AVERAGE
[Documentation](https://support.google.com/docs/answer/3093615?hl=en)

````
=AVERAGE(B2:B10)
````

### SUM
[Documentation](https://support.google.com/docs/answer/3093669?hl=en-GB)

````
=SUM(B2:B10)
````

### UNIQUE
````
=UNIQUE(UNIQUE!B2:B)
````

[Documentation](https://support.google.com/docs/answer/3093198)

As you can see, you need to specify the name of the sheet (`UNIQUE!`) and add an exclamation mark. Handy if you want to pull data from another sheet.

You can combine SORT and UNIQUE:

The SORT function contains three parts: **range**, **column to sort**, **ascending or descending order**. Of course, we put the UNIQUE function in the range part.

````
=SORT(UNIQUE(B2:B),1,TRUE)
````

➝ [Google Sheets Functions – UNIQUE, COUNTUNIQUE, SORT](https://www.bazroberts.com/2016/11/07/google-sheets-functions-unique-countunique-sort/)

### FILTER
- [Filter data in a spreadsheet](https://support.google.com/a/users/answer/9308952?hl=en)
- [Sort & filter your data](https://support.google.com/docs/answer/3540681?hl=en&ref_topic=9066125)

<iframe width="560" height="315" src="https://www.youtube.com/embed/nSo_Ops5o2w" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Option 1
[Documentation](https://support.google.com/docs/answer/3093197)

1. Select your column
2. Data > Create a Filter

Or simply click the icon on the top right corner.

The creation of a filter affects everyone. If you want just for yourself, choose `Data` > `Filters Views`. You can save it so your team can use it.

#### Option 2
````
=FILTER(A2:B13,B2:B13<10)
```` 
(only displays grades below 10 in column B3 to B31)

### Date
You can insert the date in many ways.

#### Enter the date with a shortcut
To insert the date, press `cmd or ctrl + ;`  (be sure to go to `Help > Keyboard shortcuts` and activate `Enable compatible spreadsheet shortcuts`).

#### Enter the date using DATE() or NOW()
To display a time or a date (which will be automatically updated every day when you open up your spreadsheet), use the functions `=DATE()` (receive three arguments) or `=NOW()` (provides date and time). To create a date without the current time, use [`TODAY`](https://support.google.com/docs/answer/3092984).

#### Display the time
To only display the time, use `TIME()` (three arguments)

[Documentation (DATE)](https://support.google.com/docs/answer/3092969?hl=fr)
[Documentation (NOW)](https://support.google.com/docs/answer/3092981?hl=en)
[Documentation (TIME)](https://support.google.com/docs/answer/3093056?hl=en)

#### Examples
##### DATE
`DATE(1969,7,20)` (year, month, day)
`DATE(A2,B2,C2)`

To format the date, head to `Format > Number > Date`.
To customise the format, go to `Format > Number > Custom date and time formats`.

Want the date of every week? Just enter the date manually (say in A9). In the next cell, type `=A9+7`.

##### TIME
`TIME(11,40,59)` (hour, minute, second)
`TIME(A2,B2,C2)`

###  IF
[Demo](https://docs.google.com/spreadsheets/d/14pOtBcw2gMkuZuHTodbiV-woCuPowM7bBDdoVIeGhjg/edit?pli=1#gid=0) 

#### Simple IF
`=IF(test, value_if_true, value_if_false)`

> If you want to run a logical test in a Google Sheets formula, providing different results whether the test is **TRUE** or **FALSE**, you’ll need to use the IF function.
> As the name suggests, IF is used to test whether a single cell or range of cells meets certain criteria in a logical test, where the result is always either TRUE or FALSE.  
> If the IF test is TRUE, then Google Sheets will return a **number** or **text string**, **perform a calculation**, or **run through another formula**.  
> If the result is FALSE, it’ll do something completely different. You can **combine IF with other logical functions like AND and OR** or with other **nested IF** statements.  

[How to Use the Google Sheets IF Function](https://www.howtogeek.com/449861/how-to-use-the-google-sheets-if-function/)

[Documentation](https://support.google.com/docs/answer/3093364?hl=en)

#### Using IF with AND and OR
- To use IF AND, type
````
=IF(AND(AND Argument 1, AND Argument 2), value_if_true, value_if_false)
````

- To use IF OR, type
````
=IF(OR(OR Argument 1, OR Argument 2), value_if_true, value_if_false)
````

> As the IF function performs logical tests, with TRUE or FALSE results, it’s possible to nest other logical functions like AND and OR into an IF formula. This allows you to run an initial test with multiple criteria.

> The AND function requires all test criteria to be correct for a TRUE result to be shown. OR requires only one of the test criteria to be correct for a TRUE result.

[How to Use the Google Sheets IF Function](https://www.howtogeek.com/449861/how-to-use-the-google-sheets-if-function/)

#### Nested IF Statements
`=IF(first_test, value_if_true, IF(second_test, value_if_true, value_if_false))`

 ```
=IF(first_test, value_if_true, 
     IF(second_test, value_if_true, 
        IF(third_test, value_if_true, value_if_false
          )
       )
    )
```

#### COUNTIF
Count how many items in a range meet a given criterion.

Syntax: `COUNTIF(range, criterion)`

[Documentation](https://support.google.com/docs/answer/3093480)

##### Examples
````
=COUNTIF(A1:A9, "Coffee")
````
(count how many coffee there are)

The range is `A1:A9`. The criterion is `Coffee`.

````
=COUNTIF(B14:G14, "<10")
````
(count how many grades below 10)

The range is `B14:G14`. The criterion is `<10`.

`COUNTIF` can only perform conditional counts with a single criterion. To use multiple criteria, use `COUNTIFS` ([link](https://support.google.com/docs/answer/3256550)).

#### SUMIF
What is the sum if we are talking of a specific item?

Syntax: `SUMIF(range, criterion, [sum_range])`

[Documentation](https://support.google.com/docs/answer/3093583)

##### Example
````
=SUMIF(A2:A9, "Taxi", B2:B9)
````

(says how much I spent for taxi, i.e. in `A2:A9`, if there is "Taxi", what's the sum in `B2:B9`?)
