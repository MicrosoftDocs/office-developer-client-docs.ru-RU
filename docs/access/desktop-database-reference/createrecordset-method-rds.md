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
# <a name="createrecordset-method-rds"></a><span data-ttu-id="5eedd-102">Метод CreateRecordset (RDS)</span><span class="sxs-lookup"><span data-stu-id="5eedd-102">CreateRecordset method (RDS)</span></span>

<span data-ttu-id="5eedd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5eedd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5eedd-104">Создает пустой отключенный [набор записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5eedd-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5eedd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5eedd-105">Syntax</span></span>

<span data-ttu-id="5eedd-106">*объект*. CreateRecordset (*колумнинфос*)</span><span class="sxs-lookup"><span data-stu-id="5eedd-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="5eedd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5eedd-107">Parameters</span></span>

|<span data-ttu-id="5eedd-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="5eedd-108">Parameter</span></span>|<span data-ttu-id="5eedd-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5eedd-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5eedd-110">*Object*</span><span class="sxs-lookup"><span data-stu-id="5eedd-110">*Object*</span></span> |<span data-ttu-id="5eedd-111">Объектная переменная, представляющая объект [рдссервер.](datafactory-object-rdsserver.md) DataObject или [RDS. Объект управления](datacontrol-object-rds.md) DataObject.</span><span class="sxs-lookup"><span data-stu-id="5eedd-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="5eedd-112">*колумнсинфос*</span><span class="sxs-lookup"><span data-stu-id="5eedd-112">*ColumnsInfos*</span></span> |<span data-ttu-id="5eedd-113">Массив **Variant** атрибутов, который определяет каждый столбец в созданном **наборе записей** .</span><span class="sxs-lookup"><span data-stu-id="5eedd-113">A **Variant** array of attributes that defines each column in the **Recordset** created.</span></span> <span data-ttu-id="5eedd-114">Каждое определение столбца содержит массив из четырех обязательных атрибутов и один необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="5eedd-114">Each column definition contains an array of four required attributes and one optional attribute.</span></span> <span data-ttu-id="5eedd-115">После этого набор массивов столбцов будет сгруппирован в массив, который определяет **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="5eedd-115">The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span> <span data-ttu-id="5eedd-116">Список атрибутов представлен в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5eedd-116">For a list of attributes, see the following table.</span></span>|

### <a name="variant-array-attributes"></a><span data-ttu-id="5eedd-117">Атрибуты массива Variant</span><span class="sxs-lookup"><span data-stu-id="5eedd-117">Variant array attributes</span></span>

|<span data-ttu-id="5eedd-118">Атрибут</span><span class="sxs-lookup"><span data-stu-id="5eedd-118">Attribute</span></span>|<span data-ttu-id="5eedd-119">Описание</span><span class="sxs-lookup"><span data-stu-id="5eedd-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5eedd-120">Имя</span><span class="sxs-lookup"><span data-stu-id="5eedd-120">Name</span></span> |<span data-ttu-id="5eedd-121">Имя заголовка столбца.</span><span class="sxs-lookup"><span data-stu-id="5eedd-121">Name of the column header.</span></span>|
|<span data-ttu-id="5eedd-122">Тип</span><span class="sxs-lookup"><span data-stu-id="5eedd-122">Type</span></span> |<span data-ttu-id="5eedd-123">Целое число типа данных.</span><span class="sxs-lookup"><span data-stu-id="5eedd-123">Integer of the data type.</span></span>|
|<span data-ttu-id="5eedd-124">Размер</span><span class="sxs-lookup"><span data-stu-id="5eedd-124">Size</span></span> |<span data-ttu-id="5eedd-125">Целое значение ширины в символах, независимо от типа данных.</span><span class="sxs-lookup"><span data-stu-id="5eedd-125">Integer of the width in characters, regardless of data type.</span></span>|
|<span data-ttu-id="5eedd-126">Возможность принимать значения NULL</span><span class="sxs-lookup"><span data-stu-id="5eedd-126">Nullability</span></span> |<span data-ttu-id="5eedd-127">Логическое значение.</span><span class="sxs-lookup"><span data-stu-id="5eedd-127">Boolean value.</span></span>|
|<span data-ttu-id="5eedd-128">Scale (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5eedd-128">Scale (optional)</span></span> |<span data-ttu-id="5eedd-129">Этот необязательный атрибут определяет масштаб для числовых полей.</span><span class="sxs-lookup"><span data-stu-id="5eedd-129">This optional attribute defines the scale for numeric fields.</span></span> <span data-ttu-id="5eedd-130">Если это значение не указано, числовые значения будут сокращены до шкалы 3.</span><span class="sxs-lookup"><span data-stu-id="5eedd-130">If this value is not specified, numeric values will be truncated to a scale of three.</span></span> <span data-ttu-id="5eedd-131">На точность не влияет, но количество цифр после десятичной точки будет укорочено до 3.</span><span class="sxs-lookup"><span data-stu-id="5eedd-131">Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span>|

## <a name="remarks"></a><span data-ttu-id="5eedd-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="5eedd-132">Remarks</span></span>

<span data-ttu-id="5eedd-133">Серверный бизнес-объект может заполнить полученный **набор записей** данными из поставщика данных, отличного от OLE DB, например из файла операционной системы, содержащего котировки акций.</span><span class="sxs-lookup"><span data-stu-id="5eedd-133">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="5eedd-134">В следующей таблице приведены значения [DataTypeEnum](datatypeenum.md) , поддерживаемые методом **CreateRecordset** .</span><span class="sxs-lookup"><span data-stu-id="5eedd-134">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method.</span></span> <span data-ttu-id="5eedd-135">В списке указан номер ссылки, используемый для определения полей.</span><span class="sxs-lookup"><span data-stu-id="5eedd-135">The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="5eedd-136">Каждый тип данных имеет фиксированную или переменную длину.</span><span class="sxs-lookup"><span data-stu-id="5eedd-136">Each of the data types is either fixed length or variable length.</span></span> <span data-ttu-id="5eedd-137">Типы фиксированной длины должны определяться размером – 1, так как размер предварительно определен, а определение размера по-прежнему требуется.</span><span class="sxs-lookup"><span data-stu-id="5eedd-137">Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required.</span></span> <span data-ttu-id="5eedd-138">Типы данных переменной длины допускают размер от 1 до 32767.</span><span class="sxs-lookup"><span data-stu-id="5eedd-138">Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="5eedd-139">Для некоторых типов данных переменных тип может быть приведен к типу, указанному в столбце подстановки.</span><span class="sxs-lookup"><span data-stu-id="5eedd-139">For some of the variable data types, the type may be coerced to the type noted in the Substitution column.</span></span> <span data-ttu-id="5eedd-140">Подстановки не отображаются до тех пор, пока не будет создан и заполнен **набор записей** .</span><span class="sxs-lookup"><span data-stu-id="5eedd-140">You won't see the substitutions until after the **Recordset** is created and filled.</span></span> <span data-ttu-id="5eedd-141">При необходимости вы можете проверить фактический тип данных.</span><span class="sxs-lookup"><span data-stu-id="5eedd-141">Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5eedd-142">Длина</span><span class="sxs-lookup"><span data-stu-id="5eedd-142">Length</span></span></p></th>
<th><p><span data-ttu-id="5eedd-143">Константа</span><span class="sxs-lookup"><span data-stu-id="5eedd-143">Constant</span></span></p></th>
<th><p><span data-ttu-id="5eedd-144">Номер</span><span class="sxs-lookup"><span data-stu-id="5eedd-144">Number</span></span></p></th>
<th><p><span data-ttu-id="5eedd-145">Подстановки</span><span class="sxs-lookup"><span data-stu-id="5eedd-145">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5eedd-146">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-147"><strong>адтининт</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-147"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-148">16 </span><span class="sxs-lookup"><span data-stu-id="5eedd-148">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5eedd-149">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-150"><strong>адсмаллинт</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-150"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-151">2</span><span class="sxs-lookup"><span data-stu-id="5eedd-151">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5eedd-152">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-153"><strong>адинтежер</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-153"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-154">4</span><span class="sxs-lookup"><span data-stu-id="5eedd-154">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5eedd-155">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-156"><strong>адбигинт</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-156"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-157">двадцать</span><span class="sxs-lookup"><span data-stu-id="5eedd-157">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5eedd-158">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-159"><strong>адунсигнедтининт</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-159"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-160">17 </span><span class="sxs-lookup"><span data-stu-id="5eedd-160">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5eedd-161">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-162"><strong>адунсигнедсмаллинт</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-162"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-163">18 </span><span class="sxs-lookup"><span data-stu-id="5eedd-163">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5eedd-164">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-165"><strong>адунсигнединт</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-165"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-166">19</span><span class="sxs-lookup"><span data-stu-id="5eedd-166">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5eedd-167">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-168"><strong>адунсигнедбигинт</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-168"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-169">21</span><span class="sxs-lookup"><span data-stu-id="5eedd-169">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5eedd-170">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-171"><strong>адсингле</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-171"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-172">4 </span><span class="sxs-lookup"><span data-stu-id="5eedd-172">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5eedd-173">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-174"><strong>аддаубле</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-174"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-175">5 </span><span class="sxs-lookup"><span data-stu-id="5eedd-175">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5eedd-176">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-177"><strong>адкурренци</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-177"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-178">6 </span><span class="sxs-lookup"><span data-stu-id="5eedd-178">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5eedd-179">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-180"><strong>аддеЦимал</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-180"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-181">14 </span><span class="sxs-lookup"><span data-stu-id="5eedd-181">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5eedd-182">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-183"><strong>аднумерик</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-183"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-184">131</span><span class="sxs-lookup"><span data-stu-id="5eedd-184">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5eedd-185">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-186"><strong>адбулеан</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-186"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-187">11 </span><span class="sxs-lookup"><span data-stu-id="5eedd-187">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5eedd-188">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-189"><strong>адеррор</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-189"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-190">10 </span><span class="sxs-lookup"><span data-stu-id="5eedd-190">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5eedd-191">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-192"><strong>адгуид</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-192"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-193">72</span><span class="sxs-lookup"><span data-stu-id="5eedd-193">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5eedd-194">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-195"><strong>аддате</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-195"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-196">7 </span><span class="sxs-lookup"><span data-stu-id="5eedd-196">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5eedd-197">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-198"><strong>аддбдате</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-198"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-199">133</span><span class="sxs-lookup"><span data-stu-id="5eedd-199">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5eedd-200">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-201"><strong>аддбтиме</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-201"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-202">134</span><span class="sxs-lookup"><span data-stu-id="5eedd-202">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5eedd-203">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="5eedd-203">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5eedd-204"><strong>аддбтиместамп</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-204"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-205">135</span><span class="sxs-lookup"><span data-stu-id="5eedd-205">135</span></span></p></td>
<td><p><span data-ttu-id="5eedd-206">7 </span><span class="sxs-lookup"><span data-stu-id="5eedd-206">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5eedd-207">Переменная</span><span class="sxs-lookup"><span data-stu-id="5eedd-207">Variable</span></span></p></td>
<td><p><span data-ttu-id="5eedd-208"><strong>адбстр</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-208"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-209">8 </span><span class="sxs-lookup"><span data-stu-id="5eedd-209">8</span></span></p></td>
<td><p><span data-ttu-id="5eedd-210">130</span><span class="sxs-lookup"><span data-stu-id="5eedd-210">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5eedd-211">Переменная</span><span class="sxs-lookup"><span data-stu-id="5eedd-211">Variable</span></span></p></td>
<td><p><span data-ttu-id="5eedd-212"><strong>адчар</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-212"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-213">129</span><span class="sxs-lookup"><span data-stu-id="5eedd-213">129</span></span></p></td>
<td><p><span data-ttu-id="5eedd-214">200</span><span class="sxs-lookup"><span data-stu-id="5eedd-214">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5eedd-215">Переменная</span><span class="sxs-lookup"><span data-stu-id="5eedd-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="5eedd-216"><strong>адварчар</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-216"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-217">200</span><span class="sxs-lookup"><span data-stu-id="5eedd-217">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5eedd-218">Переменная</span><span class="sxs-lookup"><span data-stu-id="5eedd-218">Variable</span></span></p></td>
<td><p><span data-ttu-id="5eedd-219"><strong>адлонгварчар</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-219"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-220">201</span><span class="sxs-lookup"><span data-stu-id="5eedd-220">201</span></span></p></td>
<td><p><span data-ttu-id="5eedd-221">200</span><span class="sxs-lookup"><span data-stu-id="5eedd-221">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5eedd-222">Переменная</span><span class="sxs-lookup"><span data-stu-id="5eedd-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="5eedd-223"><strong>адвчар</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-223"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-224">130</span><span class="sxs-lookup"><span data-stu-id="5eedd-224">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5eedd-225">Переменная</span><span class="sxs-lookup"><span data-stu-id="5eedd-225">Variable</span></span></p></td>
<td><p><span data-ttu-id="5eedd-226"><strong>адварвчар</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-226"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-227">202</span><span class="sxs-lookup"><span data-stu-id="5eedd-227">202</span></span></p></td>
<td><p><span data-ttu-id="5eedd-228">130</span><span class="sxs-lookup"><span data-stu-id="5eedd-228">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5eedd-229">Переменная</span><span class="sxs-lookup"><span data-stu-id="5eedd-229">Variable</span></span></p></td>
<td><p><span data-ttu-id="5eedd-230"><strong>адлонгварвчар</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-230"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-231">203</span><span class="sxs-lookup"><span data-stu-id="5eedd-231">203</span></span></p></td>
<td><p><span data-ttu-id="5eedd-232">130</span><span class="sxs-lookup"><span data-stu-id="5eedd-232">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5eedd-233">Переменная</span><span class="sxs-lookup"><span data-stu-id="5eedd-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="5eedd-234"><strong>адбинари</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-234"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-235">128</span><span class="sxs-lookup"><span data-stu-id="5eedd-235">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5eedd-236">Переменная</span><span class="sxs-lookup"><span data-stu-id="5eedd-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="5eedd-237"><strong>адварбинари</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-237"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-238">204</span><span class="sxs-lookup"><span data-stu-id="5eedd-238">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5eedd-239">Переменная</span><span class="sxs-lookup"><span data-stu-id="5eedd-239">Variable</span></span></p></td>
<td><p><span data-ttu-id="5eedd-240"><strong>адлонгварбинари</strong></span><span class="sxs-lookup"><span data-stu-id="5eedd-240"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="5eedd-241">205</span><span class="sxs-lookup"><span data-stu-id="5eedd-241">205</span></span></p></td>
<td><p><span data-ttu-id="5eedd-242">204</span><span class="sxs-lookup"><span data-stu-id="5eedd-242">204</span></span></p></td>
</tr>
</tbody>
</table>

