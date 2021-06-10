---
title: Свойство QueryDef.MaxRecords (DAO)
TOCTitle: MaxRecords Property
ms:assetid: 7492cde9-be30-3473-dabc-9602465910d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195877(v=office.15)
ms:contentKeyID: 48545664
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053583
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6738762ba18289293c67392d47e278066ead071d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301080"
---
# <a name="querydefmaxrecords-property-dao"></a>Свойство QueryDef.MaxRecords (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает максимальное количество записей, возвращаемых из запроса к источнику данных ODBC.

## <a name="syntax"></a>Синтаксис

*выражения* . MaxRecords

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Примечания

Значение по умолчанию — 0, что не указывает ограничения на количество возвращенных записей.

После того, как количество строк, заданных **MaxRecords,** будет возвращено вашему приложению в **[Recordset,](recordset-object-dao.md)** процессор запроса прекратит возвращать дополнительные записи, даже если больше записей будут иметь право на включение в **Набор записей.** Это свойство полезно в ситуациях, когда ограниченные клиентские ресурсы запрещают управление большим количеством записей.

> [!NOTE]
> Свойство **MaxRecords** можно использовать только с источником данных ODBC.

## <a name="example"></a>Пример

В этом примере свойство **MaxRecords** использует, чтобы установить ограничение на количество записей, возвращаемой запросом в источнике данных ODBC.

```vb 
Sub MaxRecordsX() 
 
 Dim dbsCurrent As Database 
 Dim qdfPassThrough As QueryDef 
 Dim qdfLocal As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Open a database from which QueryDef objects can be 
 ' created. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a pass-through query to retrieve data from 
 ' a Microsoft SQL Server database. 
 Set qdfPassThrough = _ 
 dbsCurrent.CreateQueryDef("") 
 
 ' Set the properties of the new query, limiting the 
 ' number of returnable records to 20. 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfPassThrough.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfPassThrough.SQL = "SELECT * FROM titles" 
 qdfPassThrough.ReturnsRecords = True 
 qdfPassThrough.MaxRecords = 20 
 
 Set rstTemp = qdfPassThrough.OpenRecordset() 
 
 ' Display results of query. 
 Debug.Print "Query results:" 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 dbsCurrent.Close 
 
End Sub 
 
```

