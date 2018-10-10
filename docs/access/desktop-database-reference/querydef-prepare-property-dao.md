---
title: QueryDef.Prepare Property (DAO)
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
ms.openlocfilehash: cec1fde6bc76438da2292ae30545337eaeea6cf4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481231"
---
# <a name="querydefprepare-property-dao"></a>QueryDef.Prepare Property (DAO)


**Применимо к**: Access 2013 | Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . Подготовка

*выражение* Переменная, которая представляет собой объект- **QueryDef** .

## <a name="remarks"></a>Замечания

Свойство **Prepare** либо наличие сервера создания временной хранимую процедуру из своего запроса и последующее выполнение или просто быть напрямую выполняемого запроса. По умолчанию **Prepare** задано значение **dbQPrepare**. Тем не менее это свойство можно задать для **dbQUnprepare** , чтобы запретить Подготовка запроса. В этом случае запрос выполняется с помощью **SQLExecDirect** API.

Создание хранимой процедуры может снизить начальной операции, но приводит к повышению производительности всех последующих ссылок к запросу. Тем не менее некоторые запросы не могут выполняться в виде хранимых процедур. В таких случаях необходимо установить свойство **подготовки** к **dbQUnprepare**.

Если **Подготовка** **dbQPrepare**, это можно переопределить при выполнении запроса путем установки для параметра **dbExecDirect**аргумент параметры метода **[Execute](querydef-execute-method-dao.md)** .


> [!NOTE]
> <P>Как только свойству DAO <STRONG><A href="querydef-sql-property-dao.md">SQL</A></STRONG> называется ODBC <STRONG>SQLPrepare</STRONG> API. Таким образом Если вы хотите повысить производительность с помощью параметра <STRONG>dbQUnprepare</STRONG> , необходимо установить свойство <STRONG>подготовить</STRONG> перед установкой <STRONG>SQL</STRONG> .</P>



## <a name="example"></a>Пример

В этом примере используется свойство **подготовить** для указания выполнения запроса непосредственно вместо создания временной хранимую процедуру на сервере.

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

