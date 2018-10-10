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
# <a name="querydefprepare-property-dao"></a><span data-ttu-id="5113c-102">QueryDef.Prepare Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="5113c-102">QueryDef.Prepare Property (DAO)</span></span>


<span data-ttu-id="5113c-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5113c-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="5113c-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5113c-104">Syntax</span></span>

<span data-ttu-id="5113c-105">*выражение* . Подготовка</span><span class="sxs-lookup"><span data-stu-id="5113c-105">*expression* .Prepare</span></span>

<span data-ttu-id="5113c-106">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="5113c-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5113c-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="5113c-107">Remarks</span></span>

<span data-ttu-id="5113c-108">Свойство **Prepare** либо наличие сервера создания временной хранимую процедуру из своего запроса и последующее выполнение или просто быть напрямую выполняемого запроса.</span><span class="sxs-lookup"><span data-stu-id="5113c-108">You can use the **Prepare** property to either have the server create a temporary stored procedure from your query and then execute it, or just have the query executed directly.</span></span> <span data-ttu-id="5113c-109">По умолчанию **Prepare** задано значение **dbQPrepare**.</span><span class="sxs-lookup"><span data-stu-id="5113c-109">By default the **Prepare** property is set to **dbQPrepare**.</span></span> <span data-ttu-id="5113c-110">Тем не менее это свойство можно задать для **dbQUnprepare** , чтобы запретить Подготовка запроса.</span><span class="sxs-lookup"><span data-stu-id="5113c-110">However, you can set this property to **dbQUnprepare** to prohibit preparing of the query.</span></span> <span data-ttu-id="5113c-111">В этом случае запрос выполняется с помощью **SQLExecDirect** API.</span><span class="sxs-lookup"><span data-stu-id="5113c-111">In this case, the query is executed using the **SQLExecDirect** API.</span></span>

<span data-ttu-id="5113c-112">Создание хранимой процедуры может снизить начальной операции, но приводит к повышению производительности всех последующих ссылок к запросу.</span><span class="sxs-lookup"><span data-stu-id="5113c-112">Creating a stored procedure can slow down the initial operation, but increases performance of all subsequent references to the query.</span></span> <span data-ttu-id="5113c-113">Тем не менее некоторые запросы не могут выполняться в виде хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="5113c-113">However, some queries cannot be executed in the form of stored procedures.</span></span> <span data-ttu-id="5113c-114">В таких случаях необходимо установить свойство **подготовки** к **dbQUnprepare**.</span><span class="sxs-lookup"><span data-stu-id="5113c-114">In these cases, you must set the **Prepare** property to **dbQUnprepare**.</span></span>

<span data-ttu-id="5113c-115">Если **Подготовка** **dbQPrepare**, это можно переопределить при выполнении запроса путем установки для параметра **dbExecDirect**аргумент параметры метода **[Execute](querydef-execute-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="5113c-115">If **Prepare** is set to **dbQPrepare**, this can be overridden when the query is executed by setting the **[Execute](querydef-execute-method-dao.md)** method's options argument to **dbExecDirect**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5113c-116">Как только свойству DAO <STRONG><A href="querydef-sql-property-dao.md">SQL</A></STRONG> называется ODBC <STRONG>SQLPrepare</STRONG> API.</span><span class="sxs-lookup"><span data-stu-id="5113c-116">The ODBC <STRONG>SQLPrepare</STRONG> API is called as soon as the DAO <STRONG><A href="querydef-sql-property-dao.md">SQL</A></STRONG> property is set.</span></span> <span data-ttu-id="5113c-117">Таким образом Если вы хотите повысить производительность с помощью параметра <STRONG>dbQUnprepare</STRONG> , необходимо установить свойство <STRONG>подготовить</STRONG> перед установкой <STRONG>SQL</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="5113c-117">Therefore, if you want to improve performance using the <STRONG>dbQUnprepare</STRONG> option, you must set the <STRONG>Prepare</STRONG> property before setting the <STRONG>SQL</STRONG> property.</span></span></P>



## <a name="example"></a><span data-ttu-id="5113c-118">Пример</span><span class="sxs-lookup"><span data-stu-id="5113c-118">Example</span></span>

<span data-ttu-id="5113c-119">В этом примере используется свойство **подготовить** для указания выполнения запроса непосредственно вместо создания временной хранимую процедуру на сервере.</span><span class="sxs-lookup"><span data-stu-id="5113c-119">This example uses the **Prepare** property to specify that a query should be executed directly rather than first creating a temporary stored procedure on the server.</span></span>

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

