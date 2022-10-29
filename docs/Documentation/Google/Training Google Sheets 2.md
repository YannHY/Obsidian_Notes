---
tags: [Documentation, Google, Sheets, training]
author: [Yann Houry]
date: 19-06-2022
---

[[Tracking Students’ Progress]]

## TRANSLATE
`=GoogleTranslate(C2, "fr", "en")`

## RANDBETWEEN
https://support.google.com/docs/answer/3093507?hl=en-GB

Exercices
https://docs.google.com/spreadsheets/d/1NjsrzCuju4JJ8pAslyu9zdJyx1psy3WRZ1958Uwqw7s/edit?pli=1#gid=0

### Syntax
`RANDBETWEEN(low, high)`

-   `low` – The low end of the random range.
-   `high` – The high end of the random range.

### Examples
- `RANDBETWEEN(1,10)`
- `RANDBETWEEN(A2,A3)`

Also see [Alice Keeler's blog](https://alicekeeler.com/2022/04/01/5-google-sheets-functions-to-know/):
> I personally use this a LOT. It allows me to generate random numbers for a variety of purposes. `=randbetween(1,30)` lets me choose a random student on my roster for example.

Add names to know whose student is selected.

### Exercice intéressant à faire: Random Name Picker
[How to Pick a Random Name from a Long List in Google Sheets](https://infoinspired.com/google-docs/spreadsheet/pick-a-random-name-from-a-long-list-in-google-sheets/) ou [How to Pick a Random Name from a Long List in Google Sheets](https://sheetaki.com/pick-a-random-name-from-a-long-list-in-google-sheets/)

#### COUNTA & RANDBETWEEN
- `COUNTA` to count the number of students (`=counta(A2:A)`).
- `RANDBETWEEN` to pick a random number between 1 and the total number of students (`RANDBETWEEN(1,30)`).

We can write the exact number of students if it is always the same. For instance, if there are always 30 names in our list, we can write this function in the following way:`RANDBETWEEN(1,30)`.

Or, if we don’t know the exact number of names or if it changes, we can use `COUNTA`.

In fact, we can combine `COUNTA` & `RANDBETWEEN` : `RANDBETWEEN(1,counta(A2:A))`

#### INDEX
The `INDEX` function returns the content of a cell, specified by row and column offset. The syntax of the `INDEX` function is as follows: `=INDEX(reference, row, column)`.

- `reference` means the range of cells where the values are located.
- `row` is an optional argument. It means the number of offset row(s) from the range.
- `column` is also an optional argument, it means the number of offset column from the range.

`=INDEX(A2:A, 10)` (returns a name in column A, row number 10)

#### INDEX & COUNTA & RANDBETWEEN
We'll finally use `INDEX` to match the randomly selected number with the corresponding name in the list:

`=index(A2:A,randbetween(1,counta(A2:A)))`

Jeter un œil sur [Google Sheets – Random Alphabetic, Random Alphanumeric and Random Alphanumeric + Character Custom Functions (Updated January 2022)](https://yagisanatode.com/2018/08/23/google-sheets-random-alphabetic-random-alphanumeric-and-random-alphanumeric-character-custom-functions/)

#### If Error
If A2:A is blank, then the random name picker formula would return an error. To avoid that, use the below formula which uses [IFERROR](https://infoinspired.com/google-docs/spreadsheet/google-sheets-iferror-function-usage-and-examples/) to return the string “No Name” in case of an error.

`=iferror(index(A2:A,randbetween(1,counta(A2:A))),"No Name!")`

#### If
If you want to set a trigger, use the following formula instead. The formula will only execute if the value in cell B3 is “Yes”.

`=if(P2="Yes",iferror(index(A2:A,randbetween(1,counta(A2:A))),"No Name!"),"")`


Use Data validation to create a drop-down menu (Yes/No)

## VLOOKUP
`=VLOOKUP($A50, $A3:$M31, 2, false)`


## Autre
Voir aussi
[How to Generate a List of Passwords in Google Sheets](https://infoinspired.com/google-docs/spreadsheet/generate-a-list-of-passwords-in-google-sheets/)