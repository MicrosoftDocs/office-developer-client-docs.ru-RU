---
title: Инструкция EXECUTE (Microsoft Access SQL)
TOCTitle: EXECUTE statement (Microsoft Access SQL)
ms:assetid: 9ec4d9ee-db2a-0319-3ccf-c035d67a1496
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198330(v=office.15)
ms:contentKeyID: 48546667
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277471
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a0fa90ac252e877c583982f4e9f900196a4674b3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879748"
---
# <a name="execute-statement-microsoft-access-sql"></a>Инструкция EXECUTE (Microsoft Access SQL)

**Применимо к**: Access 2013, Office 2013

Используется для вызова выполнения процедуры.

## <a name="syntax"></a>Синтаксис

ВЫПОЛНЕНИЕ *процедуры* \[ *param1*\[, *param2*\[,...\]\]

Инструкция EXECUTE состоит из следующих частей:

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
<td><p><em>процедура</em></p></td>
<td><p>Имя процедуры, который должен быть выполнен.</p></td>
</tr>
<tr class="even">
<td><p><em>param1 param2...</em></p></td>
<td><p>Значения для параметров, определенных в процедуре.</p></td>
</tr>
</tbody>
</table>


## <a name="example"></a>Пример

В этом примере имена запроса CategoryList и вызывает процедуру EnumFields, которые можно найти в примере инструкции SELECT.

```vb
    Sub ProcedureX() 
     
        Dim dbs As Database, rst As Recordset 
        Dim qdf As QueryDef, strSql As String 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        strSql = "PROCEDURE CategoryList; " _ 
            & "SELECT DISTINCTROW CategoryName, " _ 
            & "CategoryID FROM Categories " _ 
            & "ORDER BY CategoryName;" 
         
        ' Create a named QueryDef based on the SQL 
        ' statement. 
        Set qdf = dbs.CreateQueryDef("NewQry", strSql) 
     
        ' Create a temporary snapshot-type Recordset. 
        Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
        ' Populate the Recordset. 
        rst.MoveLast 
                 
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        Execute EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
