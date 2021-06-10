---
title: Скалярные функции ODBC
TOCTitle: ODBC scalar functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 33443fda474b3785d34d457719e49f5e358bb254
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288513"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="9c980-102">Скалярные функции ODBC</span><span class="sxs-lookup"><span data-stu-id="9c980-102">ODBC scalar functions</span></span>

<span data-ttu-id="9c980-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9c980-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9c980-104">Microsoft Access SQL поддерживает использование синтаксиса ODBC для функций scalar.</span><span class="sxs-lookup"><span data-stu-id="9c980-104">Microsoft Access SQL supports the use of the ODBC defined syntax for scalar functions.</span></span> 

<span data-ttu-id="9c980-105">Например, запрос возвращает все строки, в которых абсолютное значение изменения цены на акции превышает `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` пять.</span><span class="sxs-lookup"><span data-stu-id="9c980-105">For example, the query `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="9c980-106">Поддерживается подмножество определенных масштабарных функций ODBC.</span><span class="sxs-lookup"><span data-stu-id="9c980-106">A subset of the ODBC defined scalar functions is supported.</span></span> <span data-ttu-id="9c980-107">В следующей таблице перечислены поддерживаемые функции.</span><span class="sxs-lookup"><span data-stu-id="9c980-107">The following table lists the functions that are supported.</span></span>

<span data-ttu-id="9c980-108">Описание аргументов и полное объяснение синтаксиса побега для включаний функций в SQL см. в документации ODBC.</span><span class="sxs-lookup"><span data-stu-id="9c980-108">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="9c980-109">Функции string</span><span class="sxs-lookup"><span data-stu-id="9c980-109">String functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c980-110">ASCII</span><span class="sxs-lookup"><span data-stu-id="9c980-110">ASCII</span></span></p></td>
<td><p><span data-ttu-id="9c980-111">LENGTH</span><span class="sxs-lookup"><span data-stu-id="9c980-111">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="9c980-112">RTRIM</span><span class="sxs-lookup"><span data-stu-id="9c980-112">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c980-113">CHAR</span><span class="sxs-lookup"><span data-stu-id="9c980-113">CHAR</span></span></p></td>
<td><p><span data-ttu-id="9c980-114">LOCATE</span><span class="sxs-lookup"><span data-stu-id="9c980-114">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="9c980-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="9c980-115">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c980-116">CONCAT</span><span class="sxs-lookup"><span data-stu-id="9c980-116">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="9c980-117">LTRIM</span><span class="sxs-lookup"><span data-stu-id="9c980-117">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="9c980-118">SUBSTRING</span><span class="sxs-lookup"><span data-stu-id="9c980-118">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c980-119">LCASE</span><span class="sxs-lookup"><span data-stu-id="9c980-119">LCASE</span></span></p></td>
<td><p><span data-ttu-id="9c980-120">Правильно</span><span class="sxs-lookup"><span data-stu-id="9c980-120">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="9c980-121">UCASE</span><span class="sxs-lookup"><span data-stu-id="9c980-121">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c980-122">LEFT</span><span class="sxs-lookup"><span data-stu-id="9c980-122">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="9c980-123">Числимые функции</span><span class="sxs-lookup"><span data-stu-id="9c980-123">Numeric functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c980-124">ABS</span><span class="sxs-lookup"><span data-stu-id="9c980-124">ABS</span></span></p></td>
<td><p><span data-ttu-id="9c980-125">FLOOR</span><span class="sxs-lookup"><span data-stu-id="9c980-125">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="9c980-126">SIN</span><span class="sxs-lookup"><span data-stu-id="9c980-126">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c980-127">ATAN</span><span class="sxs-lookup"><span data-stu-id="9c980-127">ATAN</span></span></p></td>
<td><p><span data-ttu-id="9c980-128">LOG</span><span class="sxs-lookup"><span data-stu-id="9c980-128">LOG</span></span></p></td>
<td><p><span data-ttu-id="9c980-129">SQRT</span><span class="sxs-lookup"><span data-stu-id="9c980-129">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c980-130">ПОТОЛОК</span><span class="sxs-lookup"><span data-stu-id="9c980-130">CEILING</span></span></p></td>
<td><p><span data-ttu-id="9c980-131">POWER</span><span class="sxs-lookup"><span data-stu-id="9c980-131">POWER</span></span></p></td>
<td><p><span data-ttu-id="9c980-132">TAN</span><span class="sxs-lookup"><span data-stu-id="9c980-132">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c980-133">COS</span><span class="sxs-lookup"><span data-stu-id="9c980-133">COS</span></span></p></td>
<td><p><span data-ttu-id="9c980-134">RAND</span><span class="sxs-lookup"><span data-stu-id="9c980-134">RAND</span></span></p></td>
<td><p><span data-ttu-id="9c980-135">MOD</span><span class="sxs-lookup"><span data-stu-id="9c980-135">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c980-136">EXP</span><span class="sxs-lookup"><span data-stu-id="9c980-136">EXP</span></span></p></td>
<td><p><span data-ttu-id="9c980-137">SIGN</span><span class="sxs-lookup"><span data-stu-id="9c980-137">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="9c980-138">Функции & даты</span><span class="sxs-lookup"><span data-stu-id="9c980-138">Time & Date functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c980-139">CURDATE</span><span class="sxs-lookup"><span data-stu-id="9c980-139">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="9c980-140">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="9c980-140">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="9c980-141">MONTH</span><span class="sxs-lookup"><span data-stu-id="9c980-141">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c980-142">CURTIME</span><span class="sxs-lookup"><span data-stu-id="9c980-142">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="9c980-143">YEAR</span><span class="sxs-lookup"><span data-stu-id="9c980-143">YEAR</span></span></p></td>
<td><p><span data-ttu-id="9c980-144">НЕДЕЛЯ</span><span class="sxs-lookup"><span data-stu-id="9c980-144">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c980-145">NOW</span><span class="sxs-lookup"><span data-stu-id="9c980-145">NOW</span></span></p></td>
<td><p><span data-ttu-id="9c980-146">HOUR</span><span class="sxs-lookup"><span data-stu-id="9c980-146">HOUR</span></span></p></td>
<td><p><span data-ttu-id="9c980-147">QUARTER</span><span class="sxs-lookup"><span data-stu-id="9c980-147">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c980-148">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="9c980-148">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="9c980-149">MINUTE</span><span class="sxs-lookup"><span data-stu-id="9c980-149">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="9c980-150">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="9c980-150">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c980-151">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="9c980-151">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="9c980-152">SECOND</span><span class="sxs-lookup"><span data-stu-id="9c980-152">SECOND</span></span></p></td>
<td><p><span data-ttu-id="9c980-153">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="9c980-153">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="9c980-154">Преобразование типа данных</span><span class="sxs-lookup"><span data-stu-id="9c980-154">Data type conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c980-155">CONVERT</span><span class="sxs-lookup"><span data-stu-id="9c980-155">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="9c980-156">Строковые литеры можно преобразовать в следующие типы данных: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR и SQL_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="9c980-156">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

