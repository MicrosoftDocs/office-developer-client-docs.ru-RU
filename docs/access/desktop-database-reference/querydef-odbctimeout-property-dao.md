---
title: Свойство QueryDef. ODBCTimeout (DAO)
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
# <a name="querydefodbctimeout-property-dao"></a>Свойство QueryDef. ODBCTimeout (DAO)


**Область применения**: Access 2013, Office 2013

Указывает время ожидания (в секундах) до возникновения ошибки времени ожидания при выполнении объекта **[QueryDef](querydef-object-dao.md)** в базе данных ODBC.

## <a name="syntax"></a>Синтаксис

*Expression* . ODBCTimeout

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Замечания

Если для **Свойства ODBCTimeout** задано значение-1, время ожидания по умолчанию равно текущему значению **[Свойства QueryTimeout](database-querytimeout-property-dao.md)** **[подключения](connection-object-dao.md)** или объекта **[базы данных](database-object-dao.md)** , содержащего объект **QueryDef**. Если для свойства **ODBCTimeout** задано значение 0, ошибка времени ожидания не возникает.

При использовании базы данных ODBC, такой как Microsoft SQL Server, могут возникать задержки из-за сетевого трафика или интенсивного использования сервера ODBC. Вместо неопределенного периода ожидания можно указать время ожидания перед возвращением ошибки.

Установка свойства **ODBCTimeout** объекта **QueryDef** переопределяет значение, указанное в свойстве **QueryTimeOut** **подключения** или объекта **базы данных** , содержащего объект **QueryDef**, но только для этого ** Объект QueryDef** .

## <a name="example"></a>Пример

В этом примере используются свойства **ODBCTimeout** и **QueryTimeOut** , чтобы показать, как параметр **QueryTimeOut** в объекте **Database** задает значение по умолчанию **ODBCTimeout** для объектов **QueryDef** , созданных из Объект **Database** .

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

