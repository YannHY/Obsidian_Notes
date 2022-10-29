[Buttons Showcase - Share & showcase - Obsidian Forum](https://forum.obsidian.md/t/buttons-showcase/18044/2)

## Pin
```button
name Pin
type command
action Toggle pin
color yellow
```
^button-buttonpin

## New Note
```button
name New Note
type command
action Create new note
color green
```
^button-buttonnote

## Search
```button
name Search
type command
action Search current file
color blue
```
^button-buttonsearch

```button
name Show Explorer
type command
color blue
action Files: Show file explorer
```
^button-button-explorer

```button
name Search ALL Files
type command
action Search: Search in all files
color green
```
^button-Search-files

## Edit/Preview
Plus très utile

```button
name Edit/Preview
type command
action Toggle edit/preview mode
```
^button-buttonpreview

## Open
### Apps
```button
name GoodLinks Unread
type link
action goodlinks://x-callback-url/unread
color green
```

```button
name Matter Queue
type link
action matter://x-callback-url/
color blue
```

### Files
```button
name Documentation
type link
action obsidian://open?vault=Main%20Vault&file=Documentation%2FDocumentation%20TOC
color yellow
```
^button-open-documentation

```button
name Daily Notes
type link
action obsidian://open?vault=Main%20Vault&file=Daily%20Notes%2FTOC
color green
```
^button-open-daily-notes

```button
name FIS
type link
action obsidian://open?vault=Main%20Vault&file=Lycee%2FDashboard
color red
```
^button-open-fis

```button
name Books
type link
action obsidian://open?vault=Main%20Vault&file=Books%2FTable%20of%20Contents
color blue
```
^button-open-books

```button
name Écriture
type link
action obsidian://open?vault=Main%20Vault&file=%C3%89criture%2FTOC
color red
```
^button-open-ecriture

```button
name ➝ Go Back To Dashboard
type link
action obsidian://open?vault=Main%20Vault&file=Dashboard
color red 
```
^button-open-dashboard

## Insérer un lien
```button
name Blog
type link
action https://www.ralentirtravaux.com/le_blog/
```
^button-buttonblog

## Lancer une commande
```button
name Export Docx
type command
action Pandoc Plugin: Export as Word Document (docx)
```
^button-buttonword

## Books
```button
name Books
type link
action obsidian://open?vault=Books&file=Dashboard
```
^button-books

## Cours
```button
name Cours
type link
action obsidian://open?vault=Cours&file=Dashboard
```
^button-cours

## Personnel
```button
name Personnel
type link
action obsidian://open?vault=Personnel&file=Dashboard
```
^button-personnel

## Lycée
```button
name Lycee
type link
action obsidian://open?vault=Lycee&file=Dashboard
```
^button-lycee

## Help
```button
name Help
type link
action obsidian://open?vault=Obsidian%20Help&file=Start%20here
```
^button-help

<hr />

## Insert code

```js
var John = {
	name: 'John\'s family',
	bills: [124, 48, 268, 180, 42],
	calcTips: function() {
		this.tips = [];
		this.finalValues = [];
		for (var i = 0; i < this.bills.length; i++)
		{
			var percentage;
			var bill = this.bills[i];
			if (bill < 50) {percentage = .2;
		}
			else if (bill >= 50 && bill < 200) {percentage = .15;
		}
			else {percentage = .1;}
		this.tips[i] = bill * percentage;
		this.finalValues[i] = bill + bill * percentage;
		}
	}
}	
John.calcTips();
console.log(John);
```


