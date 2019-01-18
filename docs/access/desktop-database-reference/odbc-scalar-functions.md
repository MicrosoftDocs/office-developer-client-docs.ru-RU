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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718037"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="b7a28-102">Скалярные функции ODBC</span><span class="sxs-lookup"><span data-stu-id="b7a28-102">ODBC scalar functions</span></span>

<span data-ttu-id="b7a28-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7a28-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7a28-104">Microsoft Access SQL поддерживает использование синтаксиса ODBC определенные скалярные функции.</span><span class="sxs-lookup"><span data-stu-id="b7a28-104">Microsoft Access SQL supports the use of the ODBC defined syntax for scalar functions.</span></span> 

<span data-ttu-id="b7a28-105">Например, запрос `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` возвращает строки, в которой было больше, чем пять абсолютного значения изменений в цену акции.</span><span class="sxs-lookup"><span data-stu-id="b7a28-105">For example, the query `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="b7a28-106">Поддерживается подмножество определенные скалярные функции ODBC.</span><span class="sxs-lookup"><span data-stu-id="b7a28-106">A subset of the ODBC defined scalar functions is supported.</span></span> <span data-ttu-id="b7a28-107">В следующей таблице перечислены функции, которые поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="b7a28-107">The following table lists the functions that are supported.</span></span>

<span data-ttu-id="b7a28-108">Для описания аргументов и объяснение синтаксиса escape-последовательности для включения функции в инструкции SQL обратитесь к документации ODBC.</span><span class="sxs-lookup"><span data-stu-id="b7a28-108">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="b7a28-109">Строковые функции</span><span class="sxs-lookup"><span data-stu-id="b7a28-109">String functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7a28-110">ASCII</span><span class="sxs-lookup"><span data-stu-id="b7a28-110">ASCII</span></span></p></td>
<td><p><span data-ttu-id="b7a28-111">ДЛИНА</span><span class="sxs-lookup"><span data-stu-id="b7a28-111">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="b7a28-112">RTRIM</span><span class="sxs-lookup"><span data-stu-id="b7a28-112">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7a28-113">(ЗНАК)</span><span class="sxs-lookup"><span data-stu-id="b7a28-113">CHAR</span></span></p></td>
<td><p><span data-ttu-id="b7a28-114">НАЙДИТЕ</span><span class="sxs-lookup"><span data-stu-id="b7a28-114">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="b7a28-115">ПРОБЕЛ</span><span class="sxs-lookup"><span data-stu-id="b7a28-115">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7a28-116">ОБЪЕДИНИТЬ</span><span class="sxs-lookup"><span data-stu-id="b7a28-116">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="b7a28-117">ФУНКЦИИ LTRIM</span><span class="sxs-lookup"><span data-stu-id="b7a28-117">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="b7a28-118">ПОДСТРОКИ</span><span class="sxs-lookup"><span data-stu-id="b7a28-118">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7a28-119">LCASE</span><span class="sxs-lookup"><span data-stu-id="b7a28-119">LCASE</span></span></p></td>
<td><p><span data-ttu-id="b7a28-120">Правильно</span><span class="sxs-lookup"><span data-stu-id="b7a28-120">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="b7a28-121">UCASE</span><span class="sxs-lookup"><span data-stu-id="b7a28-121">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7a28-122">СЛЕВА</span><span class="sxs-lookup"><span data-stu-id="b7a28-122">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="b7a28-123">Числовые функции</span><span class="sxs-lookup"><span data-stu-id="b7a28-123">Numeric functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7a28-124">ABS</span><span class="sxs-lookup"><span data-stu-id="b7a28-124">ABS</span></span></p></td>
<td><p><span data-ttu-id="b7a28-125">ЭТАЖ</span><span class="sxs-lookup"><span data-stu-id="b7a28-125">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="b7a28-126">SIN</span><span class="sxs-lookup"><span data-stu-id="b7a28-126">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7a28-127">ATAN</span><span class="sxs-lookup"><span data-stu-id="b7a28-127">ATAN</span></span></p></td>
<td><p><span data-ttu-id="b7a28-128">ЖУРНАЛ</span><span class="sxs-lookup"><span data-stu-id="b7a28-128">LOG</span></span></p></td>
<td><p><span data-ttu-id="b7a28-129">КОРЕНЬ</span><span class="sxs-lookup"><span data-stu-id="b7a28-129">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7a28-130">ПОТОЛОК</span><span class="sxs-lookup"><span data-stu-id="b7a28-130">CEILING</span></span></p></td>
<td><p><span data-ttu-id="b7a28-131">POWER</span><span class="sxs-lookup"><span data-stu-id="b7a28-131">POWER</span></span></p></td>
<td><p><span data-ttu-id="b7a28-132">TAN</span><span class="sxs-lookup"><span data-stu-id="b7a28-132">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7a28-133">COS</span><span class="sxs-lookup"><span data-stu-id="b7a28-133">COS</span></span></p></td>
<td><p><span data-ttu-id="b7a28-134">РЭНД</span><span class="sxs-lookup"><span data-stu-id="b7a28-134">RAND</span></span></p></td>
<td><p><span data-ttu-id="b7a28-135">MOD</span><span class="sxs-lookup"><span data-stu-id="b7a28-135">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7a28-136">EXP</span><span class="sxs-lookup"><span data-stu-id="b7a28-136">EXP</span></span></p></td>
<td><p><span data-ttu-id="b7a28-137">ЗНАК</span><span class="sxs-lookup"><span data-stu-id="b7a28-137">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="b7a28-138">Функции даты & времени</span><span class="sxs-lookup"><span data-stu-id="b7a28-138">Time & Date functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7a28-139">CURDATE</span><span class="sxs-lookup"><span data-stu-id="b7a28-139">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="b7a28-140">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b7a28-140">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="b7a28-141">МЕСЯЦ</span><span class="sxs-lookup"><span data-stu-id="b7a28-141">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7a28-142">CURTIME</span><span class="sxs-lookup"><span data-stu-id="b7a28-142">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="b7a28-143">ГОД</span><span class="sxs-lookup"><span data-stu-id="b7a28-143">YEAR</span></span></p></td>
<td><p><span data-ttu-id="b7a28-144">НЕДЕЛИ</span><span class="sxs-lookup"><span data-stu-id="b7a28-144">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7a28-145">СЕЙЧАС</span><span class="sxs-lookup"><span data-stu-id="b7a28-145">NOW</span></span></p></td>
<td><p><span data-ttu-id="b7a28-146">ЧАС</span><span class="sxs-lookup"><span data-stu-id="b7a28-146">HOUR</span></span></p></td>
<td><p><span data-ttu-id="b7a28-147">КВАРТАЛ</span><span class="sxs-lookup"><span data-stu-id="b7a28-147">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7a28-148">ДЕНЬ МЕСЯЦА</span><span class="sxs-lookup"><span data-stu-id="b7a28-148">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="b7a28-149">МИНУТЫ</span><span class="sxs-lookup"><span data-stu-id="b7a28-149">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="b7a28-150">ФУНКЦИЯ MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="b7a28-150">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7a28-151">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="b7a28-151">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="b7a28-152">СЕКУНДЫ</span><span class="sxs-lookup"><span data-stu-id="b7a28-152">SECOND</span></span></p></td>
<td><p><span data-ttu-id="b7a28-153">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="b7a28-153">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="b7a28-154">Преобразования типов данных</span><span class="sxs-lookup"><span data-stu-id="b7a28-154">Data type conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7a28-155">ПРЕОБРАЗОВАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7a28-155">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="b7a28-156">Строковые литералы можно преобразовать в следующие типы данных: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR и SQL_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="b7a28-156">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

