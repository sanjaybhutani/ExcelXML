# ExcelXML
**Convert a Table or a Grid control into a Microsoft Excel XML Spreadsheet file.**

Original author: Rodrigo Bruscain

The ExcelXML project is designed to bring to the Visual FoxPro the possibility to generate a Excel file converting 99% of all visual caracteristics from a Grid. However, there is the possibility to generate a file without a Grid.

## Goals
* Excel files with over 65,535 rows
* No limit size (it depends on the Operating System)
* Convert a Grid Control into a Excel XML file considering 99% of the visual characteristics
* It is possible to use Grid Dynamics properties
* Based in all Grid visual properties
* It is possible to convert a table without a Grid Control as well
* Easy to implement and it is not necessary to change your code
* Compatible with Microsoft Excel 2003 or higher
* The files can be opened by OpenOffice reducing conversion errors
* Open the file by Excel and save in other formats to reduce the size without losing information
* It is not necessary to have Microsoft Excel installed

**Release version 1.08**  
NEW - Document author included as username or computername.  
FIX - Field Date and DateTime with the year lower than 1900 will be forced to 1900. This is necessary because the lower allowed year in a cell of Excel is 1900  
FIX - Automatic column width for fields type char bigger that 190 columns

**Release version 1.07**  
FIX - Data with the characters "<" or ">" are replaced for {""[" and "](_-and-_)""} in order to avoid data conflict during the conversion.
FIX - Alias error when the property   "RecordSourceType" in the Grid control is diferent than 1.  
FIX - Included samples with no progressbar in order to avoid the error ole 0x80040154. This error happens only in some machines that the ActiveX ProgressBar doesn't exists.

**Release version 1.06**  
FIX - SET COLLATE TO controled at run-time to avoid the error "Invalid Key Length"

**Release version 1.05**  
FIX - Column data type Date and DateTime when converted has wrong format.  
FIX - Column data type DateTime is not considered the time in current value field.

**Release version 1.04**  
FIX - Sheet name cannot exceed 31 characters  
FIX - Sheet name cannot contain any of the following characteres:  {" : \ / ? * [  ](--)"}  
FIX - Sheet name cannot be blank. If is blank, will be changed to "Sheet1"

**Release version 1.03**  
FIX - Field Date/Datetime with NULL or EMPTY value builds a Excel file incorrectly.  
FIX - Index error when the index tag is too big.

| Properties and Methods | Description |  
| -----------------------|-------------|
|![](ExcelXML_property_vs.bmp) ColumnCount | Returns the number of columns included in the Excel file.|  
|![](ExcelXML_property_vs.bmp) File | Inform the name of Excel file. If you don't inform the name with the extension, the XML extension will be included. The default file name is "Book1"|  
|![](ExcelXML_property_vs.bmp) GridObject | Inform the Grid control object to convert a Grid control in an Excel XML file.|
|![](ExcelXML_property_vs.bmp) HasFilter | .T. Includes the option Filter in all columns in the generated file.|
|![](ExcelXML_property_vs.bmp) LockHeader | .T. locks the header in the generated file. This option in Excel is called by Freeze Top Row.|
|![](ExcelXML_property_vs.bmp) OpenAfterSaving | .T. to open the file after saving it.|
|![](ExcelXML_property_vs.bmp) RowCount | Returns the number of rows included in the Excel file.|
|![](ExcelXML_property_vs.bmp) SetStyles | .T. to define that the Excel file will have the Grid visual characteristics transported.|
|![](ExcelXML_property_vs.bmp) SheetName | Excel sheet name. The default name is "Sheet1"|
|![](ExcelXML_property_vs.bmp) xmlEncoding | XML encoding type used to set the code that defines special characters. Default code is "iso-8859-1".|
|![](ExcelXML_property_vs.bmp) Version | Object that contains the information about this class.|
|![](ExcelXML_method_vs.bmp) About|About ExcelXML class|
|![](ExcelXML_method_vs.bmp) Progress|Method used to show the percentage processed.|
|![](ExcelXML_method_vs.bmp) Save|Creates the Excel XML file.|

## Sample 01
![](ExcelXML_sample01.png)

![](ExcelXML_sample01_excel.png)

## Sample 02
![](ExcelXML_sample02.png)

![](ExcelXML_sample02_excel.png)

## Sample 03
![](ExcelXML_sample03.png)

![](ExcelXML_sample03_excel.png)

## Sample 04 - No Grid control
![](ExcelXML_sample04.png)

![](ExcelXML_sample04_excel.png)
