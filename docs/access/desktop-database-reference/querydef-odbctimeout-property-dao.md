---
title: QueryDef.ODBCTimeout Property (DAO)
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
ms.openlocfilehash: dcb15511f3052366eb3d322c26cdd31d72c9beab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482879"
---
# <a name="querydefodbctimeout-property-dao"></a>QueryDef.ODBCTimeout Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Указывает количество секунд до ошибку времени ожидания происходит, когда **[QueryDef](querydef-object-dao.md)** выполняется в базе данных ODBC.

## <a name="syntax"></a>Синтаксис

*выражение* . Время ожидания ODBC

*выражение* Переменная, которая представляет собой объект- **QueryDef** .

## <a name="remarks"></a>Замечания

Если свойство **время ожидания ODBC** — это значение -1, время ожидания по умолчанию используется текущий параметр свойства **[QueryTimeout](database-querytimeout-property-dao.md)** **[подключения](connection-object-dao.md)** или объекта **[базы данных](database-object-dao.md)** , содержащий **QueryDef**. Если свойство **время ожидания ODBC** имеет значение 0, время ожидания ошибок нет.

При использовании базы данных ODBC, например Microsoft SQL Server, задержки могут возникнуть из-за сетевой трафик или интенсивное использование сервера ODBC. Без необходимости неограниченное время, можно указать время ожидания перед сообщение об ошибке.

**Время ожидания ODBC** свойства объекта **QueryDef** переопределяет значение, назначаемое свойству **QueryTimeout** объекта **подключения** или **базы данных** , содержащего **QueryDef**, но только для этого ** QueryDef** объекта.

## <a name="example"></a>Пример

В этом примере используется для отображения как параметр **QueryTimeout** для объекта **базы данных** задает **время ожидания ODBC** по умолчанию для любого объекта **QueryDef** , созданный из свойства **QueryTimeout** и **время ожидания ODBC** Объект **базы данных** .

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

