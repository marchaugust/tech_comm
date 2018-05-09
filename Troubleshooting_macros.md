# Troubleshooting Wrong Table Formats With Macros
When you generate a word document from RoboHelp and choose to map the existing template with a predefined word one, style mapping issues can occur. The most frequent issue is caused by table mapping. Macros allow you to automate the task of fixing all the table styles, without the need to scroll through the document and make changes to each table.

**Note:** The table style that you want to apply must be defined in the style sheet.

## Prerequisites
To run macros, you must first add the Developer tab to the ribbon. To add it, follow these steps:

1. Right click on the ribbon.
2. Select **Customize the ribbon**. The **Word Options** window opens.
3. Choose the **Developer** option from the list.

![developer](https://github.com/marchaugust/files/blob/master/developer.JPG)

4. Click Ok. You now have access to the **Developer** tab.

## Creating and running a macro
To create and run a macro, follow these steps:

1. Go to **Developer** and select **Macros**. A new dialog box opens.
2. Name your macro. For example, Tables.
3. Click Create. A Microsoft Visual Basic for Apps window opens.
4. Copy the following macro into the text editor:

```
   Sub ApplyTableStyle()
    For Each tbl In ActiveDocument.Tables
            tbl.Style = "PurpleTable1"
    Next
End Sub 
```
5. Click **Run Sub**.

![run_sub](https://github.com/marchaugust/files/blob/master/run_sub.JPG)

6. Click Save and close the Visual Basic window. The table style is now applied. 

