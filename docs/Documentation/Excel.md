# Excel
- [Workbook Link support coming to Excel for the web](https://techcommunity.microsoft.com/t5/excel-blog/workbook-link-support-coming-to-excel-for-the-web/ba-p/1590314)
- [How to Reference Another Sheet or Workbook in Excel (with Examples)](https://trumpexcel.com/reference-another-sheet-or-workbook-in-excel/)
- [How to create external reference in Excel to refer to another sheet or workbook](https://www.ablebits.com/office-addins-blog/2015/12/08/excel-reference-another-sheet-workbook/)
- [Create an external reference (link) to a cell range in another workbook](https://support.microsoft.com/en-us/office/create-an-external-reference-link-to-a-cell-range-in-another-workbook-c98d1803-dd75-4668-ac6a-d7cca2a9b95f#ID0EADAAA=Web) (peu utile)

Exemple pour un fichier ouvert en local. Si fichier fermé, placer le chemin (`\='C:\\Users\\sumit\\Desktop\\\[Example File.xlsx\]Sheet1'!$A$1`).

```
\='\[Example File.xlsx\]SalesData'!A1
````

```
='[Progression de grammaire (élève).xlsx]Sheet1'!B6
```

> In case there are spaces in the external workbook name or the sheet name (or both), then you need to add put the file name (in square brackets) and the sheet name in single quotes.

## Excel for the web

Data > Get External Data > From HTML > Online Locations

Choisir spreadsheet dans OneDrive.

Ca ouvre le fichier en ligne. Copier la cellule dont on veut récupérer les données puis aller :

dans Home > Paste > Paste Link

IMPORTANT : penser à retirer les $


```
='https://domain/folder/[workbookName.xlsx]sheetName'!CellOrRangeAddress
```

## Create a drop-down list

1.  Select the cells that you want to contain the **lists**.
2.  On the ribbon, click DATA > Data Validation.
3.  In the dialog, set Allow to **List**.
4.  Click in Source, type the text or numbers (separated by commas, for a comma-delimited **list**) that you want in your **drop**-**down list**, and click OK.

[Link](https://support.microsoft.com/en-us/office/video-create-and-manage-drop-down-lists-28db87b6-725f-49d7-9b29-ab4bc56cefc2)


https://lyceeinternationallondon-my.sharepoint.com/:x:/r/personal/yhoury_lyceeinternational_london/_layouts/15/Doc.aspx?sourcedoc=%7B3D56D2A1-928C-4DCA-A689-DB0F87EF17A3%7D&file=Progression%20de%20grammaire%20(élève).xlsx&action=default&mobileredirect=true&cid=47b4bef8-07b9-4701-8ca5-edbc7a13dcb0

https://lyceeinternationallondon-my.sharepoint.com/:x:/r/personal/yhoury_lyceeinternational_london/_layouts/15/Doc.aspx?sourcedoc=%7B12F22239-2013-4C9C-AACC-1FDC71FEE3E7%7D&file=Progression%20de%20grammaire%20(prof).xlsx&action=default&mobileredirect=true&cid=947b096f-2584-4a7e-9118-11d52a16e040

## Pivot tables

https://youtu.be/m0wI61ahfLc (Excel)
https://onedrive.live.com/view.aspx?resid=B09F9559F6A16B6C!65108&ithint=file%2cxlsx&authkey=!ABOLwNw_-anW0Yw

