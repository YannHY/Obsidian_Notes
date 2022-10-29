---
tags: [Documentation, Google, sheets, formula]
author: [Yann Houry]
date: [03-10-2021]
---

```ad-seealso
title: Voir aussi
collapse: open

- [[Sheets Formula#IF]]
- [[Sheets Formula#Nested IF Statements]]
- [[Sheets Formula#Using IF with AND and OR]]
- [[Sheets Formula#COUNTIF]]
- [[Sheets Formula#COUNTA]]
- [[Sheets Formula#SUMIF]]
- [[Sheets Formula#Date]]
- [[Sheets Formula#Sparkline]]
- [[Sheets Formula#VLOOKUP]]
- [[Sheets Formula#UNIQUE]]
- [[Sheets Formula#SORT]]
- [[Sheets Formula#FILTER]]
- [[Sheets Formula#Chart & Graph]]
- [[Sheets Formula#Concatenate]]
- [[Sheets Formula#SPLIT]]
- [[Sheets Formula#Query]]
- [[Sheets Formula#QR Code Generator]]
- [[Sheets Formula#IMPORTFEED]]
- [[Sheets Formula#Google Translate]]
- [[Sheets Formula#Match Index]]
- [[Sheets Formula#IMPORTRANGE]]
- [[Sheets Formula#Pivot tables]]
- [[Sheets Formula#Automatically create email addresses]]
- [[Sheets Formula#Remove Characters]]
- [[Sheets Formula#Checkboxes]]
```

