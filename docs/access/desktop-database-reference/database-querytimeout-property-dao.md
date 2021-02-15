---
title: Свойство Database.QueryTimeout (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: c83ca852-715a-c853-429b-80a15c3fc39b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823170(v=office.15)
ms:contentKeyID: 48547648
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f47d6c51079bf36cb7e1ca596a3476f1a7219c5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294740"
---
# <a name="databasequerytimeout-property-dao"></a>Свойство Database.QueryTimeout (DAO)


**Область применения**: Access 2013, Office 2013


Задает или возвращает значение, которое указывает количество секунд ожидания до возникновения ошибки времени ожидания при выполнении запроса в источнике данных ODBC.

## <a name="syntax"></a>Синтаксис

*выражение .* QueryTimeout

*выражение*: переменная, представляющая объект **Database**.

## <a name="remarks"></a>Заметки

Значение по умолчанию  60.

При использовании базы данных ODBC, например Microsoft SQL Server, могут возникнуть задержки из-за сетевого трафика или интенсивного использования сервера ODBC. Вместо того чтобы ждать неопределенное время, можно указать время ожидания.

При использовании **QueryTimeout** с объектом **[Connection](connection-object-dao.md)** или **[Database](database-object-dao.md)** указывается глобальное значение для всех запросов, связанных с базой данных. Это значение можно переопрепредить для определенного запроса, задав свойство **ODBCTimeout** конкретного **[объекта QueryDef.](querydef-object-dao.md)**

## <a name="example"></a>Пример

В этом примере используются свойства **ODBCTimeout** и **QueryTimeout,** чтобы показать, как параметр **QueryTimeout** для объекта **Database** задает параметр **ODBCTimeout** по умолчанию для любых объектов **QueryDef,** созданных из объекта **Database.**

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

