---
title: Свойство QueryDef.Prepare (DAO)
TOCTitle: Prepare Property
ms:assetid: d5a285c4-bd00-028b-b785-f1890db29bab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835035(v=office.15)
ms:contentKeyID: 48547968
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101187
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ac05510a218d1cf4cf925acc2ca8908b7bcbcd03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303271"
---
# <a name="querydefprepare-property-dao"></a>Свойство QueryDef.Prepare (DAO)

**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражения* . Подготовка

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Примечания

Свойство **Prepare** можно использовать для того, чтобы сервер создал временную процедуру хранения из запроса, а затем выполнил ее или просто выполнил запрос напрямую. По умолчанию **свойство Prepare** настроено на **dbQPrepare**. Однако это свойство можно установить **в dbQUnprepare,** чтобы запретить подготовку запроса. В этом случае запрос выполняется с помощью **API SQLExecDirect.**

Создание сохраненной процедуры может замедлить начальную операцию, но повышает производительность всех последующих ссылок на запрос. Однако некоторые запросы не могут выполняться в виде сохраненных процедур. В этих случаях необходимо установить свойство **Prepare** для **dbQUnprepare.**

Если **задан** параметр Prepare для **dbQPrepare,** это может быть переопределено при выполнении запроса, задав аргумент параметрам метода **[Execute](querydef-execute-method-dao.md)** **в dbExecDirect.**

> [!NOTE]
> API **SQLPrepare** ODBC называется сразу же после SQL свойства **[DAO.](querydef-sql-property-dao.md)** Поэтому для повышения производительности с помощью параметра **dbQUnprepare** необходимо задать свойство **Prepare** **перед SQL** свойством.

## <a name="example"></a>Пример

В этом примере свойство **Prepare** указывает, что запрос должен выполняться непосредственно, а не сначала создавать временную процедуру хранения на сервере.

```vb 
Sub PrepareX() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' object. 
 Set wrkODBC = CreateWorkspace("", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Set qdfTemp = conPubs.CreateQueryDef("") 
 
 With qdfTemp 
 ' Because you will only run this query once, specify 
 ' the ODBC SQLExecDirect API function. If you do 
 ' not set this property before you set the SQL 
 ' property, the ODBC SQLPrepare API function will 
 ' be called anyway which will nullify any 
 ' performance gain. 
 .Prepare = dbQUnprepare 
 .SQL = "UPDATE roysched " & _ 
 "SET royalty = royalty * 2 " & _ 
 "WHERE title_id LIKE 'BU____' OR " & _ 
 "title_id LIKE 'PC____'" 
 .Execute 
 End With 
 
 Debug.Print "Query results:" 
 
 ' Open recordset containing modified records. 
 Set rstTemp = conPubs.OpenRecordset( _ 
 "SELECT * FROM roysched " & _ 
 "WHERE title_id LIKE 'BU____' OR " & _ 
 "title_id LIKE 'PC____'") 
 
 ' Enumerate recordset. 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , !title_id, !lorange, _ 
 !hirange, !royalty 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 conPubs.Close 
 wrkODBC.Close 
 
```