##  IF
➝ [Documentation Google](https://support.google.com/docs/answer/3093364?hl=en)

````
=IF(test, value_if_true, value_if_false)
````

### Exemple ````

````
=IF(B4=“Suit”,1, 0)
````

➝ [How to Use the Google Sheets IF Function](https://www.howtogeek.com/449861/how-to-use-the-google-sheets-if-function/):

> If you want to run a logical test in a Google Sheets formula, providing different results whether the test is **TRUE** or **FALSE**, you’ll need to use the IF function. Here’s how to use it in Google Sheets.  
> As the name suggests, IF is used to test whether a single cell or range of cells meets certain criteria in a logical test, where the result is always either TRUE or FALSE.  
> If the IF test is TRUE, then Google Sheets will return a **number** or **text string**, **perform a calculation**, or **run through another formula**.  
> If the result is FALSE, it’ll do something completely different. You can **combine IF with other logical functions like AND and OR** or with other **nested IF** statements.  

### Créer des menus conditionnels
Dans le but de sélectionner des [[Compétences]]

- [How to Create a Dependent Drop Down List in Google Sheets](https://productivityspot.com/dependent-drop-list-google-sheets/)
- [LISTE DÉROULANTE CONDITIONNELLE SOUS GOOGLE SHEET](https://mychromebook.fr/liste-deroulante-conditionnelle-sous-google-sheet/)

## Nested IF Statements
````
=IF(first_test, value_if_true, IF(second_test, value_if_true, value_if_false))
````
 
````
=IF(first_test, IF(second_test, value_if_true, value_if_false), value_if_false)
````

````
=IF(B4=“très bonne participation”, 2, 
     IF(B4=“bonne participation”, 1, 
        IF(B4=“suit mais ne participe pas”, 0.5, 0
          )
       )
    )
````
 
## Using IF with AND and OR
To use IF AND, type
````
=IF(AND(AND Argument 1, AND Argument 2), value_if_true, value_if_false)
````

To use IF OR
````
=IF(OR(OR Argument 1, OR Argument 2), value_if_true, value_if_false)
````

## COUNTIF
➝ [Documentation Google](https://support.google.com/docs/answer/3093480)

`COUNTIF(A1:A10,”coffee”)`  (ne compte que les cafés et donne donc le nombre de fois que le mot apparait).

## COUNTA
➝ [Documentation Google]([](https://support.google.com/docs/answer/3093991?hl=en))



## SUMIF
➝ [Documentation Google](https://support.google.com/docs/answer/3093583)

`SUMIF(A1:A10,’coffee’,B1:B10)`  (dans la colonne A1 à A10, on veut additionner uniquement le coût des cafés (et pas par exemple des chocolats ou des thés) qui apparaissent dans B1 à B10)

## Date
You can insert the date in many ways:  
-   To insert the date, press `cmd or ctrl + ;`  (be sure to go to `Help > Keyboard shortcuts` and activate `Enable compatible spreadsheet shortcuts`).
-   To display a time or a date (which will be automatically updated every day), use the functions `=NOW()` or `=DATE()`. To format the date, head to `Format > Number > Date`.
 
More on that in [How to Add the Current Date and Time in Google Sheets](https://www.howtogeek.com/448444/how-to-add-the-current-date-and-time-in-google-sheets/).

Voir aussi `TIME()`

## Sparkline
Sparklines are small, lightweight charts that exist inside a single cell: 
````
=SPARKLINE(B3:M3)
````

````
=SPARKLINE($B50:$M50,{"charttype","bar";"max",AVERAGE(B50:M50);"color1","#3C8CD6";"color2","#F0EEEE"})
````
( to display a progress bar)

- [How to Use Sparklines in Google Sheets](https://www.howtogeek.com/450155/how-to-use-sparklines-in-google-sheets/)
- [Everything you ever wanted to know about Sparklines in Google Sheets](https://www.benlcollins.com/spreadsheets/sparklines-in-google-sheets/))

## VLOOKUP
Extracts data from cell in specified column, using specified search key: 
````
=VLOOKUP($A50, $A3:$M31, 2, false)
```` 

- [How to Use VLOOKUP in Google Sheets](https://www.youtube.com/watch?v=_yKn70cl-Mo)
- [How to Find Data in Google Sheets with VLOOKUP](https://www.howtogeek.com/447024/how-to-find-data-in-google-sheets-with-vlookup/)

## UNIQUE
➝ [Documentation Google](https://support.google.com/docs/answer/3093198)

## SORT
➝ [Documentation Google](https://support.google.com/docs/answer/3093150)

````
=SORT(A3:B31,B3:B31, True)
````
(on sélectionne les data, et dans ces data, on sélectionne la partie que l’on veut classer par ordre croissant (false) ou décroissant (true).

## FILTER
➝ [FILTER](https://support.google.com/docs/answer/3093197)

````
=FILTER(A3:B31,B3:B31<10)
````
(n’affiche que les notes inférieures à 10 dans la colonne B3 à B31)

Jeter un œil sur les autres possibilités (en particulier `ISBLANK`) :

````
=FILTER(A2:C6, ISBLANK(C2:C6))
````

````
=FILTER(A2:C6,B2:B6 = 2)
````

````
=FILTER(A2:C6, B2:B6>2, B2:B6<4)
````

````
=FILTER(A2:C6, NOT(ISBLANK(C2:C6)))
````

A LIRE [Using the FILTER function in Google Sheets (Single or multiple conditions)](https://www.spreadsheetclass.com/google-sheets-filter-function/)

## Chart & Graph
➝ [Add & edit a chart or graph](https://support.google.com/docs/answer/63824?visit_id=637495177398946366-414543288&rd=1)
- [Charts](https://www.youtube.com/playlist?list=PLv9Pf9aNgemsnwb2uNnVsTOzCJZudPUOD)
- [Watch one of these videos on YouTube](https://www.youtube.com/playlist?list=PLv9Pf9aNgemsnwb2uNnVsTOzCJZudPUOD).

## Concatenate
[Concatenate data from multiple cells](https://www.howtogeek.com/447559/how-to-concatenate-data-from-multiple-cells-in-google-sheets/)

````
=CONCATENATE(B4," ",C4," ",D4," ",E4," ",F4," ",G4," ",H4," ",I4," ",J4," ",K4)
````  

## SPLIT
- [Split function](https://www.benlcollins.com/spreadsheets/split-function/) -> `=SPLIT(A1,", ")`
- [Google Sheets: Split Up Student Names](https://alicekeeler.com/2021/07/03/google-sheets-split-up-student-names/)

## Query
- [QUERY](https://support.google.com/docs/answer/3093343?hl=fr)

`QUERY(data, query, headers)`

- `data`: The range of cells to perform the query on.
- `query`: The query to perform (must either be enclosed in quotation marks)
- `headers` (OPTIONAL): The number of header rows at the top of `data`. If omitted or set to `-1`, the value is guessed based on the content of `data`.

Example :
`QUERY('Sheet1'!A2:AH,"select A,C,D,E, 1)`

- [Google Sheets Query function: The Most Powerful Function in Google Sheets](https://www.benlcollins.com/spreadsheets/google-sheets-query-sql/)
- [How to Use the QUERY Function in Google Sheets](https://www.howtogeek.com/450465/how-to-use-the-query-function-in-google-sheets/)

<iframe width="560" height="315" src="https://www.youtube.com/embed/iWi3nL5MPK4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

````
=QUERY('Sheet1'!A2:AH,"SELECT *",1)
````

`SELECT *` retrieves all of the columns from the table.

### Where Clause

````
=QUERY('Sheet1'!A1:D20,"SELECT B, D WHERE D > 100",1)
````

➝ In Sheet1 (A1:20), select columns B and D and only the value > 100.

## QR Code Generator
![[QR-Code-Generator.jpeg | 500]]

## IMPORTFEED
````
=IMPORTFEED(A2, "items", FALSE, 10)
````

## Google Translate
````
=GoogleTranslate(C2, "fr", "en")
````

## Match Index
- [Match Index](https://youtu.be/9sLWDjAEuyc)
- [INDEX](https://support.google.com/docs/answer/3098242?hl=en-GB)
- [MATCH](https://support.google.com/docs/answer/3093378?hl=en-GB)

In [[Tracking Students’ Progress]], the function is: ````
````
=INDEX(Liste!$B$2:$B$30,MATCH(Tables!F5,Liste!$A$2:$A$30))
````

What it does is simply using two functions in one: `INDEX` then `MATCH`.

- `INDEX` returns the content of a cell specified by row and column offset.
- `MATCH` returns the relative position of an item in a range that matches a specified value (see [How to Use INDEX and MATCH together](https://youtu.be/ypCtiDmnqcE)).  

## IMPORTRANGE
Avec numéro de cellules qui peuvent changer
[importrange when copied to other cells automatically change range](https://webapps.stackexchange.com/questions/130946/importrange-when-copied-to-other-cells-automatically-change-range)
````
=IMPORTRANGE($A$2, "Sheet1!E"&ROW(E4))
````

````
=IMPORTRANGE("https://docs.google.com/spreadsheets/d/abcd123abcd123", "sheet1!A1:C10")
````

- [Fonction IMPORTRANGE](https://support.google.com/docs/answer/3093340?hl=en)

## Pivot tables
➝ [Create & use pivot tables](https://support.google.com/docs/answer/1272900?visit_id=637495177398946366-414543288&rd=1)
➝ [Google Sheets Pivot Tables - Basic Tutorial](https://www.youtube.com/watch?v=Tty0RyD1KLw)

## Automatically create email addresses
Vu sur [Dice Rolls and Normal Distributions in Google Sheets](https://youtu.be/NVA7WIF94VE?t=639)

<iframe width="560" height="315" src="https://www.youtube.com/embed/NVA7WIF94VE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- [List of Random Names](http://listofrandomnames.com)
- Data > Split text to columns 
- =left(A1)&B1&”@lyceechurchill.london”
- =LOWER(left(A1)&B1&”@lyceechurchill.london”) (en utilisant la formule [LOWER](https://www.spreadsheetclass.com/make-text-lowercase-in-google-sheets-with-the-lower-function/))

### Créer des adresses emails automatiquement
Pour ce faire, j'ai généré aléatoirement une liste de noms. Je ne retrouve plus le site que j'ai utilisé, mais en cherchant un peu j'ai trouvé :

- [Name Generator](https://www.name-generator.org.uk/)
- [Random Name Generator](https://randomwordgenerator.com/name.php)
- [Random Name Generator (un autre)](http://random-name-generator.info/index.php?n=25&g=1&st=2)

Pour séparer les noms en deux colonnes, utiliser Data > Split text to columns (separator: space).

On obtient deux colonnes. Dans une troisième, on insère une formule comme `=LOWER(left(A1)&B1&"@lyceechurchill.london")`.

![[create-adresses.png | 700]]
Ça évite de les créer manuellement (notre modèle d'adresse était initiale du prénom + nom + @lyceechurchill.london).

## Remove Characters
Let's say we have a list of email addresses like user1234@g.lfis.edu.hk and you only want what's before the `@`, use:

````
=SUBSTITUTE(G2,"@g.lfis.edu.hk","")
````

Lire la suite très intéressante : [Google Sheets: remove the same text or certain characters from multiple cells at once](https://www.ablebits.com/office-addins-blog/2021/04/29/google-sheets-remove-text/) (notamment pour utiliser REGEXREPLACE)

Intéressant sur la manipulation du texte (dont les formules)
[How to rotate text in Google Sheets](https://www.spreadsheetclass.com/rotate-text-in-google-sheets/)

## Checkboxes
- [How to Count Checkboxes in Google Sheets](https://www.alphr.com/google-sheets-cout-checkboxes/)
- [How to Count Checkboxes in Google Sheets](https://www.howtogeek.com/794460/how-to-count-checkboxes-in-google-sheets/)

````
=COUNTIF(A2:A22, TRUE)
````

<hr />

```ad-seealso
title: Voir aussi
collapse: open

- [[Tracking Students’ Progress]]
- [[Sheets Documentation]]
- [[Dollar Sign]]
- [[Training Google Sheets]]
- [[Training Google Sheets 2]]
```
