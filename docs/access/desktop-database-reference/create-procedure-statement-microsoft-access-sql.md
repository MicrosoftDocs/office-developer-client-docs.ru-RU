---
title: Оператор CREATE PROCEDURE (Microsoft Access SQL)
TOCTitle: CREATE PROCEDURE statement (Microsoft Access SQL)
ms:assetid: 1fbb5267-9862-bfb4-6436-176152d7a6cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845861(v=office.15)
ms:contentKeyID: 48543649
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: f223e164bd36a6a1a76140a28dd57cd2005e4a20
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700768"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a><span data-ttu-id="f2963-102">Оператор CREATE PROCEDURE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="f2963-102">CREATE PROCEDURE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="f2963-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2963-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="f2963-104">Создает сохраняемую процедуру.</span><span class="sxs-lookup"><span data-stu-id="f2963-104">Creates a stored procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="f2963-105">Ядро СУБД Access не поддерживает использование оператора CREATE PROCEDURE или любые операторы DDL с базами данных с ядром СУБД Jet, не принадлежащими Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f2963-105">The Microsoft Access database engine does not support the use of CREATE PROCEDURE, or any of the DDL statements, with non-Microsoft Jet database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2963-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2963-106">Syntax</span></span>

<span data-ttu-id="f2963-107">CREATE PROCEDURE *procedure* \[*param1 datatype*\[, *param2 datatype*\[, …\]\] AS sqlstatement</span><span class="sxs-lookup"><span data-stu-id="f2963-107">CREATE PROCEDURE *procedure* \[*param1 datatype*\[, *param2 datatype*\[, …\]\] AS sqlstatement</span></span>

<span data-ttu-id="f2963-108">Оператор CREATE PROCEDURE состоит из трех частей:</span><span class="sxs-lookup"><span data-stu-id="f2963-108">The CREATE PROCEDURE statement has these parts:</span></span>

|<span data-ttu-id="f2963-109">Часть</span><span class="sxs-lookup"><span data-stu-id="f2963-109">Part</span></span>|<span data-ttu-id="f2963-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f2963-110">Description</span></span>|
|:---|:----------|
|<span data-ttu-id="f2963-111">*procedure*</span><span class="sxs-lookup"><span data-stu-id="f2963-111">*Procedure*</span></span>|<span data-ttu-id="f2963-112">Название процедуры.</span><span class="sxs-lookup"><span data-stu-id="f2963-112">Choose another name for the procedure.</span></span> <span data-ttu-id="f2963-113">Необходимо выполнение стандартных соглашений об именовании.</span><span class="sxs-lookup"><span data-stu-id="f2963-113">It must follow standard naming conventions.</span></span>|
|<span data-ttu-id="f2963-114">*param1*, *param2*</span><span class="sxs-lookup"><span data-stu-id="f2963-114">*param1*, *param2*</span></span>|<span data-ttu-id="f2963-115">От 1 до 255 имен полей или параметров.</span><span class="sxs-lookup"><span data-stu-id="f2963-115">From one to 255 field names or parameters.</span></span> <span data-ttu-id="f2963-116">Пример:</span><span class="sxs-lookup"><span data-stu-id="f2963-116">For example:</span></span><br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/><span data-ttu-id="f2963-117">Дополнительные сведения о параметрах см. в разделе [ПАРАМЕТРЫ](parameters-declaration-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="f2963-117">For more information about query parameters, see [Customize responses](parameters-declaration-microsoft-access-sql.md).</span></span>|
|<span data-ttu-id="f2963-118">*datatype*</span><span class="sxs-lookup"><span data-stu-id="f2963-118">*DataType*</span></span>|<span data-ttu-id="f2963-119">Один из основных [типов данных Microsoft Access SQL](sql-data-types.md) или их синонимов.</span><span class="sxs-lookup"><span data-stu-id="f2963-119">One of the primary [Microsoft Access SQL data types](sql-data-types.md) or their synonyms.</span></span>|
|<span data-ttu-id="f2963-120">*sqlstatement*</span><span class="sxs-lookup"><span data-stu-id="f2963-120">*sqlstatement*</span></span>|<span data-ttu-id="f2963-121">Оператор SQL, например SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE и т. д.</span><span class="sxs-lookup"><span data-stu-id="f2963-121">An SQL statement such as SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE, and so on.</span></span>|


## <a name="remarks"></a><span data-ttu-id="f2963-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2963-122">Remarks</span></span>

<span data-ttu-id="f2963-123">Оператор SQL состоит из выражения PROCEDURE, определяющего имя процедуры, необязательный список определений параметров и одного оператора SQL.</span><span class="sxs-lookup"><span data-stu-id="f2963-123">An SQL procedure consists of a PROCEDURE clause that specifies the name of the procedure, an optional list of parameter definitions, and a single SQL statement.</span></span>

<span data-ttu-id="f2963-124">Имя процедуры не может совпадать с именем существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="f2963-124">A procedure name cannot be the same as the name of an existing table.</span></span>

## <a name="example"></a><span data-ttu-id="f2963-125">Пример</span><span class="sxs-lookup"><span data-stu-id="f2963-125">Example</span></span>

<span data-ttu-id="f2963-126">В этом примере присваивается имя запросу EnumFields и выполняется вызов процедуры EnumFields, который вы можете найти в приведенном примере инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="f2963-126">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
