---
title: Свойство QueryDef. Prepare (DAO)
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
# <a name="querydefprepare-property-dao"></a>Свойство QueryDef. Prepare (DAO)

**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . Подготовка

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Замечания

Свойство **Prepare** можно использовать для того, чтобы сервер мог создать временную хранимую процедуру в запросе, а затем выполнить ее или просто выполнить запрос напрямую. По умолчанию для свойства **Prepare** задано значение **дбкпрепаре**. Однако для этого свойства можно задать значение **дбкунпрепаре** , чтобы запретить подготовку запроса. В этом случае запрос выполняется с помощью API **склексекдирект** .

Создание хранимой процедуры может замедлить выполнение начальной операции, но повышает производительность всех последующих ссылок на запрос. Однако некоторые запросы невозможно выполнить в виде хранимых процедур. В таких случаях необходимо присвоить свойству **Prepare** значение **дбкунпрепаре**.

Если параметр **Prepare** имеет значение **дбкпрепаре**, его можно переопределить при выполнении запроса, присвоив аргументу options метода **[EXECUTE](querydef-execute-method-dao.md)** значение **дбексекдирект**.

> [!NOTE]
> API-интерфейс ODBC **склпрепаре** вызывается сразу после задания свойства DAO **[SQL](querydef-sql-property-dao.md)** . Таким образом, если вы хотите увеличить производительность с помощью параметра **дбкунпрепаре** , необходимо задать свойство **Prepare** перед заданием свойства **SQL** .

## <a name="example"></a>Пример

В этом примере используется свойство **Prepare** для указания того, что запрос должен выполняться напрямую, а не сначала создается временная хранимая процедура на сервере.

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

