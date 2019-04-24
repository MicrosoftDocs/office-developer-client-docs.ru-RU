---
title: Метод CreateRecordset (RDS)
TOCTitle: CreateRecordset method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3dda0840617c32e9dceea3bd1baa362c5652a373
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295340"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="f934f-102">Метод CreateRecordset (RDS)</span><span class="sxs-lookup"><span data-stu-id="f934f-102">CreateRecordset method (RDS)</span></span>

<span data-ttu-id="f934f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f934f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f934f-104">Создает пустой отключенный [набор записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f934f-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f934f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f934f-105">Syntax</span></span>

<span data-ttu-id="f934f-106">*объект*. CreateRecordset (*колумнинфос*)</span><span class="sxs-lookup"><span data-stu-id="f934f-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="f934f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f934f-107">Parameters</span></span>

|<span data-ttu-id="f934f-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="f934f-108">Parameter</span></span>|<span data-ttu-id="f934f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f934f-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f934f-110">*Object*</span><span class="sxs-lookup"><span data-stu-id="f934f-110">*Object*</span></span> |<span data-ttu-id="f934f-111">Объектная переменная, представляющая объект [рдссервер.](datafactory-object-rdsserver.md) DataObject или [RDS. Объект управления](datacontrol-object-rds.md) DataObject.</span><span class="sxs-lookup"><span data-stu-id="f934f-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="f934f-112">*Колумнсинфос*</span><span class="sxs-lookup"><span data-stu-id="f934f-112">*ColumnsInfos*</span></span> |<span data-ttu-id="f934f-113">Массив **Variant** атрибутов, который определяет каждый столбец в созданном **наборе записей** .</span><span class="sxs-lookup"><span data-stu-id="f934f-113">A **Variant** array of attributes that defines each column in the **Recordset** created.</span></span> <span data-ttu-id="f934f-114">Каждое определение столбца содержит массив из четырех обязательных атрибутов и один необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="f934f-114">Each column definition contains an array of four required attributes and one optional attribute.</span></span> <span data-ttu-id="f934f-115">После этого набор массивов столбцов будет сгруппирован в массив, который определяет **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="f934f-115">The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span> <span data-ttu-id="f934f-116">Список атрибутов представлен в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f934f-116">For a list of attributes, see the following table.</span></span>|

### <a name="variant-array-attributes"></a><span data-ttu-id="f934f-117">Атрибуты массива Variant</span><span class="sxs-lookup"><span data-stu-id="f934f-117">Variant array attributes</span></span>

|<span data-ttu-id="f934f-118">Атрибут</span><span class="sxs-lookup"><span data-stu-id="f934f-118">Attribute</span></span>|<span data-ttu-id="f934f-119">Описание</span><span class="sxs-lookup"><span data-stu-id="f934f-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f934f-120">Имя</span><span class="sxs-lookup"><span data-stu-id="f934f-120">Name</span></span> |<span data-ttu-id="f934f-121">Имя заголовка столбца.</span><span class="sxs-lookup"><span data-stu-id="f934f-121">Name of the column header.</span></span>|
|<span data-ttu-id="f934f-122">Тип</span><span class="sxs-lookup"><span data-stu-id="f934f-122">Type</span></span> |<span data-ttu-id="f934f-123">Целое число типа данных.</span><span class="sxs-lookup"><span data-stu-id="f934f-123">Integer of the data type.</span></span>|
|<span data-ttu-id="f934f-124">Размер</span><span class="sxs-lookup"><span data-stu-id="f934f-124">Size</span></span> |<span data-ttu-id="f934f-125">Целое значение ширины в символах, независимо от типа данных.</span><span class="sxs-lookup"><span data-stu-id="f934f-125">Integer of the width in characters, regardless of data type.</span></span>|
|<span data-ttu-id="f934f-126">Возможность принимать значения NULL</span><span class="sxs-lookup"><span data-stu-id="f934f-126">Nullability</span></span> |<span data-ttu-id="f934f-127">Логическое значение.</span><span class="sxs-lookup"><span data-stu-id="f934f-127">Boolean value.</span></span>|
|<span data-ttu-id="f934f-128">Scale (необязательно)</span><span class="sxs-lookup"><span data-stu-id="f934f-128">Scale (optional)</span></span> |<span data-ttu-id="f934f-129">Этот необязательный атрибут определяет масштаб для числовых полей.</span><span class="sxs-lookup"><span data-stu-id="f934f-129">This optional attribute defines the scale for numeric fields.</span></span> <span data-ttu-id="f934f-130">Если это значение не указано, числовые значения будут сокращены до шкалы 3.</span><span class="sxs-lookup"><span data-stu-id="f934f-130">If this value is not specified, numeric values will be truncated to a scale of three.</span></span> <span data-ttu-id="f934f-131">На точность не влияет, но количество цифр после десятичной точки будет укорочено до 3.</span><span class="sxs-lookup"><span data-stu-id="f934f-131">Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f934f-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="f934f-132">Remarks</span></span>

<span data-ttu-id="f934f-133">Серверный бизнес-объект может заполнить полученный **набор записей** данными из поставщика данных, отличного от OLE DB, например из файла операционной системы, содержащего котировки акций.</span><span class="sxs-lookup"><span data-stu-id="f934f-133">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="f934f-134">В следующей таблице приведены значения [DataTypeEnum](datatypeenum.md) , поддерживаемые методом **CreateRecordset** .</span><span class="sxs-lookup"><span data-stu-id="f934f-134">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method.</span></span> <span data-ttu-id="f934f-135">В списке указан номер ссылки, используемый для определения полей.</span><span class="sxs-lookup"><span data-stu-id="f934f-135">The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="f934f-136">Каждый тип данных имеет фиксированную или переменную длину.</span><span class="sxs-lookup"><span data-stu-id="f934f-136">Each of the data types is either fixed length or variable length.</span></span> <span data-ttu-id="f934f-137">Типы фиксированной длины должны определяться размером – 1, так как размер предварительно определен, а определение размера по-прежнему требуется.</span><span class="sxs-lookup"><span data-stu-id="f934f-137">Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required.</span></span> <span data-ttu-id="f934f-138">Типы данных переменной длины допускают размер от 1 до 32767.</span><span class="sxs-lookup"><span data-stu-id="f934f-138">Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="f934f-139">Для некоторых типов данных переменных тип может быть приведен к типу, указанному в столбце подСтановки.</span><span class="sxs-lookup"><span data-stu-id="f934f-139">For some of the variable data types, the type may be coerced to the type noted in the Substitution column.</span></span> <span data-ttu-id="f934f-140">Подстановки не отображаются до тех пор, пока не будет создан и заполнен **набор записей** .</span><span class="sxs-lookup"><span data-stu-id="f934f-140">You won't see the substitutions until after the **Recordset** is created and filled.</span></span> <span data-ttu-id="f934f-141">При необходимости вы можете проверить фактический тип данных.</span><span class="sxs-lookup"><span data-stu-id="f934f-141">Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f934f-142">Длина</span><span class="sxs-lookup"><span data-stu-id="f934f-142">Length</span></span></p></th>
<th><p><span data-ttu-id="f934f-143">Константа</span><span class="sxs-lookup"><span data-stu-id="f934f-143">Constant</span></span></p></th>
<th><p><span data-ttu-id="f934f-144">Номер</span><span class="sxs-lookup"><span data-stu-id="f934f-144">Number</span></span></p></th>
<th><p><span data-ttu-id="f934f-145">Подстановки</span><span class="sxs-lookup"><span data-stu-id="f934f-145">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f934f-146">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-147"><strong>Адтининт</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-147"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-148">столбцов</span><span class="sxs-lookup"><span data-stu-id="f934f-148">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f934f-149">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-150"><strong>Адсмаллинт</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-150"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-151">2</span><span class="sxs-lookup"><span data-stu-id="f934f-151">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f934f-152">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-153"><strong>Адинтежер</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-153"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-154">4</span><span class="sxs-lookup"><span data-stu-id="f934f-154">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f934f-155">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-156"><strong>Адбигинт</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-156"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-157">двадцать</span><span class="sxs-lookup"><span data-stu-id="f934f-157">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f934f-158">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-159"><strong>Адунсигнедтининт</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-159"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-160">17</span><span class="sxs-lookup"><span data-stu-id="f934f-160">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f934f-161">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-162"><strong>Адунсигнедсмаллинт</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-162"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-163">0,18</span><span class="sxs-lookup"><span data-stu-id="f934f-163">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f934f-164">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-165"><strong>Адунсигнединт</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-165"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-166">19</span><span class="sxs-lookup"><span data-stu-id="f934f-166">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f934f-167">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-168"><strong>Адунсигнедбигинт</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-168"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-169">21</span><span class="sxs-lookup"><span data-stu-id="f934f-169">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f934f-170">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-171"><strong>Адсингле</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-171"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-172">SP4</span><span class="sxs-lookup"><span data-stu-id="f934f-172">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f934f-173">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-174"><strong>Аддаубле</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-174"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-175">17:00</span><span class="sxs-lookup"><span data-stu-id="f934f-175">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f934f-176">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-177"><strong>Адкурренци</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-177"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-178">ICMPv6</span><span class="sxs-lookup"><span data-stu-id="f934f-178">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f934f-179">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-180"><strong>АддеЦимал</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-180"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-181">14</span><span class="sxs-lookup"><span data-stu-id="f934f-181">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f934f-182">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-183"><strong>Аднумерик</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-183"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-184">131</span><span class="sxs-lookup"><span data-stu-id="f934f-184">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f934f-185">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-186"><strong>Адбулеан</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-186"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-187">-11:00</span><span class="sxs-lookup"><span data-stu-id="f934f-187">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f934f-188">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-189"><strong>Адеррор</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-189"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-190">десяти</span><span class="sxs-lookup"><span data-stu-id="f934f-190">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f934f-191">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-192"><strong>Адгуид</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-192"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-193">72</span><span class="sxs-lookup"><span data-stu-id="f934f-193">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f934f-194">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-195"><strong>Аддате</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-195"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-196">см</span><span class="sxs-lookup"><span data-stu-id="f934f-196">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f934f-197">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-198"><strong>Аддбдате</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-198"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-199">133</span><span class="sxs-lookup"><span data-stu-id="f934f-199">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f934f-200">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-201"><strong>Аддбтиме</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-201"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-202">134</span><span class="sxs-lookup"><span data-stu-id="f934f-202">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f934f-203">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f934f-203">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f934f-204"><strong>Аддбтиместамп</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-204"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-205">135</span><span class="sxs-lookup"><span data-stu-id="f934f-205">135</span></span></p></td>
<td><p><span data-ttu-id="f934f-206">см</span><span class="sxs-lookup"><span data-stu-id="f934f-206">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f934f-207">Переменная</span><span class="sxs-lookup"><span data-stu-id="f934f-207">Variable</span></span></p></td>
<td><p><span data-ttu-id="f934f-208"><strong>Адбстр</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-208"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-209">8,5</span><span class="sxs-lookup"><span data-stu-id="f934f-209">8</span></span></p></td>
<td><p><span data-ttu-id="f934f-210">130</span><span class="sxs-lookup"><span data-stu-id="f934f-210">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f934f-211">Переменная</span><span class="sxs-lookup"><span data-stu-id="f934f-211">Variable</span></span></p></td>
<td><p><span data-ttu-id="f934f-212"><strong>Адчар</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-212"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-213">129</span><span class="sxs-lookup"><span data-stu-id="f934f-213">129</span></span></p></td>
<td><p><span data-ttu-id="f934f-214">200</span><span class="sxs-lookup"><span data-stu-id="f934f-214">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f934f-215">Переменная</span><span class="sxs-lookup"><span data-stu-id="f934f-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="f934f-216"><strong>Адварчар</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-216"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-217">200</span><span class="sxs-lookup"><span data-stu-id="f934f-217">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f934f-218">Переменная</span><span class="sxs-lookup"><span data-stu-id="f934f-218">Variable</span></span></p></td>
<td><p><span data-ttu-id="f934f-219"><strong>Адлонгварчар</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-219"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-220">201</span><span class="sxs-lookup"><span data-stu-id="f934f-220">201</span></span></p></td>
<td><p><span data-ttu-id="f934f-221">200</span><span class="sxs-lookup"><span data-stu-id="f934f-221">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f934f-222">Переменная</span><span class="sxs-lookup"><span data-stu-id="f934f-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="f934f-223"><strong>Адвчар</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-223"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-224">130</span><span class="sxs-lookup"><span data-stu-id="f934f-224">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f934f-225">Переменная</span><span class="sxs-lookup"><span data-stu-id="f934f-225">Variable</span></span></p></td>
<td><p><span data-ttu-id="f934f-226"><strong>Адварвчар</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-226"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-227">202</span><span class="sxs-lookup"><span data-stu-id="f934f-227">202</span></span></p></td>
<td><p><span data-ttu-id="f934f-228">130</span><span class="sxs-lookup"><span data-stu-id="f934f-228">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f934f-229">Переменная</span><span class="sxs-lookup"><span data-stu-id="f934f-229">Variable</span></span></p></td>
<td><p><span data-ttu-id="f934f-230"><strong>Адлонгварвчар</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-230"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-231">203</span><span class="sxs-lookup"><span data-stu-id="f934f-231">203</span></span></p></td>
<td><p><span data-ttu-id="f934f-232">130</span><span class="sxs-lookup"><span data-stu-id="f934f-232">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f934f-233">Переменная</span><span class="sxs-lookup"><span data-stu-id="f934f-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="f934f-234"><strong>Адбинари</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-234"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-235">128</span><span class="sxs-lookup"><span data-stu-id="f934f-235">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f934f-236">Переменная</span><span class="sxs-lookup"><span data-stu-id="f934f-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="f934f-237"><strong>Адварбинари</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-237"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-238">204</span><span class="sxs-lookup"><span data-stu-id="f934f-238">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f934f-239">Переменная</span><span class="sxs-lookup"><span data-stu-id="f934f-239">Variable</span></span></p></td>
<td><p><span data-ttu-id="f934f-240"><strong>Адлонгварбинари</strong></span><span class="sxs-lookup"><span data-stu-id="f934f-240"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f934f-241">205</span><span class="sxs-lookup"><span data-stu-id="f934f-241">205</span></span></p></td>
<td><p><span data-ttu-id="f934f-242">204</span><span class="sxs-lookup"><span data-stu-id="f934f-242">204</span></span></p></td>
</tr>
</tbody>
</table>

