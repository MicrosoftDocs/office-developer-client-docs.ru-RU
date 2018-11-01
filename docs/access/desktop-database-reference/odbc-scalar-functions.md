---
title: Скалярные функции ODBC
TOCTitle: ODBC Scalar Functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 21e6000e8620011f5f6f0c2481bb9c03fd71bab5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887959"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="997ce-102">Скалярные функции ODBC</span><span class="sxs-lookup"><span data-stu-id="997ce-102">ODBC Scalar Functions</span></span>


<span data-ttu-id="997ce-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="997ce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="997ce-104">Microsoft® Access SQL поддерживает использование синтаксиса ODBC определенные скалярные функции.</span><span class="sxs-lookup"><span data-stu-id="997ce-104">Microsoft® Access SQL supports the use of the ODBC defined syntax for scalar functions.</span></span> <span data-ttu-id="997ce-105">Например следующий запрос:</span><span class="sxs-lookup"><span data-stu-id="997ce-105">For example, the query:</span></span>

<span data-ttu-id="997ce-106">Выбор DAILYCLOSE, DAILYCHANGE из DAILYQUOTE ГДЕ {fn ABS(DAILYCHANGE)} \> 5</span><span class="sxs-lookup"><span data-stu-id="997ce-106">SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} \> 5</span></span>

<span data-ttu-id="997ce-107">Возвращает строки, в которой было больше, чем пять абсолютного значения изменений в цену акции.</span><span class="sxs-lookup"><span data-stu-id="997ce-107">Would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="997ce-108">Поддерживается подмножество определенные скалярные функции ODBC.</span><span class="sxs-lookup"><span data-stu-id="997ce-108">A subset of the ODBC defined scalar functions is supported.</span></span> <span data-ttu-id="997ce-109">В следующей таблице перечислены функции, которые поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="997ce-109">The following table lists the functions that are supported.</span></span>

