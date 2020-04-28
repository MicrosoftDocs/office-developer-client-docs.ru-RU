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
# <a name="querydefprepare-property-dao"></a><span data-ttu-id="c5142-102">Свойство QueryDef. Prepare (DAO)</span><span class="sxs-lookup"><span data-stu-id="c5142-102">QueryDef.Prepare property (DAO)</span></span>

<span data-ttu-id="c5142-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5142-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="c5142-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5142-104">Syntax</span></span>

<span data-ttu-id="c5142-105">*Expression* . Подготовка</span><span class="sxs-lookup"><span data-stu-id="c5142-105">*expression* .Prepare</span></span>

<span data-ttu-id="c5142-106">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="c5142-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5142-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="c5142-107">Remarks</span></span>

<span data-ttu-id="c5142-108">Свойство **Prepare** можно использовать для того, чтобы сервер мог создать временную хранимую процедуру в запросе, а затем выполнить ее или просто выполнить запрос напрямую.</span><span class="sxs-lookup"><span data-stu-id="c5142-108">You can use the **Prepare** property to either have the server create a temporary stored procedure from your query and then execute it, or just have the query executed directly.</span></span> <span data-ttu-id="c5142-109">По умолчанию для свойства **Prepare** задано значение **дбкпрепаре**.</span><span class="sxs-lookup"><span data-stu-id="c5142-109">By default the **Prepare** property is set to **dbQPrepare**.</span></span> <span data-ttu-id="c5142-110">Однако для этого свойства можно задать значение **дбкунпрепаре** , чтобы запретить подготовку запроса.</span><span class="sxs-lookup"><span data-stu-id="c5142-110">However, you can set this property to **dbQUnprepare** to prohibit preparing of the query.</span></span> <span data-ttu-id="c5142-111">В этом случае запрос выполняется с помощью API **склексекдирект** .</span><span class="sxs-lookup"><span data-stu-id="c5142-111">In this case, the query is executed using the **SQLExecDirect** API.</span></span>

<span data-ttu-id="c5142-112">Создание хранимой процедуры может замедлить выполнение начальной операции, но повышает производительность всех последующих ссылок на запрос.</span><span class="sxs-lookup"><span data-stu-id="c5142-112">Creating a stored procedure can slow down the initial operation, but increases performance of all subsequent references to the query.</span></span> <span data-ttu-id="c5142-113">Однако некоторые запросы невозможно выполнить в виде хранимых процедур.</span><span class="sxs-lookup"><span data-stu-id="c5142-113">However, some queries cannot be executed in the form of stored procedures.</span></span> <span data-ttu-id="c5142-114">В таких случаях необходимо присвоить свойству **Prepare** значение **дбкунпрепаре**.</span><span class="sxs-lookup"><span data-stu-id="c5142-114">In these cases, you must set the **Prepare** property to **dbQUnprepare**.</span></span>

<span data-ttu-id="c5142-115">Если параметр **Prepare** имеет значение **дбкпрепаре**, его можно переопределить при выполнении запроса, присвоив аргументу options метода **[EXECUTE](querydef-execute-method-dao.md)** значение **дбексекдирект**.</span><span class="sxs-lookup"><span data-stu-id="c5142-115">If **Prepare** is set to **dbQPrepare**, this can be overridden when the query is executed by setting the **[Execute](querydef-execute-method-dao.md)** method's options argument to **dbExecDirect**.</span></span>

> [!NOTE]
> <span data-ttu-id="c5142-116">API-интерфейс ODBC **склпрепаре** вызывается сразу после задания свойства DAO **[SQL](querydef-sql-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="c5142-116">The ODBC **SQLPrepare** API is called as soon as the DAO **[SQL](querydef-sql-property-dao.md)** property is set.</span></span> <span data-ttu-id="c5142-117">Таким образом, если вы хотите увеличить производительность с помощью параметра **дбкунпрепаре** , необходимо задать свойство **Prepare** перед заданием свойства **SQL** .</span><span class="sxs-lookup"><span data-stu-id="c5142-117">Therefore, if you want to improve performance using the **dbQUnprepare** option, you must set the **Prepare** property before setting the **SQL** property.</span></span>

## <a name="example"></a><span data-ttu-id="c5142-118">Пример</span><span class="sxs-lookup"><span data-stu-id="c5142-118">Example</span></span>

<span data-ttu-id="c5142-119">В этом примере используется свойство **Prepare** для указания того, что запрос должен выполняться напрямую, а не сначала создается временная хранимая процедура на сервере.</span><span class="sxs-lookup"><span data-stu-id="c5142-119">This example uses the **Prepare** property to specify that a query should be executed directly rather than first creating a temporary stored procedure on the server.</span></span>

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

