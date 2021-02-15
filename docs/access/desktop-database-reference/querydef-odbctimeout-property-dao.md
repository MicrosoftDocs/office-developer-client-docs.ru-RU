---
title: Свойство QueryDef.ODBCTimeout (DAO)
TOCTitle: ODBCTimeout Property
ms:assetid: b251c4fb-64a8-aa95-deed-64425df3e00c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822019(v=office.15)
ms:contentKeyID: 48547166
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053052
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2d34aee30e649b1c25ddc6af8078da2af9dd3b84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301003"
---
# <a name="querydefodbctimeout-property-dao"></a>Свойство QueryDef.ODBCTimeout (DAO)


**Область применения**: Access 2013, Office 2013

Указывает время ожидания в секундах до возникновения ошибки времени ожидания при выполнении **[QueryDef](querydef-object-dao.md)** в базе данных ODBC.

## <a name="syntax"></a>Синтаксис

*выражение .* ODBCTimeout

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Примечания

Если для свойства **ODBCTimeout** установлено значение -1, по умолчанию по умолчанию устанавливается текущее значение параметра **[свойства QueryTimeout](database-querytimeout-property-dao.md)** объекта **[Connection](connection-object-dao.md)** или **[Database,](database-object-dao.md)** который содержит **QueryDef.** Если для **свойства ODBCTimeout** установлено 0, ошибка времени простоя не возникает.

При использовании базы данных ODBC, например Microsoft SQL Server, задержки могут возникать из-за сетевого трафика или интенсивного использования сервера ODBC. Вместо того чтобы ждать неопределенное время, можно указать время ожидания перед возвратом ошибки.

При установке свойства **ODBCTimeout** объекта **QueryDef** переопределяется значение, указанное **свойством QueryTimeout** объекта **Connection** или **Database,** содержащего **QueryDef,** но только для этого объекта **QueryDef.**

## <a name="example"></a>Пример

В этом примере используются свойства **ODBCTimeout** и **QueryTimeout,** чтобы показать, как параметр **QueryTimeout** объекта **базы** данных задает параметр **ODBCTimeout** по умолчанию для любых объектов **QueryDef,** созданных из объекта **Database.**

```vb 
Sub ODBCTimeoutX() 
 
 Dim dbsCurrent As Database 
 Dim qdfStores As QueryDef 
 Dim rstStores As Recordset 
 
 Set dbsCurrent = OpenDatabase("Northwind.mdb") 
 
 ' Change the default QueryTimeout of the Northwind 
 ' database. 
 Debug.Print "Default QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 dbsCurrent.QueryTimeout = 30 
 Debug.Print "New QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 
 ' Create a new QueryDef object. 
 Set qdfStores = dbsCurrent.CreateQueryDef("Stores", _ 
 "SELECT * FROM stores") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the SQL Server. 
 qdfStores.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 
 ' Change the ODBCTimeout setting of the new QueryDef 
 ' object from its default setting. 
 Debug.Print "Default ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 qdfStores.ODBCTimeout = 0 
 Debug.Print "New ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 
 ' Execute the query and display the results. 
 Set rstStores = qdfStores.OpenRecordset() 
 
 Debug.Print "Contents of recordset:" 
 With rstStores 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 ' Delete new QueryDef because this is a demonstration. 
 dbsCurrent.QueryDefs.Delete qdfStores.Name 
 dbsCurrent.Close 
 
End Sub 
 
```

