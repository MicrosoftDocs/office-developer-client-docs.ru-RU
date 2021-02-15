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
# <a name="createrecordset-method-rds"></a><span data-ttu-id="f4023-102">Метод CreateRecordset (RDS)</span><span class="sxs-lookup"><span data-stu-id="f4023-102">CreateRecordset method (RDS)</span></span>

<span data-ttu-id="f4023-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4023-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f4023-104">Создает пустой отключенный набор [записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="f4023-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f4023-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4023-105">Syntax</span></span>

<span data-ttu-id="f4023-106">*object .* CreateRecordset(*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="f4023-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="f4023-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4023-107">Parameters</span></span>

|<span data-ttu-id="f4023-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="f4023-108">Parameter</span></span>|<span data-ttu-id="f4023-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f4023-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f4023-110">*Object*</span><span class="sxs-lookup"><span data-stu-id="f4023-110">*Object*</span></span> |<span data-ttu-id="f4023-111">Объектная переменная, представляюная [RDSServer.DataFactory](datafactory-object-rdsserver.md) или [RDS. Объект DataControl.](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="f4023-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="f4023-112">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="f4023-112">*ColumnsInfos*</span></span> |<span data-ttu-id="f4023-113">Массив **атрибутов Variant,** который определяет каждый столбец в **созданном наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="f4023-113">A **Variant** array of attributes that defines each column in the **Recordset** created.</span></span> <span data-ttu-id="f4023-114">Каждое определение столбца содержит массив из четырех необходимых атрибутов и один необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="f4023-114">Each column definition contains an array of four required attributes and one optional attribute.</span></span> <span data-ttu-id="f4023-115">Затем набор массивов столбцов сгруппировать в массив, который определяет **набор записей.**</span><span class="sxs-lookup"><span data-stu-id="f4023-115">The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span> <span data-ttu-id="f4023-116">Список атрибутов см. в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f4023-116">For a list of attributes, see the following table.</span></span>|

### <a name="variant-array-attributes"></a><span data-ttu-id="f4023-117">Атрибуты массива variant</span><span class="sxs-lookup"><span data-stu-id="f4023-117">Variant array attributes</span></span>

|<span data-ttu-id="f4023-118">Атрибут</span><span class="sxs-lookup"><span data-stu-id="f4023-118">Attribute</span></span>|<span data-ttu-id="f4023-119">Описание</span><span class="sxs-lookup"><span data-stu-id="f4023-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f4023-120">Имя</span><span class="sxs-lookup"><span data-stu-id="f4023-120">Name</span></span> |<span data-ttu-id="f4023-121">Имя загона столбца.</span><span class="sxs-lookup"><span data-stu-id="f4023-121">Name of the column header.</span></span>|
|<span data-ttu-id="f4023-122">Type</span><span class="sxs-lookup"><span data-stu-id="f4023-122">Type</span></span> |<span data-ttu-id="f4023-123">Integer of the data type.</span><span class="sxs-lookup"><span data-stu-id="f4023-123">Integer of the data type.</span></span>|
|<span data-ttu-id="f4023-124">Size</span><span class="sxs-lookup"><span data-stu-id="f4023-124">Size</span></span> |<span data-ttu-id="f4023-125">Integer of the width in characters, regardless of data type.</span><span class="sxs-lookup"><span data-stu-id="f4023-125">Integer of the width in characters, regardless of data type.</span></span>|
|<span data-ttu-id="f4023-126">Nullability</span><span class="sxs-lookup"><span data-stu-id="f4023-126">Nullability</span></span> |<span data-ttu-id="f4023-127">Boolean value.</span><span class="sxs-lookup"><span data-stu-id="f4023-127">Boolean value.</span></span>|
|<span data-ttu-id="f4023-128">Масштаб (необязательно)</span><span class="sxs-lookup"><span data-stu-id="f4023-128">Scale (optional)</span></span> |<span data-ttu-id="f4023-129">Этот необязательный атрибут определяет масштаб для числовых полей.</span><span class="sxs-lookup"><span data-stu-id="f4023-129">This optional attribute defines the scale for numeric fields.</span></span> <span data-ttu-id="f4023-130">Если это значение не указано, числимые значения будут усечены до шкалы из трех.</span><span class="sxs-lookup"><span data-stu-id="f4023-130">If this value is not specified, numeric values will be truncated to a scale of three.</span></span> <span data-ttu-id="f4023-131">Точность не затрагивается, но число цифр после десятичной точки будет усечено до трех.</span><span class="sxs-lookup"><span data-stu-id="f4023-131">Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f4023-132">Заметки</span><span class="sxs-lookup"><span data-stu-id="f4023-132">Remarks</span></span>

<span data-ttu-id="f4023-133">Бизнес-объект на стороне сервера может заполнить полученный набор **записей** данными от поставщика данных, не относящегося к OLE DB, например файла операционной системы, содержащего котировки акций.</span><span class="sxs-lookup"><span data-stu-id="f4023-133">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="f4023-134">В следующей таблице перечислены [значения DataTypeEnum,](datatypeenum.md) поддерживаемые **методом CreateRecordset.**</span><span class="sxs-lookup"><span data-stu-id="f4023-134">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method.</span></span> <span data-ttu-id="f4023-135">Указанный номер является эталонным номером, используемым для определения полей.</span><span class="sxs-lookup"><span data-stu-id="f4023-135">The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="f4023-136">Каждый из типов данных имеет фиксированную длину или переменную длину.</span><span class="sxs-lookup"><span data-stu-id="f4023-136">Each of the data types is either fixed length or variable length.</span></span> <span data-ttu-id="f4023-137">Типы фиксированной длины должны быть определены с размером –1, так как размер предопределяется, а определение размера по-прежнему требуется.</span><span class="sxs-lookup"><span data-stu-id="f4023-137">Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required.</span></span> <span data-ttu-id="f4023-138">Типы данных переменной длины позволяют использовать от 1 до 32767.</span><span class="sxs-lookup"><span data-stu-id="f4023-138">Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="f4023-139">Для некоторых переменных типов данных тип может быть приведите к типу, определенному в столбце подстановки.</span><span class="sxs-lookup"><span data-stu-id="f4023-139">For some of the variable data types, the type may be coerced to the type noted in the Substitution column.</span></span> <span data-ttu-id="f4023-140">Подстановки будут отсещены только  после создания и заполнения наборов записей.</span><span class="sxs-lookup"><span data-stu-id="f4023-140">You won't see the substitutions until after the **Recordset** is created and filled.</span></span> <span data-ttu-id="f4023-141">Затем при необходимости можно проверить фактический тип данных.</span><span class="sxs-lookup"><span data-stu-id="f4023-141">Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4023-142">Длина</span><span class="sxs-lookup"><span data-stu-id="f4023-142">Length</span></span></p></th>
<th><p><span data-ttu-id="f4023-143">Константа</span><span class="sxs-lookup"><span data-stu-id="f4023-143">Constant</span></span></p></th>
<th><p><span data-ttu-id="f4023-144">Числовой</span><span class="sxs-lookup"><span data-stu-id="f4023-144">Number</span></span></p></th>
<th><p><span data-ttu-id="f4023-145">Подстановка</span><span class="sxs-lookup"><span data-stu-id="f4023-145">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4023-146">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-147"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-147"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-148">16 </span><span class="sxs-lookup"><span data-stu-id="f4023-148">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4023-149">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-150"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-150"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-151">2 </span><span class="sxs-lookup"><span data-stu-id="f4023-151">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4023-152">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-153"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-153"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-154">3 </span><span class="sxs-lookup"><span data-stu-id="f4023-154">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4023-155">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-156"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-156"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-157">20</span><span class="sxs-lookup"><span data-stu-id="f4023-157">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4023-158">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-159"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-159"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-160">17 </span><span class="sxs-lookup"><span data-stu-id="f4023-160">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4023-161">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-162"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-162"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-163">18 </span><span class="sxs-lookup"><span data-stu-id="f4023-163">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4023-164">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-165"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-165"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-166">19</span><span class="sxs-lookup"><span data-stu-id="f4023-166">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4023-167">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-168"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-168"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-169">21</span><span class="sxs-lookup"><span data-stu-id="f4023-169">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4023-170">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-171"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-171"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-172">4 </span><span class="sxs-lookup"><span data-stu-id="f4023-172">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4023-173">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-174"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-174"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-175">5 </span><span class="sxs-lookup"><span data-stu-id="f4023-175">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4023-176">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-177"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-177"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-178">6 </span><span class="sxs-lookup"><span data-stu-id="f4023-178">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4023-179">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-180"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-180"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-181">14 </span><span class="sxs-lookup"><span data-stu-id="f4023-181">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4023-182">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-183"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-183"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-184">131</span><span class="sxs-lookup"><span data-stu-id="f4023-184">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4023-185">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-186"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-186"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-187">11</span><span class="sxs-lookup"><span data-stu-id="f4023-187">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4023-188">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-189"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-189"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-190">10 </span><span class="sxs-lookup"><span data-stu-id="f4023-190">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4023-191">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-192"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-192"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-193">72</span><span class="sxs-lookup"><span data-stu-id="f4023-193">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4023-194">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-195"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-195"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-196">7 </span><span class="sxs-lookup"><span data-stu-id="f4023-196">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4023-197">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-198"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-198"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-199">133</span><span class="sxs-lookup"><span data-stu-id="f4023-199">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4023-200">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-201"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-201"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-202">134</span><span class="sxs-lookup"><span data-stu-id="f4023-202">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4023-203">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="f4023-203">Fixed</span></span></p></td>
<td><p><span data-ttu-id="f4023-204"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-204"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-205">135</span><span class="sxs-lookup"><span data-stu-id="f4023-205">135</span></span></p></td>
<td><p><span data-ttu-id="f4023-206">7 </span><span class="sxs-lookup"><span data-stu-id="f4023-206">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4023-207">Переменная</span><span class="sxs-lookup"><span data-stu-id="f4023-207">Variable</span></span></p></td>
<td><p><span data-ttu-id="f4023-208"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-208"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-209">8 </span><span class="sxs-lookup"><span data-stu-id="f4023-209">8</span></span></p></td>
<td><p><span data-ttu-id="f4023-210">130</span><span class="sxs-lookup"><span data-stu-id="f4023-210">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4023-211">Переменная</span><span class="sxs-lookup"><span data-stu-id="f4023-211">Variable</span></span></p></td>
<td><p><span data-ttu-id="f4023-212"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-212"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-213">129</span><span class="sxs-lookup"><span data-stu-id="f4023-213">129</span></span></p></td>
<td><p><span data-ttu-id="f4023-214">200</span><span class="sxs-lookup"><span data-stu-id="f4023-214">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4023-215">Переменная</span><span class="sxs-lookup"><span data-stu-id="f4023-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="f4023-216"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-216"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-217">200</span><span class="sxs-lookup"><span data-stu-id="f4023-217">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4023-218">Переменная</span><span class="sxs-lookup"><span data-stu-id="f4023-218">Variable</span></span></p></td>
<td><p><span data-ttu-id="f4023-219"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-219"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-220">201</span><span class="sxs-lookup"><span data-stu-id="f4023-220">201</span></span></p></td>
<td><p><span data-ttu-id="f4023-221">200</span><span class="sxs-lookup"><span data-stu-id="f4023-221">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4023-222">Переменная</span><span class="sxs-lookup"><span data-stu-id="f4023-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="f4023-223"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-223"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-224">130</span><span class="sxs-lookup"><span data-stu-id="f4023-224">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4023-225">Переменная</span><span class="sxs-lookup"><span data-stu-id="f4023-225">Variable</span></span></p></td>
<td><p><span data-ttu-id="f4023-226"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-226"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-227">202</span><span class="sxs-lookup"><span data-stu-id="f4023-227">202</span></span></p></td>
<td><p><span data-ttu-id="f4023-228">130</span><span class="sxs-lookup"><span data-stu-id="f4023-228">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4023-229">Переменная</span><span class="sxs-lookup"><span data-stu-id="f4023-229">Variable</span></span></p></td>
<td><p><span data-ttu-id="f4023-230"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-230"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-231">203</span><span class="sxs-lookup"><span data-stu-id="f4023-231">203</span></span></p></td>
<td><p><span data-ttu-id="f4023-232">130</span><span class="sxs-lookup"><span data-stu-id="f4023-232">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4023-233">Переменная</span><span class="sxs-lookup"><span data-stu-id="f4023-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="f4023-234"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-234"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-235">128</span><span class="sxs-lookup"><span data-stu-id="f4023-235">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4023-236">Переменная</span><span class="sxs-lookup"><span data-stu-id="f4023-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="f4023-237"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-237"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-238">204</span><span class="sxs-lookup"><span data-stu-id="f4023-238">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4023-239">Переменная</span><span class="sxs-lookup"><span data-stu-id="f4023-239">Variable</span></span></p></td>
<td><p><span data-ttu-id="f4023-240"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="f4023-240"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f4023-241">205</span><span class="sxs-lookup"><span data-stu-id="f4023-241">205</span></span></p></td>
<td><p><span data-ttu-id="f4023-242">204</span><span class="sxs-lookup"><span data-stu-id="f4023-242">204</span></span></p></td>
</tr>
</tbody>
</table>

