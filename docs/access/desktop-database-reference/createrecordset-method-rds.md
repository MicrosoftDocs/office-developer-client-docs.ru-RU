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
# <a name="createrecordset-method-rds"></a><span data-ttu-id="ace2f-102">Метод CreateRecordset (RDS)</span><span class="sxs-lookup"><span data-stu-id="ace2f-102">CreateRecordset method (RDS)</span></span>

<span data-ttu-id="ace2f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ace2f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ace2f-104">Создает пустой, отключенный [набор записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="ace2f-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ace2f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ace2f-105">Syntax</span></span>

<span data-ttu-id="ace2f-106">*объект*. CreateRecordset *(ColumnInfos)*</span><span class="sxs-lookup"><span data-stu-id="ace2f-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="ace2f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ace2f-107">Parameters</span></span>

|<span data-ttu-id="ace2f-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="ace2f-108">Parameter</span></span>|<span data-ttu-id="ace2f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ace2f-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ace2f-110">*Object*</span><span class="sxs-lookup"><span data-stu-id="ace2f-110">*Object*</span></span> |<span data-ttu-id="ace2f-111">Переменная объекта, представляюая [RDSServer.DataFactory](datafactory-object-rdsserver.md) или [RDS. Объект DataControl.](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="ace2f-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="ace2f-112">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="ace2f-112">*ColumnsInfos*</span></span> |<span data-ttu-id="ace2f-113">Набор **атрибутов Variant,** определяя каждый столбец **созданного Набор записей.**</span><span class="sxs-lookup"><span data-stu-id="ace2f-113">A **Variant** array of attributes that defines each column in the **Recordset** created.</span></span> <span data-ttu-id="ace2f-114">Каждое определение столбца содержит массив из четырех необходимых атрибутов и одного необязательного атрибута.</span><span class="sxs-lookup"><span data-stu-id="ace2f-114">Each column definition contains an array of four required attributes and one optional attribute.</span></span> <span data-ttu-id="ace2f-115">Затем набор массивов столбцов сгруппироваться в массив, который определяет **Набор записей.**</span><span class="sxs-lookup"><span data-stu-id="ace2f-115">The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span> <span data-ttu-id="ace2f-116">Список атрибутов см. в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ace2f-116">For a list of attributes, see the following table.</span></span>|

### <a name="variant-array-attributes"></a><span data-ttu-id="ace2f-117">Атрибуты массива variant</span><span class="sxs-lookup"><span data-stu-id="ace2f-117">Variant array attributes</span></span>

|<span data-ttu-id="ace2f-118">Атрибут</span><span class="sxs-lookup"><span data-stu-id="ace2f-118">Attribute</span></span>|<span data-ttu-id="ace2f-119">Описание</span><span class="sxs-lookup"><span data-stu-id="ace2f-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ace2f-120">Имя</span><span class="sxs-lookup"><span data-stu-id="ace2f-120">Name</span></span> |<span data-ttu-id="ace2f-121">Имя загона столбца.</span><span class="sxs-lookup"><span data-stu-id="ace2f-121">Name of the column header.</span></span>|
|<span data-ttu-id="ace2f-122">Тип</span><span class="sxs-lookup"><span data-stu-id="ace2f-122">Type</span></span> |<span data-ttu-id="ace2f-123">Integer типа данных.</span><span class="sxs-lookup"><span data-stu-id="ace2f-123">Integer of the data type.</span></span>|
|<span data-ttu-id="ace2f-124">Size</span><span class="sxs-lookup"><span data-stu-id="ace2f-124">Size</span></span> |<span data-ttu-id="ace2f-125">Набор ширины символов независимо от типа данных.</span><span class="sxs-lookup"><span data-stu-id="ace2f-125">Integer of the width in characters, regardless of data type.</span></span>|
|<span data-ttu-id="ace2f-126">Недействительность</span><span class="sxs-lookup"><span data-stu-id="ace2f-126">Nullability</span></span> |<span data-ttu-id="ace2f-127">Значение Boolean.</span><span class="sxs-lookup"><span data-stu-id="ace2f-127">Boolean value.</span></span>|
|<span data-ttu-id="ace2f-128">Масштаб (необязательный)</span><span class="sxs-lookup"><span data-stu-id="ace2f-128">Scale (optional)</span></span> |<span data-ttu-id="ace2f-129">Этот необязательный атрибут определяет масштаб для числовых полей.</span><span class="sxs-lookup"><span data-stu-id="ace2f-129">This optional attribute defines the scale for numeric fields.</span></span> <span data-ttu-id="ace2f-130">Если это значение не указано, численные значения будут усечены до трех.</span><span class="sxs-lookup"><span data-stu-id="ace2f-130">If this value is not specified, numeric values will be truncated to a scale of three.</span></span> <span data-ttu-id="ace2f-131">Точность не влияет, но число цифр, следующих за десятичной точкой, будет усечено до трех.</span><span class="sxs-lookup"><span data-stu-id="ace2f-131">Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ace2f-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="ace2f-132">Remarks</span></span>

<span data-ttu-id="ace2f-133">Бизнес-объект на стороне сервера может  заполнять полученный набор записей данными от поставщика данных, не относящегося к OLE DB, например файла операционной системы, содержащего котировки акций.</span><span class="sxs-lookup"><span data-stu-id="ace2f-133">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="ace2f-134">В следующей таблице перечислены значения [DataTypeEnum,](datatypeenum.md) поддерживаемые **методом CreateRecordset.**</span><span class="sxs-lookup"><span data-stu-id="ace2f-134">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method.</span></span> <span data-ttu-id="ace2f-135">Указанный номер — это справочный номер, используемый для определения полей.</span><span class="sxs-lookup"><span data-stu-id="ace2f-135">The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="ace2f-136">Каждый из типов данных имеет фиксированную длину или переменную длину.</span><span class="sxs-lookup"><span data-stu-id="ace2f-136">Each of the data types is either fixed length or variable length.</span></span> <span data-ttu-id="ace2f-137">Типы фиксированной длины должны быть определены с размером -1, так как размер заранее определен и определение размера по-прежнему требуется.</span><span class="sxs-lookup"><span data-stu-id="ace2f-137">Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required.</span></span> <span data-ttu-id="ace2f-138">Типы данных переменной длины позволяют размер от 1 до 32767.</span><span class="sxs-lookup"><span data-stu-id="ace2f-138">Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="ace2f-139">Для некоторых типов переменных данных тип может быть принужден к типу, отмеченным в столбце Подмена.</span><span class="sxs-lookup"><span data-stu-id="ace2f-139">For some of the variable data types, the type may be coerced to the type noted in the Substitution column.</span></span> <span data-ttu-id="ace2f-140">Замены будут созданы и заполнены только после создания и заполнения **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="ace2f-140">You won't see the substitutions until after the **Recordset** is created and filled.</span></span> <span data-ttu-id="ace2f-141">Затем вы можете проверить фактический тип данных, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="ace2f-141">Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ace2f-142">Длина</span><span class="sxs-lookup"><span data-stu-id="ace2f-142">Length</span></span></p></th>
<th><p><span data-ttu-id="ace2f-143">Константа</span><span class="sxs-lookup"><span data-stu-id="ace2f-143">Constant</span></span></p></th>
<th><p><span data-ttu-id="ace2f-144">Номер</span><span class="sxs-lookup"><span data-stu-id="ace2f-144">Number</span></span></p></th>
<th><p><span data-ttu-id="ace2f-145">Замена</span><span class="sxs-lookup"><span data-stu-id="ace2f-145">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ace2f-146">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-147"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-147"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-148">16 </span><span class="sxs-lookup"><span data-stu-id="ace2f-148">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace2f-149">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-150"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-150"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-151">2</span><span class="sxs-lookup"><span data-stu-id="ace2f-151">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace2f-152">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-153"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-153"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-154">3</span><span class="sxs-lookup"><span data-stu-id="ace2f-154">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace2f-155">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-156"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-156"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-157">20</span><span class="sxs-lookup"><span data-stu-id="ace2f-157">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace2f-158">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-159"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-159"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-160">17 </span><span class="sxs-lookup"><span data-stu-id="ace2f-160">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace2f-161">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-162"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-162"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-163">18 </span><span class="sxs-lookup"><span data-stu-id="ace2f-163">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace2f-164">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-165"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-165"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-166">19</span><span class="sxs-lookup"><span data-stu-id="ace2f-166">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace2f-167">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-168"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-168"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-169">21</span><span class="sxs-lookup"><span data-stu-id="ace2f-169">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace2f-170">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-171"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-171"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-172">4 </span><span class="sxs-lookup"><span data-stu-id="ace2f-172">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace2f-173">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-174"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-174"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-175">5 </span><span class="sxs-lookup"><span data-stu-id="ace2f-175">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace2f-176">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-177"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-177"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-178">6 </span><span class="sxs-lookup"><span data-stu-id="ace2f-178">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace2f-179">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-180"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-180"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-181">14 </span><span class="sxs-lookup"><span data-stu-id="ace2f-181">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace2f-182">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-183"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-183"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-184">131</span><span class="sxs-lookup"><span data-stu-id="ace2f-184">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace2f-185">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-186"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-186"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-187">11</span><span class="sxs-lookup"><span data-stu-id="ace2f-187">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace2f-188">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-189"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-189"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-190">10 </span><span class="sxs-lookup"><span data-stu-id="ace2f-190">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace2f-191">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-192"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-192"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-193">72</span><span class="sxs-lookup"><span data-stu-id="ace2f-193">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace2f-194">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-195"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-195"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-196">7 </span><span class="sxs-lookup"><span data-stu-id="ace2f-196">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace2f-197">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-198"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-198"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-199">133</span><span class="sxs-lookup"><span data-stu-id="ace2f-199">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace2f-200">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-201"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-201"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-202">134</span><span class="sxs-lookup"><span data-stu-id="ace2f-202">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace2f-203">ИСПРАВЛЕНО</span><span class="sxs-lookup"><span data-stu-id="ace2f-203">Fixed</span></span></p></td>
<td><p><span data-ttu-id="ace2f-204"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-204"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-205">135</span><span class="sxs-lookup"><span data-stu-id="ace2f-205">135</span></span></p></td>
<td><p><span data-ttu-id="ace2f-206">7 </span><span class="sxs-lookup"><span data-stu-id="ace2f-206">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace2f-207">Переменная</span><span class="sxs-lookup"><span data-stu-id="ace2f-207">Variable</span></span></p></td>
<td><p><span data-ttu-id="ace2f-208"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-208"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-209">8 </span><span class="sxs-lookup"><span data-stu-id="ace2f-209">8</span></span></p></td>
<td><p><span data-ttu-id="ace2f-210">130</span><span class="sxs-lookup"><span data-stu-id="ace2f-210">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace2f-211">Переменная</span><span class="sxs-lookup"><span data-stu-id="ace2f-211">Variable</span></span></p></td>
<td><p><span data-ttu-id="ace2f-212"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-212"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-213">129</span><span class="sxs-lookup"><span data-stu-id="ace2f-213">129</span></span></p></td>
<td><p><span data-ttu-id="ace2f-214">200</span><span class="sxs-lookup"><span data-stu-id="ace2f-214">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace2f-215">Переменная</span><span class="sxs-lookup"><span data-stu-id="ace2f-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="ace2f-216"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-216"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-217">200</span><span class="sxs-lookup"><span data-stu-id="ace2f-217">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace2f-218">Переменная</span><span class="sxs-lookup"><span data-stu-id="ace2f-218">Variable</span></span></p></td>
<td><p><span data-ttu-id="ace2f-219"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-219"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-220">201</span><span class="sxs-lookup"><span data-stu-id="ace2f-220">201</span></span></p></td>
<td><p><span data-ttu-id="ace2f-221">200</span><span class="sxs-lookup"><span data-stu-id="ace2f-221">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace2f-222">Переменная</span><span class="sxs-lookup"><span data-stu-id="ace2f-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="ace2f-223"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-223"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-224">130</span><span class="sxs-lookup"><span data-stu-id="ace2f-224">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace2f-225">Переменная</span><span class="sxs-lookup"><span data-stu-id="ace2f-225">Variable</span></span></p></td>
<td><p><span data-ttu-id="ace2f-226"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-226"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-227">202</span><span class="sxs-lookup"><span data-stu-id="ace2f-227">202</span></span></p></td>
<td><p><span data-ttu-id="ace2f-228">130</span><span class="sxs-lookup"><span data-stu-id="ace2f-228">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace2f-229">Переменная</span><span class="sxs-lookup"><span data-stu-id="ace2f-229">Variable</span></span></p></td>
<td><p><span data-ttu-id="ace2f-230"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-230"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-231">203</span><span class="sxs-lookup"><span data-stu-id="ace2f-231">203</span></span></p></td>
<td><p><span data-ttu-id="ace2f-232">130</span><span class="sxs-lookup"><span data-stu-id="ace2f-232">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace2f-233">Переменная</span><span class="sxs-lookup"><span data-stu-id="ace2f-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="ace2f-234"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-234"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-235">128</span><span class="sxs-lookup"><span data-stu-id="ace2f-235">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace2f-236">Переменная</span><span class="sxs-lookup"><span data-stu-id="ace2f-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="ace2f-237"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-237"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-238">204</span><span class="sxs-lookup"><span data-stu-id="ace2f-238">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace2f-239">Переменная</span><span class="sxs-lookup"><span data-stu-id="ace2f-239">Variable</span></span></p></td>
<td><p><span data-ttu-id="ace2f-240"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="ace2f-240"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="ace2f-241">205</span><span class="sxs-lookup"><span data-stu-id="ace2f-241">205</span></span></p></td>
<td><p><span data-ttu-id="ace2f-242">204</span><span class="sxs-lookup"><span data-stu-id="ace2f-242">204</span></span></p></td>
</tr>
</tbody>
</table>

