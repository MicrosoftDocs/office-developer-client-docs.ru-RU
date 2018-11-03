---
title: Описание PARAMETERS (Microsoft Access SQL)
TOCTitle: PARAMETERS declaration (Microsoft Access SQL)
ms:assetid: 0dcaad68-6a5f-93dc-e62a-b82b36e1e69c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845220(v=office.15)
ms:contentKeyID: 48543230
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277577
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e906e90fd6f7bf6e26898ed5381ef687c2ee8514
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937345"
---
# <a name="parameters-declaration-microsoft-access-sql"></a>Описание PARAMETERS (Microsoft Access SQL)


**Применимо к**: Access 2013, Office 2013

Объявляет имя и тип данных для каждого параметра в запросе с параметрами.

## <a name="syntax"></a>Синтаксис

Параметры *типа данных имя* \[, *тип данных имя* \[,...\]\]

Описание PARAMETERS состоит из следующих частей:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Часть</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>name</em></p></td>
<td><p>Имя параметра. Назначается свойство <strong>Name</strong> объекта <strong>параметра</strong> и используется для идентификации этого параметра в коллекции <strong>параметров</strong> . Можно использовать <em>имя</em> как строка, которая отображается в диалоговом окне во время запроса приложением. Используйте скобки ([]), чтобы заключить текст, который содержит пробелов и знаков препинания. Например, [Низкая цена] и [приступить к отчет с какой month?] — допустимое <em>имя</em> аргументов.</p></td>
</tr>
<tr class="even">
<td><p><em>Тип данных</em></p></td>
<td><p>Одна из основных <a href="sql-data-types.md">типов данных Microsoft Access SQL</a> или их синонимы.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Для запросов, на которых выполняется регулярно можно использовать параметры объявления для создания запроса с параметрами. Параметр запроса может помочь автоматизировать процесс изменения условия запроса. С помощью параметра запроса кода потребуется для предоставления параметров при каждом выполнении запроса.

Описание PARAMETERS обязательно предшествует любой другой инструкции, включая [Выбор](select-statement-microsoft-access-sql.md).

Если объявление включает несколько параметров, разделяйте их запятыми. Следующий пример включает в себя два параметра:

```sql
PARAMETERS [Low price] Currency, [Beginning date] DateTime;
```

*Имя* , но не *тип данных* можно использовать в предложении [ГДЕ](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) или [HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\)) . В следующем примере описаны два параметра предоставляемую и применено условие в записи в таблице Orders:

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a>Пример

В этом примере пользователю требуется укажите название задания, а затем использует данной должности как критерии для запроса.

Он вызывает процедуру EnumFields, которые можно найти в примере [оператор SELECT](select-statement-microsoft-access-sql.md) .

```vb
    Sub ParametersX() 
     
        Dim dbs As Database, qdf As QueryDef 
        Dim rst As Recordset 
        Dim strSql As String, strParm As String 
        Dim strMessage As String 
        Dim intCommand As Integer 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("NorthWind.mdb") 
         
        ' Define the parameters clause. 
        strParm = "PARAMETERS [Employee Title] CHAR; " 
     
        ' Define an SQL statement with the parameters 
        ' clause. 
        strSql = strParm & "SELECT LastName, FirstName, " _ 
            & "EmployeeID " _ 
            & "FROM Employees " _ 
            & "WHERE Title =[Employee Title];" 
         
        ' Create a QueryDef object based on the  
        ' SQL statement. 
        Set qdf = dbs.CreateQueryDef _ 
            ("Find Employees", strSql) 
         
        Do While True 
            strMessage = "Find Employees by Job " _ 
                & "title:" & Chr(13) _ 
                & "  Choose Job Title:" & Chr(13) _ 
                & "   1 - Sales Manager" & Chr(13) _ 
                & "   2 - Sales Representative" & Chr(13) _ 
                & "   3 - Inside Sales Coordinator" 
             
            intCommand = Val(InputBox(strMessage)) 
             
            Select Case intCommand 
                Case 1 
                    qdf("Employee Title") = _ 
                        "Sales Manager" 
                Case 2 
                    qdf("Employee Title") = _ 
                        "Sales Representative" 
                Case 3 
                    qdf("Employee Title") = _ 
                        "Inside Sales Coordinator" 
                Case Else 
                    Exit Do 
            End Select 
             
            ' Create a temporary snapshot-type Recordset. 
            Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
            ' Populate the Recordset. 
            rst.MoveLast 
                 
            ' Call EnumFields to print the contents of the  
            ' Recordset. Pass the Recordset object and desired 
            ' field width. 
            EnumFields rst, 12 
     
        Loop 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "Find Employees" 
         
        dbs.Close 
     
    End Sub
```
