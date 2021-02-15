---
title: Свойство TableDef.SourceTableName (DAO)
TOCTitle: SourceTableName Property
ms:assetid: 3c02f5f6-70ae-39ec-0984-8d6b81992418
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192675(v=office.15)
ms:contentKeyID: 48544300
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052901
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: bd2610e728d97d3a9fc2f6359a42fd3cdccb11e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314261"
---
# <a name="tabledefsourcetablename-property-dao"></a>Свойство TableDef.SourceTableName (DAO)


**Область применения**: Access 2013, Office 2013 

Задает или возвращает значение, которое указывает имя связанной таблицы или имя базовой таблицы (только для рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение .* SourceTableName

*выражение*: переменная, представляющая объект **TableDef**.

## <a name="remarks"></a>Комментарии

Этот параметр свойства доступно только для чтения для базовой таблицы и для чтения и записи для связанной таблицы или объекта, не подключенного к коллекции. Для базовой таблицы значением является строка нулевой длины ("").

## <a name="example"></a>Пример

В этом примере свойства **Connect** и **SourceTableName** используются для привязки различных внешних таблиц к базе данных Microsoft Access. Процедура ConnectOutput необходима для запуска этой процедуры.

```vb 
Sub ConnectX() 
 
 Dim dbsTemp As Database 
 Dim strMenu As String 
 Dim strInput As String 
 
 ' Open a Microsoft Access database to which you will link 
 ' a table. 
 Set dbsTemp = OpenDatabase("DB1.mdb") 
 
 ' Build menu text. 
 strMenu = "Enter number for data source:" & vbCr 
 strMenu = strMenu & _ 
 " 1. Microsoft Access database" & vbCr 
 strMenu = strMenu & _ 
 " 2. Microsoft FoxPro 3.0 table" & vbCr 
 strMenu = strMenu & _ 
 " 3. dBASE table" & vbCr 
 strMenu = strMenu & _ 
 " 4. Paradox table" & vbCr 
 strMenu = strMenu & _ 
 " M. (see choices 5-9)" 
 
 ' Get user's choice. 
 strInput = InputBox(strMenu) 
 
 If UCase(strInput) = "M" Then 
 
 ' Build menu text. 
 strMenu = "Enter number for data source:" & vbCr 
 strMenu = strMenu & _ 
 " 5. Microsoft Excel spreadsheet" & vbCr 
 strMenu = strMenu & _ 
 " 6. Lotus spreadsheet" & vbCr 
 strMenu = strMenu & _ 
 " 7. Comma-delimited text (CSV)" & vbCr 
 strMenu = strMenu & _ 
 " 8. HTML table" & vbCr 
 strMenu = strMenu & _ 
 " 9. Microsoft Exchange folder" 
 
 ' Get user's choice. 
 strInput = InputBox(strMenu) 
 
 End If 
 
 ' Call the ConnectOutput procedure. The third argument 
 ' will be used as the Connect string, and the fourth 
 ' argument will be used as the SourceTableName. 
 Select Case Val(strInput) 
 Case 1 
 ConnectOutput dbsTemp, _ 
 "AccessTable", _ 
 ";DATABASE=C:\My Documents\Northwind.mdb", _ 
 "Employees" 
 Case 2 
 ConnectOutput dbsTemp, _ 
 "FoxProTable", _ 
 "FoxPro 3.0;DATABASE=C:\FoxPro30\Samples", _ 
 "Q1Sales" 
 Case 3 
 ConnectOutput dbsTemp, _ 
 "dBASETable", _ 
 "dBase IV;DATABASE=C:\dBASE\Samples", _ 
 "Accounts" 
 Case 4 
 ConnectOutput dbsTemp, _ 
 "ParadoxTable", _ 
 "Paradox 3.X;DATABASE=C:\Paradox\Samples", _ 
 "Accounts" 
 Case 5 
 ConnectOutput dbsTemp, _ 
 "ExcelTable", _ 
 "Excel 5.0;" & _ 
 "DATABASE=C:\Excel\Samples\Q1Sales.xls", _ 
 "January Sales" 
 Case 6 
 ConnectOutput dbsTemp, _ 
 "LotusTable", _ 
 "Lotus WK3;" & _ 
 "DATABASE=C:\Lotus\Samples\Sales.xls", _ 
 "THIRDQTR" 
 Case 7 
 ConnectOutput dbsTemp, _ 
 "CSVTable", _ 
 "Text;DATABASE=C:\Samples", _ 
 "Sample.txt" 
 Case 8 
 ConnectOutput dbsTemp, _ 
 "HTMLTable", _ 
 "HTML Import;DATABASE=https://" & _ 
 "www.server1.com/samples/page1.html", _ 
 "Q1SalesData" 
 Case 9 
 ConnectOutput dbsTemp, _ 
 "ExchangeTable", _ 
 "Exchange 4.0;MAPILEVEL=" & _ 
 "Mailbox - Michelle Wortman (Exchange)" & _ 
 "|People\Important;", _ 
 "Jerry Wheeler" 
 End Select 
 
 dbsTemp.Close 
 
End Sub 
 
Sub ConnectOutput(dbsTemp As Database, _ 
 strTable As String, strConnect As String, _ 
 strSourceTable As String) 
 
 Dim tdfLinked As TableDef 
 Dim rstLinked As Recordset 
 Dim intTemp As Integer 
 
 ' Create a new TableDef, set its Connect and 
 ' SourceTableName properties based on the passed 
 ' arguments, and append it to the TableDefs collection. 
 Set tdfLinked = dbsTemp.CreateTableDef(strTable) 
 
 tdfLinked.Connect = strConnect 
 tdfLinked.SourceTableName = strSourceTable 
 dbsTemp.TableDefs.Append tdfLinked 
 
 Set rstLinked = dbsTemp.OpenRecordset(strTable) 
 
 Debug.Print "Data from linked table:" 
 
 ' Display the first three records of the linked table. 
 intTemp = 1 
 With rstLinked 
 Do While Not .EOF And intTemp <= 3 
 Debug.Print , .Fields(0), .Fields(1) 
 intTemp = intTemp + 1 
 .MoveNext 
 Loop 
 If Not .EOF Then Debug.Print , "[additional records]" 
 .Close 
 End With 
 
 ' Delete the linked table because this is a demonstration. 
 dbsTemp.TableDefs.Delete strTable 
 
End Sub 
 
```

