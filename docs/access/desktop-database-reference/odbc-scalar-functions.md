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
# <a name="odbc-scalar-functions"></a><span data-ttu-id="4df85-102">Скалярные функции ODBC</span><span class="sxs-lookup"><span data-stu-id="4df85-102">ODBC scalar functions</span></span>

<span data-ttu-id="4df85-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4df85-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4df85-104">Microsoft Access SQL поддерживает использование определенного синтаксиса ODBC для скалярных функций.</span><span class="sxs-lookup"><span data-stu-id="4df85-104">Microsoft Access SQL supports the use of the ODBC defined syntax for scalar functions.</span></span> 

<span data-ttu-id="4df85-105">Например, запрос `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` возвращает все строки, где абсолютное значение изменения цены на акции превышает 5.</span><span class="sxs-lookup"><span data-stu-id="4df85-105">For example, the query `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="4df85-106">Поддерживается подмножество определенных в ODBC скалярных функций.</span><span class="sxs-lookup"><span data-stu-id="4df85-106">A subset of the ODBC defined scalar functions is supported.</span></span> <span data-ttu-id="4df85-107">В следующей таблице перечислены поддерживаемые функции.</span><span class="sxs-lookup"><span data-stu-id="4df85-107">The following table lists the functions that are supported.</span></span>

<span data-ttu-id="4df85-108">Описание аргументов и полное описание синтаксиса escape для включения функций в инструкцию SQL см в документации по ODBC.</span><span class="sxs-lookup"><span data-stu-id="4df85-108">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="4df85-109">Строковые функции</span><span class="sxs-lookup"><span data-stu-id="4df85-109">String functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4df85-110">ФОРМАТ</span><span class="sxs-lookup"><span data-stu-id="4df85-110">ASCII</span></span></p></td>
<td><p><span data-ttu-id="4df85-111">ВРЕМЕНИ</span><span class="sxs-lookup"><span data-stu-id="4df85-111">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="4df85-112">RTRIM</span><span class="sxs-lookup"><span data-stu-id="4df85-112">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4df85-113">РАЗДЕЛИТЕЛ</span><span class="sxs-lookup"><span data-stu-id="4df85-113">CHAR</span></span></p></td>
<td><p><span data-ttu-id="4df85-114">РАЗДЕЛ</span><span class="sxs-lookup"><span data-stu-id="4df85-114">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="4df85-115">ПРОБЕЛ</span><span class="sxs-lookup"><span data-stu-id="4df85-115">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4df85-116">ЗНАЧЕНИЙ</span><span class="sxs-lookup"><span data-stu-id="4df85-116">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="4df85-117">LTRIM</span><span class="sxs-lookup"><span data-stu-id="4df85-117">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="4df85-118">SUBSTRING</span><span class="sxs-lookup"><span data-stu-id="4df85-118">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4df85-119">LCASE</span><span class="sxs-lookup"><span data-stu-id="4df85-119">LCASE</span></span></p></td>
<td><p><span data-ttu-id="4df85-120">Правильно</span><span class="sxs-lookup"><span data-stu-id="4df85-120">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="4df85-121">УКАСЕ</span><span class="sxs-lookup"><span data-stu-id="4df85-121">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4df85-122">ЛЕВЫЙ</span><span class="sxs-lookup"><span data-stu-id="4df85-122">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="4df85-123">Числовые функции</span><span class="sxs-lookup"><span data-stu-id="4df85-123">Numeric functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4df85-124">ABS</span><span class="sxs-lookup"><span data-stu-id="4df85-124">ABS</span></span></p></td>
<td><p><span data-ttu-id="4df85-125">КУХОН</span><span class="sxs-lookup"><span data-stu-id="4df85-125">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="4df85-126">Синус</span><span class="sxs-lookup"><span data-stu-id="4df85-126">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4df85-127">ATAN</span><span class="sxs-lookup"><span data-stu-id="4df85-127">ATAN</span></span></p></td>
<td><p><span data-ttu-id="4df85-128">ВХОДЕ</span><span class="sxs-lookup"><span data-stu-id="4df85-128">LOG</span></span></p></td>
<td><p><span data-ttu-id="4df85-129">КОРЕНЬ</span><span class="sxs-lookup"><span data-stu-id="4df85-129">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4df85-130">Г</span><span class="sxs-lookup"><span data-stu-id="4df85-130">CEILING</span></span></p></td>
<td><p><span data-ttu-id="4df85-131">ПОТРЕБЛЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4df85-131">POWER</span></span></p></td>
<td><p><span data-ttu-id="4df85-132">TAN</span><span class="sxs-lookup"><span data-stu-id="4df85-132">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4df85-133">COS</span><span class="sxs-lookup"><span data-stu-id="4df85-133">COS</span></span></p></td>
<td><p><span data-ttu-id="4df85-134">СЛЧИС</span><span class="sxs-lookup"><span data-stu-id="4df85-134">RAND</span></span></p></td>
<td><p><span data-ttu-id="4df85-135">MOD</span><span class="sxs-lookup"><span data-stu-id="4df85-135">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4df85-136">Кнопка</span><span class="sxs-lookup"><span data-stu-id="4df85-136">EXP</span></span></p></td>
<td><p><span data-ttu-id="4df85-137">ДОЛЛАР</span><span class="sxs-lookup"><span data-stu-id="4df85-137">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="4df85-138">Функции time _Амп_ Date</span><span class="sxs-lookup"><span data-stu-id="4df85-138">Time & Date functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4df85-139">КУРДАТЕ</span><span class="sxs-lookup"><span data-stu-id="4df85-139">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="4df85-140">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="4df85-140">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="4df85-141">MONTH</span><span class="sxs-lookup"><span data-stu-id="4df85-141">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4df85-142">КУРТИМЕ</span><span class="sxs-lookup"><span data-stu-id="4df85-142">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="4df85-143">YEAR</span><span class="sxs-lookup"><span data-stu-id="4df85-143">YEAR</span></span></p></td>
<td><p><span data-ttu-id="4df85-144">Я</span><span class="sxs-lookup"><span data-stu-id="4df85-144">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4df85-145">НАСТРОЕН</span><span class="sxs-lookup"><span data-stu-id="4df85-145">NOW</span></span></p></td>
<td><p><span data-ttu-id="4df85-146">HOUR</span><span class="sxs-lookup"><span data-stu-id="4df85-146">HOUR</span></span></p></td>
<td><p><span data-ttu-id="4df85-147">КВАРТАЛЕ</span><span class="sxs-lookup"><span data-stu-id="4df85-147">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4df85-148">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="4df85-148">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="4df85-149">MINUTE</span><span class="sxs-lookup"><span data-stu-id="4df85-149">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="4df85-150">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="4df85-150">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4df85-151">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="4df85-151">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="4df85-152">SECOND</span><span class="sxs-lookup"><span data-stu-id="4df85-152">SECOND</span></span></p></td>
<td><p><span data-ttu-id="4df85-153">ДАЙНАМЕ</span><span class="sxs-lookup"><span data-stu-id="4df85-153">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="4df85-154">Преобразование типов данных</span><span class="sxs-lookup"><span data-stu-id="4df85-154">Data type conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4df85-155">CONVERT</span><span class="sxs-lookup"><span data-stu-id="4df85-155">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="4df85-156">Строковые литералы могут быть преобразованы в следующие типы данных: СКЛ_ФЛОАТ, СКЛ_ДАУБЛЕ, СКЛ_НУМЕРИК, СКЛ_ИНТЕЖЕР, СКЛ_РЕАЛ, СКЛ_СМАЛЛИНТ, СКЛ_ВАРЧАР и СКЛ_ДАТЕТИМЕ.</span><span class="sxs-lookup"><span data-stu-id="4df85-156">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

