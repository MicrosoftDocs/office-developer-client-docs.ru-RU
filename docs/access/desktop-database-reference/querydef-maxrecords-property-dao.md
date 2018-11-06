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
ms.openlocfilehash: 0156983a455c72e4046424def188e41b94705087
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998230"
---
# <a name="querydefmaxrecords-property-dao"></a>Свойство QueryDef.MaxRecords (DAO)

**Применимо к**: Access 2013, Office 2013

Задает или возвращает максимальное число записей для возврата из запроса к источнику данных ODBC.

## <a name="syntax"></a>Синтаксис

*выражение* . MaxRecords

*выражение* Переменная, которая представляет собой объект- **QueryDef** .

## <a name="remarks"></a>Примечания

Значение по умолчанию равно 0, указывающее без ограничений на количество возвращаемых записей.

После возвращения максимальному числу строк, указанного идентификатором **MaxRecords** в приложение в **[набор записей](recordset-object-dao.md)**, обработчик запросов остановит возвращение дополнительные записи даже в том случае, если удовлетворяющих несколько записей для включения в **набор записей**. Это свойство можно использовать в ситуациях, где ресурсы ограниченный клиент запретить управление большим количеством записей.

> [!NOTE]
> Свойство **MaxRecords** может использоваться только с источником данных ODBC.

## <a name="example"></a>Пример

В этом примере используется свойство **MaxRecords** задание ограничения на количество записей возвращаемых запросом на источник данных ODBC.

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

