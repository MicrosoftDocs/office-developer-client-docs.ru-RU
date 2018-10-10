---
title: CREATE PROCEDURE Statement (Microsoft Access SQL)
TOCTitle: CREATE PROCEDURE Statement (Microsoft Access SQL)
ms:assetid: 1fbb5267-9862-bfb4-6436-176152d7a6cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845861(v=office.15)
ms:contentKeyID: 48543649
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: adad7d052e7efbece90f626a50eb50b7bb5b834e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482135"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a><span data-ttu-id="658c9-102">CREATE PROCEDURE Statement (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="658c9-102">CREATE PROCEDURE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="658c9-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="658c9-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="658c9-104">Создает хранимую процедуру.</span><span class="sxs-lookup"><span data-stu-id="658c9-104">Creates a stored procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="658c9-105">Ядро базы данных Microsoft Access не поддерживает использование создать процедуру или любой другой инструкции DDL с базами данных, ядро базы данных Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="658c9-105">The Microsoft Access database engine does not support the use of CREATE PROCEDURE, or any of the DDL statements, with non-Microsoft Jet database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="658c9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="658c9-106">Syntax</span></span>

<span data-ttu-id="658c9-107">ПРОЦЕДУРА СОЗДАНИЯ *процедуры* \[ *тип данных param1*\[, *тип данных param2*\[,... \] \] Как sqlstatement</span><span class="sxs-lookup"><span data-stu-id="658c9-107">CREATE PROCEDURE *procedure* \[*param1 datatype*\[, *param2 datatype*\[, …\]\] AS sqlstatement</span></span>

<span data-ttu-id="658c9-108">Инструкция CREATE PROCEDURE состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="658c9-108">The CREATE PROCEDURE statement has these parts:</span></span>

|<span data-ttu-id="658c9-109">Часть</span><span class="sxs-lookup"><span data-stu-id="658c9-109">Part</span></span>|<span data-ttu-id="658c9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="658c9-110">Description</span></span>|
|:---|:----------|
|<span data-ttu-id="658c9-111">*процедура*</span><span class="sxs-lookup"><span data-stu-id="658c9-111">*procedure*</span></span>|<span data-ttu-id="658c9-112">Имя процедуры.</span><span class="sxs-lookup"><span data-stu-id="658c9-112">A name for the procedure.</span></span> <span data-ttu-id="658c9-113">Оно должно соответствовать стандартным соглашениям об именах.</span><span class="sxs-lookup"><span data-stu-id="658c9-113">It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="658c9-114">*param1* *param2*</span><span class="sxs-lookup"><span data-stu-id="658c9-114">*param1*, *param2*</span></span>|<span data-ttu-id="658c9-115">От одного до 255 имен полей или параметров.</span><span class="sxs-lookup"><span data-stu-id="658c9-115">From one to 255 field names or parameters.</span></span> <span data-ttu-id="658c9-116">Пример:</span><span class="sxs-lookup"><span data-stu-id="658c9-116">For example:</span></span><br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="658c9-117">[Дополнительные сведения о параметрах см.](parameters-declaration-microsoft-access-sql.md)</span><span class="sxs-lookup"><span data-stu-id="658c9-117">For more information about parameters, see [PARAMETERS](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="658c9-118">*Тип данных*</span><span class="sxs-lookup"><span data-stu-id="658c9-118">*datatype*</span></span>|<span data-ttu-id="658c9-119">Одна из основных [типов данных Microsoft Access SQL](sql-data-types.md) или их синонимы.</span><span class="sxs-lookup"><span data-stu-id="658c9-119">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span>|
|<span data-ttu-id="658c9-120">*SQLStatement*</span><span class="sxs-lookup"><span data-stu-id="658c9-120">*sqlstatement*</span></span>|<span data-ttu-id="658c9-121">Инструкция SQL, такие как выбор, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE и т.д.</span><span class="sxs-lookup"><span data-stu-id="658c9-121">An SQL statement such as SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE, and so on.</span></span>|


## <a name="remarks"></a><span data-ttu-id="658c9-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="658c9-122">Remarks</span></span>

<span data-ttu-id="658c9-123">Процедура SQL состоит из предложения PROCEDURE, которое определяет имя процедуры, дополнительный список параметров определения и одной инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="658c9-123">An SQL procedure consists of a PROCEDURE clause that specifies the name of the procedure, an optional list of parameter definitions, and a single SQL statement.</span></span>

<span data-ttu-id="658c9-124">Имя процедуры не может быть имя существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="658c9-124">A procedure name cannot be the same as the name of an existing table.</span></span>

## <a name="example"></a><span data-ttu-id="658c9-125">Пример</span><span class="sxs-lookup"><span data-stu-id="658c9-125">Example</span></span>

<span data-ttu-id="658c9-126">В этом примере имена запроса CategoryList и вызывает процедуру EnumFields, которые можно найти в примере инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="658c9-126">This example names the query CategoryList, and calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
