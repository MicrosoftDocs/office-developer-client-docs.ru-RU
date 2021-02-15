---
title: Предложение PROCEDURE (Microsoft Access SQL)
TOCTitle: PROCEDURE clause (Microsoft Access SQL)
ms:assetid: a718802c-9260-88d5-ec29-d5e5594927b0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821342(v=office.15)
ms:contentKeyID: 48546872
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277578
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 72f31c71e710cca79695a7221f0e033d18d2f420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301381"
---
# <a name="procedure-clause-microsoft-access-sql"></a><span data-ttu-id="484bb-102">Предложение PROCEDURE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="484bb-102">PROCEDURE clause (Microsoft Access SQL)</span></span>

<span data-ttu-id="484bb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="484bb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="484bb-104">Определяет имя и необязательные параметры для запроса.</span><span class="sxs-lookup"><span data-stu-id="484bb-104">Defines a name and optional parameters for a query.</span></span>

> [!NOTE]
> <span data-ttu-id="484bb-105">Предложение PROCEDURE было замехано заявлением PROCEDURE.</span><span class="sxs-lookup"><span data-stu-id="484bb-105">The PROCEDURE clause has been superseded by the PROCEDURE statement.</span></span> <span data-ttu-id="484bb-106">Хотя предложение PROCEDURE по-прежнему поддерживается, заявление PROCEDURE предоставляет более набор возможностей предложения PROCEDURE и является рекомендуемой синтаксис.</span><span class="sxs-lookup"><span data-stu-id="484bb-106">Although the PROCEDURE clause is still supported, the PROCEDURE statement provides a superset of the capability of the PROCEDURE clause and is the recommended syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="484bb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="484bb-107">Syntax</span></span>

<span data-ttu-id="484bb-108">ИМЯ  \[ *ПРОЦЕДУРы param1 datatype,* \[ *param2 datatype*, \[ ...\]\]</span><span class="sxs-lookup"><span data-stu-id="484bb-108">PROCEDURE *name* \[*param1 datatype*\[, *param2 datatype*\[, …\]\]</span></span>

<span data-ttu-id="484bb-109">Предложение PROCEDURE имеет указанные здесь части.</span><span class="sxs-lookup"><span data-stu-id="484bb-109">The PROCEDURE clause has these parts:</span></span>

|<span data-ttu-id="484bb-110">Часть</span><span class="sxs-lookup"><span data-stu-id="484bb-110">Part</span></span> |<span data-ttu-id="484bb-111">Описание</span><span class="sxs-lookup"><span data-stu-id="484bb-111">Description</span></span> |
|:----|:-----------|
|<span data-ttu-id="484bb-112">*name*</span><span class="sxs-lookup"><span data-stu-id="484bb-112">*name*</span></span> |<span data-ttu-id="484bb-113">Название процедуры.</span><span class="sxs-lookup"><span data-stu-id="484bb-113">A name for the procedure.</span></span> <span data-ttu-id="484bb-114">Необходимо выполнение стандартных соглашений об именовании.</span><span class="sxs-lookup"><span data-stu-id="484bb-114">It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="484bb-115">*param1*, *param2*</span><span class="sxs-lookup"><span data-stu-id="484bb-115">*param1*, *param2*</span></span> |<span data-ttu-id="484bb-116">Одно или несколько имен полей или параметров.</span><span class="sxs-lookup"><span data-stu-id="484bb-116">One or more field names or parameters.</span></span> <span data-ttu-id="484bb-117">Например:</span><span class="sxs-lookup"><span data-stu-id="484bb-117">For example:</span></span><br/><br/>`PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="484bb-118">Дополнительные сведения о параметрах см. [в параметрах.](parameters-declaration-microsoft-access-sql.md)</span><span class="sxs-lookup"><span data-stu-id="484bb-118">For more information about parameters, see [parameters](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="484bb-119">*datatype*</span><span class="sxs-lookup"><span data-stu-id="484bb-119">*datatype*</span></span> | <span data-ttu-id="484bb-120">Один из основных [типов данных Microsoft Access SQL](sql-data-types.md) или их синонимов.</span><span class="sxs-lookup"><span data-stu-id="484bb-120">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span> |


## <a name="remarks"></a><span data-ttu-id="484bb-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="484bb-121">Remarks</span></span>

<span data-ttu-id="484bb-122">Процедура SQL состоит из предложения PROCEDURE (которое указывает имя процедуры), необязательного списка определений параметров и одного SQL процедуры.</span><span class="sxs-lookup"><span data-stu-id="484bb-122">An SQL procedure consists of a PROCEDURE clause (which specifies the name of the procedure), an optional list of parameter definitions, and a single SQL statement.</span></span> <span data-ttu-id="484bb-123">Например, процедура получения номера части может выполнить запрос, который \_ \_ извлекает указанный номер части.</span><span class="sxs-lookup"><span data-stu-id="484bb-123">For example, the procedure Get\_Part\_Number might run a query that retrieves a specified part number.</span></span>

> [!NOTE]
> - <span data-ttu-id="484bb-124">Если предложение содержит несколько определений полей (то есть пары *param-datatype),* разделяйте их запятой.</span><span class="sxs-lookup"><span data-stu-id="484bb-124">If the clause includes more than one field definition (that is, *param-datatype* pairs), separate them with commas.</span></span>
> - <span data-ttu-id="484bb-125">За предложением PROCEDURE следует SQL (например, [SELECT](select-statement-microsoft-access-sql.md) или [UPDATE).](update-statement-microsoft-access-sql.md)</span><span class="sxs-lookup"><span data-stu-id="484bb-125">The PROCEDURE clause must be followed by an SQL statement (for example, a [SELECT](select-statement-microsoft-access-sql.md) or [UPDATE](update-statement-microsoft-access-sql.md) statement).</span></span>

## <a name="example"></a><span data-ttu-id="484bb-126">Пример</span><span class="sxs-lookup"><span data-stu-id="484bb-126">Example</span></span>

<span data-ttu-id="484bb-127">В этом примере присваивается имя запросу CategoryList и выполняется вызов процедуры EnumFields, которую вы можете найти в приведенном примере для оператора SELECT.</span><span class="sxs-lookup"><span data-stu-id="484bb-127">This example names the query CategoryList, and calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub ProcedureX() 
     
        Dim dbs As Database, rst As Recordset 
        Dim qdf As QueryDef, strSql As String 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        strSql = "PROCEDURE CategoryList; " _ 
            & "SELECT DISTINCTROW CategoryName, " _ 
            & "CategoryID FROM Categories " _ 
            & "ORDER BY CategoryName;" 
         
        ' Create a named QueryDef based on the SQL 
        ' statement. 
        Set qdf = dbs.CreateQueryDef("NewQry", strSql) 
     
        ' Create a temporary snapshot-type Recordset. 
        Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
        ' Populate the Recordset. 
        rst.MoveLast 
                 
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
