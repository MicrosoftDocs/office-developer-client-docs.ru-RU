---
title: PROCEDURE Clause (Microsoft Access SQL)
TOCTitle: PROCEDURE Clause (Microsoft Access SQL)
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
ms.openlocfilehash: 63b38a469c5de60588783381c24c61296b177bdd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877991"
---
# <a name="procedure-clause-microsoft-access-sql"></a><span data-ttu-id="3a638-102">PROCEDURE Clause (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="3a638-102">PROCEDURE Clause (Microsoft Access SQL)</span></span>

<span data-ttu-id="3a638-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a638-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a638-104">Определяет имя и необязательные параметры для запроса.</span><span class="sxs-lookup"><span data-stu-id="3a638-104">Defines a name and optional parameters for a query.</span></span>

> [!NOTE]
> <span data-ttu-id="3a638-105">Предложение ПРОЦЕДУРЫ, был заменен на оператор ПРОЦЕДУРЫ.</span><span class="sxs-lookup"><span data-stu-id="3a638-105">The PROCEDURE clause has been superseded by the PROCEDURE statement.</span></span> <span data-ttu-id="3a638-106">Несмотря на то, что предложение ПРОЦЕДУРЫ по-прежнему поддерживается, оператор ПРОЦЕДУРЫ обеспечивает подмножеством возможность предложение ПРОЦЕДУРЫ и рекомендуемые синтаксис.</span><span class="sxs-lookup"><span data-stu-id="3a638-106">Although the PROCEDURE clause is still supported, the PROCEDURE statement provides a superset of the capability of the PROCEDURE clause and is the recommended syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a638-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a638-107">Syntax</span></span>

<span data-ttu-id="3a638-108">ПРОЦЕДУРЫ *имя* \[ *тип данных param1*\[, *тип данных param2*\[,...\]\]</span><span class="sxs-lookup"><span data-stu-id="3a638-108">PROCEDURE *name* \[*param1 datatype*\[, *param2 datatype*\[, …\]\]</span></span>

<span data-ttu-id="3a638-109">Предложение процедура состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="3a638-109">The PROCEDURE clause has these parts:</span></span>

|<span data-ttu-id="3a638-110">Часть</span><span class="sxs-lookup"><span data-stu-id="3a638-110">Part</span></span> |<span data-ttu-id="3a638-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3a638-111">Description</span></span> |
|:----|:-----------|
|<span data-ttu-id="3a638-112">*name*</span><span class="sxs-lookup"><span data-stu-id="3a638-112">*name*</span></span> |<span data-ttu-id="3a638-113">Имя процедуры.</span><span class="sxs-lookup"><span data-stu-id="3a638-113">A name for the procedure.</span></span> <span data-ttu-id="3a638-114">Оно должно соответствовать стандартным соглашениям об именах.</span><span class="sxs-lookup"><span data-stu-id="3a638-114">It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="3a638-115">*param1* *param2*</span><span class="sxs-lookup"><span data-stu-id="3a638-115">*param1*, *param2*</span></span> |<span data-ttu-id="3a638-116">Один или несколько имен полей или параметров.</span><span class="sxs-lookup"><span data-stu-id="3a638-116">One or more field names or parameters.</span></span> <span data-ttu-id="3a638-117">Пример:</span><span class="sxs-lookup"><span data-stu-id="3a638-117">For example:</span></span><br/><br/>`PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="3a638-118">[Дополнительные сведения о параметрах см.](parameters-declaration-microsoft-access-sql.md)</span><span class="sxs-lookup"><span data-stu-id="3a638-118">For more information about parameters, see [parameters](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="3a638-119">*Тип данных*</span><span class="sxs-lookup"><span data-stu-id="3a638-119">*datatype*</span></span> | <span data-ttu-id="3a638-120">Одна из основных [типов данных Microsoft Access SQL](sql-data-types.md) или их синонимы.</span><span class="sxs-lookup"><span data-stu-id="3a638-120">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span> |


## <a name="remarks"></a><span data-ttu-id="3a638-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="3a638-121">Remarks</span></span>

<span data-ttu-id="3a638-122">Процедура SQL состоит из предложения PROCEDURE (определяющего имя процедуры), дополнительный список параметров определения и одной инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="3a638-122">An SQL procedure consists of a PROCEDURE clause (which specifies the name of the procedure), an optional list of parameter definitions, and a single SQL statement.</span></span> <span data-ttu-id="3a638-123">Например, процедура Get\_часть\_номер может выполнять запрос, который извлекает указанную часть номер.</span><span class="sxs-lookup"><span data-stu-id="3a638-123">For example, the procedure Get\_Part\_Number might run a query that retrieves a specified part number.</span></span>

> [!NOTE]
> - <span data-ttu-id="3a638-124">Если предложение включает более одного определения поля (то есть, пары *параметр-тип данных* ), разделяйте их запятыми.</span><span class="sxs-lookup"><span data-stu-id="3a638-124">If the clause includes more than one field definition (that is, *param-datatype* pairs), separate them with commas.</span></span>
> - <span data-ttu-id="3a638-125">Предложение процедуру необходимо следовать инструкции SQL [(например, [ВЫБЕРИТЕ](select-statement-microsoft-access-sql.md) инструкции)](update-statement-microsoft-access-sql.md) .</span><span class="sxs-lookup"><span data-stu-id="3a638-125">The PROCEDURE clause must be followed by an SQL statement (for example, a [SELECT](select-statement-microsoft-access-sql.md) or [UPDATE](update-statement-microsoft-access-sql.md) statement).</span></span>

## <a name="example"></a><span data-ttu-id="3a638-126">Пример</span><span class="sxs-lookup"><span data-stu-id="3a638-126">Example</span></span>

<span data-ttu-id="3a638-127">В этом примере имена запроса CategoryList и вызывает процедуру EnumFields, которые можно найти в примере инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="3a638-127">This example names the query CategoryList, and calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
