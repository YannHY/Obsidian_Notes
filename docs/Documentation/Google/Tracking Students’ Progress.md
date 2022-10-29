---
tags: [Tutorial, Google]
---

I want to be able to easily track students’ progress and I want everything to be in one place. So I made [this spreadsheet](https://docs.google.com/spreadsheets/d/113g9xxHOCXHKNI4DkIiIBmmaAgzX9NDTxtMt-l9jO4Y/edit#gid=963676669) (though I have to confess that, at the beginning, I wanted to make a workshop dedicated to spreadsheets so participants could learn as many functions as possible).

There are 18 sheets in this spreadsheet. I called the first one Home (“Accueil” in French). On this home page, you will find links to all the other sheets. On the last one, you will find support and explanation on how to use and modify them (sorry but it’s in French).

![[accueil.png]]
![[aide.png]]
The other seventeen sheets are:

-   Grade (term 1)
-   Grade (term 2)
-   Charts (term 1)
-   Charts (term 2)
-   Competences
-   Assess participation (term 1)
-   Assess participation (term 2)
-   Comments
-   Report (term 1)
-   Report (term 2)
-   Attendance
-   Special Needs
-   Accounts
-   Create groups
-   Student Picker
-   Seating plan

Depending on the sheet, you will find one link to Google Classroom and one link to Pronote. If needed, you will find the date and time as well.

You can insert the date in many ways:  

-   To insert the date, press `cmd or ctrl + ;`  (be sure to go to `Help > Keyboard shortcuts` and activate `Enable compatible spreadsheet shortcuts`).
-   To display a time or a date (which will be automatically updated every day), use the functions `=NOW()` or `=DATE()`. To format the date, head to `Format > Number > Date`.
 
More on that in [How to Add the Current Date and Time in Google Sheets](https://www.howtogeek.com/448444/how-to-add-the-current-date-and-time-in-google-sheets/).

## Grades & Competences
Enter your grades. The spreadsheet calculates the average. You get the lowest and highest grades or number of grades below, say, 10.

`Conditional formatting` helps you figure out what are the overall results in a glimpse. Of course, you can filter these results. This means you can see only the grades below ten. More on that down below.

![[notes.gif]]

The results can be browsed individually and show you a dynamic graphic as well.

![[resultats-individuels.gif]]

I use the box next to the chart to take notes when filling the reports.

Here are the functions I used:

-   `=AVERAGE(B3:M3)` → calculate the grade average
-   `=SUM(N4:W4)`→ Sum up numbers
-   `=SPARKLINE(B3:M3)` → Sparklines are small, lightweight charts that exist inside a single cell (read [How to Use Sparklines in Google Sheets](https://www.howtogeek.com/450155/how-to-use-sparklines-in-google-sheets/) or [Everything you ever wanted to know about Sparklines in Google Sheets](https://www.benlcollins.com/spreadsheets/sparklines-in-google-sheets/) to learn more)
`=SPARKLINE($B50:$M50,{"charttype","bar";"max",AVERAGE(B50:M50);"color1","#3C8CD6";"color2","#F0EEEE"})( to display a progress bar)`
-   `=(B2)` → avoid to write something twice
-   `=MAX(B3:B31)` → display the highest grades
-   `=MIN(B3:B31)` → display the lowest grades
-   `=COUNTIF(B$9:B$37, "<10")` → Count only certain values
-   `=VLOOKUP($A50, $A3:$M31, 2, false)` → extracts data from cell in specified column, using specified search key (watch and read [How to Use VLOOKUP in Google Sheets](https://www.youtube.com/watch?v=_yKn70cl-Mo) & [How to Find Data in Google Sheets with VLOOKUP](https://www.howtogeek.com/447024/how-to-find-data-in-google-sheets-with-vlookup/) to learn how to master these functions)
    
To display the colors, use `Conditional Formatting` (`Format > Conditional Formatting`) It will colour certain items depending on the criteria you choose (ie A grade below 10).

-   For grades, choose “Greater than” or “Less than or Is equal to”.
-   For assessing participation (see down below), pick “Text is exactly”.

![[conditional-formatting.gif]]

## Charts
With charts, results become more visual. You can create a chart for each assessment or a chart for all the results during the term (`Insert > Chart`).

![[charts.gif]]

If you need help with charts, have a look at this page: [Add & edit a chart or graph](https://support.google.com/docs/answer/63824?co=GENIE.Platform%3DDesktop&hl=en). You may also want to [watch one of these videos on YouTube](https://www.youtube.com/playlist?list=PLv9Pf9aNgemsnwb2uNnVsTOzCJZudPUOD).

## Assess participation
Quickly assess participation by selecting in a drop-down menu the appropriate observation. A grade is automatically generated accordingly.

![[participation.gif]]

To create a dropdown menu (fastest way to insert data), use `Data Validation` (`Data > Data Validation`) and choose “List of items” (or “Number” if you prefer).

![[data-validation.gif]]

I also use `Data Validation` for filling reports (have a look at [Create a drop-down list where the list is separate sentences that include commas](https://support.google.com/docs/thread/16942201?hl=en)).

As I want to automatically grade participation during class, I use an `IF` function. Basically, if a student is doing a great job (excellent participation for instance), he or she gets two points. To know more about the `IF` function, [read this](https://support.google.com/docs/answer/3093364?hl=en-GB).

It should look something like this:  

`=IF(B4="très bonne participation", 2, 1)`

As we have multiple conditions, we need nested if:

```
=IF(logical_expression, value_if_true, 

 IF(logical_expression, value_if_true, 

 IF(logical_expression, value_if_true, value_if_false

 		)

 	)

 )
```
  
```
=IF(B7="très bonne participation", 2, 

 IF(B7="bonne participation", 1, 

 IF(B7="suit mais ne participe pas", 0.5, 0

 		)

 	)

 )
```
  
As there is no need to display the calculation, some rows have been hidden. To learn how to hide a row or column in a Google Spreadsheet, [read this article](https://gsuitetips.com/tips/sheets/hide-rows-and-columns-in-a-google-spreadsheet/).

## Reports
Produce a full report by selecting your appreciation in a ready-made bank. Then you just have to copy and paste the whole thing.

I also take notes on a daily basis so that the process of writing an appreciation runs throughout the whole period. My final appreciation becomes more accurate and feels more personal.

![[reports.gif]]

To do that, I made a bank of observations (see screenshot down below).

![[bank.png]]

When selecting a student, a drop-down menu (made with `Data Validation`) takes these observations providing your criteria is “List from a range”.  

![[List-from-a-range.png]]

All the observations will be [concatenated](https://www.howtogeek.com/447559/how-to-concatenate-data-from-multiple-cells-in-google-sheets/) in one cell:

`=CONCATENATE(B4," ",C4," ",D4," ",E4," ",F4," ",G4," ",H4," ",I4," ",J4," ",K4)`  

![[concatenate.png]]

## Attendance  
Imagine you are out of school with your students (when the pandemic’s over of course). You want to make the roll call quite quickly so you don’t want or can’t launch Pronote. But you can share the sheet with the vie scolaire. Very handy during a fire drill.

![[appel.gif]]

All you have to do is create [checkboxes](https://www.benlcollins.com/spreadsheets/google-sheets-checkbox/) (by the way, have a look at the last possibility at the end of the article. Very interesting).

So, go to `Insert > Checkbox`.

When the checkbox is unticked, it is `FALSE`. When ticked, it’s `TRUE`. Use `Conditional Formatting` to make them green or red (or whatever color you want) if a student is missing or not.

![[custom-formula.png]]
In “Format rules”, choose “Custom formula is” and type (for instance) `= $B2:B30 = TRUE` or `= $B2:B30 = FALSE`). Then choose the colour.

You can add a “Filter view” so you can display only the students missing.

![[filter-view-appel.gif]]

To create a [filter](https://support.google.com/docs/answer/3540681?co=GENIE.Platform%3DDesktop&hl=en), head to `Data > Create a filter`.  

## Special needs
Like I said at the beginning of this article, I want everything to be in one place. So I used the `IMPORTRANGE` function to import on my spreadsheet the content of another spreadsheet.

![[import-range.png]]
You won’t find it on this spreadsheet but lately, I added several tabs using the `IMPORTRANGE` function to gather information provided by my students (they have their own spreadsheet where they say what they are doing). It’s a long story to explain but if you read French you can [learn more about that by reading this article](https://www.ralentirtravaux.com/le_blog/comment-differencier-lenseignement-a-partir-dun-simple-spreadsheet/) or [this presentation](https://docs.google.com/presentation/d/11agHcVnziXGjI560aEOAdo7pG8ytQxs2Ue7PGui6Fuk/edit#slide=id.gdedf640b69_1_32).

![[slide.png]]
For now, you just need to know that you can monitor the progress of your students quite easily: they can tell you what exercise they’ve done, if they need help or if they can move on to the next step and why not? ask for an assessment. This is all about autonomous work so everyone is working at its own pace.

![[grammaire.jpg]]

To know more about this function, please refer to [Google's documentation](https://support.google.com/docs/answer/3093340?hl=en). It looks like this: 

`=IMPORTRANGE("https://docs.google.com/spreadsheets/d/abcd123abcd123", "sheet1!A1:C10")`

You just specify the URL of the spreadsheet and say where is the data you want to import (on which sheet, which rows).

## Seating plan
My colleague Jean showed me this nice trick. Using the `INDEX`/`MATCH` functions, you can create a seating plan. Very handy when you want to place students randomly and mix them up a little.

![[plan.gif]]

This may surprise you, but to do that you need three sheets.

1.  On the first one (the sheet is labelled “Liste”), you will find a list of your students. For each student, a random number is allocated. Using Filters, you can change the order of the names so they are mixed up. To assign a random number use this function: `=RAND()` (it returns a random number between 0 inclusive and 1 exclusive).
    
2.  On the second one (“Tables”), you have a simple sitting plan with only numbers.
    
	![[seating-plan.png]]
3.  Finally, on the third one (“Plan”), you have the same sitting plan but (and this is where the magic happens) but instead of numbers, you have a function using [INDEX](https://support.google.com/docs/answer/3098242?hl=en-GB) and [MATCH](https://support.google.com/docs/answer/3093378?hl=en-GB). It places random students!
    
	![[index-match.png]]
So the function is: `=INDEX(Liste!$B$2:$B$30,MATCH(Tables!F5,Liste!$A$2:$A$30))`

What it does is simply using two functions in one: `INDEX` then `MATCH`.

`INDEX` returns the content of a cell specified by row and column offset.

`MATCH` returns the relative position of an item in a range that matches a specified value (see [How to Use INDEX and MATCH together](https://youtu.be/ypCtiDmnqcE)).  

Since we only need the list of the students and the sitting plan, we hide the second tab (the one named “Tables”). To hide a sheet, follow these steps:

![[hide.gif]]

## Create groups 
Following the same method as mentioned above, you can create groups of 2 to 6 students.

![[groups.gif]]

Therefore, we have three sheets:

![[groupe.png]]

![[groupe1.png]]
![[groupe2.png]]
But, as I was able to put everything I needed on one sheet, I chose to hide the two others. Indeed, there is enough room to display everything we need on one single sheet. With an `IF` function (if I select the number 3 to create groups of 3 students), I can display the automatically generated groups on one of the hidden spreadsheets. To import the content of another sheet, I used [ARRAYFORMULA](https://www.youtube.com/watch?v=iGvvK8O5BpQ).

Remember that `IMPORT RANGE` can fetch data located on another spreadsheet. `ARRAYFORMULA` can bring over data that are on another sheet (keep in mind that a spreadsheet has multiple sheets or tabs).

## Pick a student randomly
![[choix.gif]]

Following [this tutorial](https://infoinspired.com/google-docs/spreadsheet/pick-a-random-name-from-a-long-list-in-google-sheets/), I was able to create this random picker with three functions. I wanted to insert an animated gif but alas it does not work.

The three functions are:

1.  `RANDBETWEEN`
2.  `COUNTA`
3.  `INDEX`

You already know `INDEX`. So there is `COUNTA` which counts all values in a data set, including those which appear more than once and text values (including zero-length strings and whitespace). To count unique values, use `COUNTUNIQUE`. To count only numeric values use `COUNT`.

And there is `RANDBETWEEN` (`=RANDBETWEEN()`). It generates a random number. 

We saw that `RAND` returns a random number between 0 and 1. `RANDBETWEEN` returns a number between 1 and whatever you want (read [How to Use RAND and RANDBETWEEN Functions in Google Sheets](https://infoinspired.com/google-docs/spreadsheet/rand-and-randbetween-functions-in-google-sheets/) to learn more about that).

To know how to combine these functions to create your name picker, have a look at the aforementioned tutorial.

## Conclusion
I’m not a spreadsheet specialist and I’m pretty sure you must have plenty of ideas of what we could do with a spreadsheet to not only track students' progress but to assess them as accurately as possible and help them become autonomous students as well.

You have probably noticed that there is no script at all in this spreadsheet. That’s because I’m terrible at Google Script but that’s also because I wanted this file to be as light and fast as possible. But, again, maybe you’ll have skills and ideas that I don’t. So I can’t wait to read your suggestions.

On top of that, keep in mind we can automate things using [Zapier](https://zapier.com) for instance. I don’t have a subscription so I can’t really use it but as I played with it, I was able to see the potential (for instance, if I take attendance, send automatically an email to the school so they know everyone is here during our little trip in town).

Again, let me know what you think!