<span data-ttu-id="997ce-110">Для описания аргументов и объяснение синтаксиса escape-последовательности для включения функции в инструкции SQL обратитесь к документации ODBC.</span><span class="sxs-lookup"><span data-stu-id="997ce-110">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="997ce-111">Строковые функции</span><span class="sxs-lookup"><span data-stu-id="997ce-111">String Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="997ce-112">ASCII</span><span class="sxs-lookup"><span data-stu-id="997ce-112">ASCII</span></span></p></td>
<td><p><span data-ttu-id="997ce-113">ДЛИНА</span><span class="sxs-lookup"><span data-stu-id="997ce-113">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="997ce-114">RTRIM</span><span class="sxs-lookup"><span data-stu-id="997ce-114">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="997ce-115">(ЗНАК)</span><span class="sxs-lookup"><span data-stu-id="997ce-115">CHAR</span></span></p></td>
<td><p><span data-ttu-id="997ce-116">НАЙДИТЕ</span><span class="sxs-lookup"><span data-stu-id="997ce-116">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="997ce-117">ПРОБЕЛ</span><span class="sxs-lookup"><span data-stu-id="997ce-117">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="997ce-118">ОБЪЕДИНИТЬ</span><span class="sxs-lookup"><span data-stu-id="997ce-118">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="997ce-119">ФУНКЦИИ LTRIM</span><span class="sxs-lookup"><span data-stu-id="997ce-119">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="997ce-120">ПОДСТРОКИ</span><span class="sxs-lookup"><span data-stu-id="997ce-120">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="997ce-121">LCASE</span><span class="sxs-lookup"><span data-stu-id="997ce-121">LCASE</span></span></p></td>
<td><p><span data-ttu-id="997ce-122">Правильно</span><span class="sxs-lookup"><span data-stu-id="997ce-122">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="997ce-123">UCASE</span><span class="sxs-lookup"><span data-stu-id="997ce-123">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="997ce-124">СЛЕВА</span><span class="sxs-lookup"><span data-stu-id="997ce-124">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="997ce-125">Числовые функции</span><span class="sxs-lookup"><span data-stu-id="997ce-125">Numeric Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="997ce-126">ABS</span><span class="sxs-lookup"><span data-stu-id="997ce-126">ABS</span></span></p></td>
<td><p><span data-ttu-id="997ce-127">ЭТАЖ</span><span class="sxs-lookup"><span data-stu-id="997ce-127">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="997ce-128">SIN</span><span class="sxs-lookup"><span data-stu-id="997ce-128">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="997ce-129">ATAN</span><span class="sxs-lookup"><span data-stu-id="997ce-129">ATAN</span></span></p></td>
<td><p><span data-ttu-id="997ce-130">ЖУРНАЛ</span><span class="sxs-lookup"><span data-stu-id="997ce-130">LOG</span></span></p></td>
<td><p><span data-ttu-id="997ce-131">КОРЕНЬ</span><span class="sxs-lookup"><span data-stu-id="997ce-131">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="997ce-132">ПОТОЛОК</span><span class="sxs-lookup"><span data-stu-id="997ce-132">CEILING</span></span></p></td>
<td><p><span data-ttu-id="997ce-133">POWER</span><span class="sxs-lookup"><span data-stu-id="997ce-133">POWER</span></span></p></td>
<td><p><span data-ttu-id="997ce-134">TAN</span><span class="sxs-lookup"><span data-stu-id="997ce-134">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="997ce-135">COS</span><span class="sxs-lookup"><span data-stu-id="997ce-135">COS</span></span></p></td>
<td><p><span data-ttu-id="997ce-136">РЭНД</span><span class="sxs-lookup"><span data-stu-id="997ce-136">RAND</span></span></p></td>
<td><p><span data-ttu-id="997ce-137">MOD</span><span class="sxs-lookup"><span data-stu-id="997ce-137">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="997ce-138">EXP</span><span class="sxs-lookup"><span data-stu-id="997ce-138">EXP</span></span></p></td>
<td><p><span data-ttu-id="997ce-139">ЗНАК</span><span class="sxs-lookup"><span data-stu-id="997ce-139">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="997ce-140">Функции обработки даты и времени</span><span class="sxs-lookup"><span data-stu-id="997ce-140">Time & Date Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="997ce-141">CURDATE</span><span class="sxs-lookup"><span data-stu-id="997ce-141">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="997ce-142">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="997ce-142">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="997ce-143">МЕСЯЦ</span><span class="sxs-lookup"><span data-stu-id="997ce-143">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="997ce-144">CURTIME</span><span class="sxs-lookup"><span data-stu-id="997ce-144">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="997ce-145">ГОД</span><span class="sxs-lookup"><span data-stu-id="997ce-145">YEAR</span></span></p></td>
<td><p><span data-ttu-id="997ce-146">НЕДЕЛИ</span><span class="sxs-lookup"><span data-stu-id="997ce-146">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="997ce-147">СЕЙЧАС</span><span class="sxs-lookup"><span data-stu-id="997ce-147">NOW</span></span></p></td>
<td><p><span data-ttu-id="997ce-148">ЧАС</span><span class="sxs-lookup"><span data-stu-id="997ce-148">HOUR</span></span></p></td>
<td><p><span data-ttu-id="997ce-149">КВАРТАЛ</span><span class="sxs-lookup"><span data-stu-id="997ce-149">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="997ce-150">ДЕНЬ МЕСЯЦА</span><span class="sxs-lookup"><span data-stu-id="997ce-150">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="997ce-151">МИНУТЫ</span><span class="sxs-lookup"><span data-stu-id="997ce-151">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="997ce-152">ФУНКЦИЯ MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="997ce-152">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="997ce-153">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="997ce-153">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="997ce-154">СЕКУНДЫ</span><span class="sxs-lookup"><span data-stu-id="997ce-154">SECOND</span></span></p></td>
<td><p><span data-ttu-id="997ce-155">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="997ce-155">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="997ce-156">Преобразования типов данных</span><span class="sxs-lookup"><span data-stu-id="997ce-156">Data Type Conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="997ce-157">ПРЕОБРАЗОВАНИЕ</span><span class="sxs-lookup"><span data-stu-id="997ce-157">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="997ce-158">Строковые литералы можно преобразовать в следующие типы данных: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR и SQL_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="997ce-158">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

