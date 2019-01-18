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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703022"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="eed42-102">Метод CreateRecordset (RDS)</span><span class="sxs-lookup"><span data-stu-id="eed42-102">CreateRecordset method (RDS)</span></span>

<span data-ttu-id="eed42-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eed42-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eed42-104">Создает пустой, отключенные [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="eed42-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eed42-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eed42-105">Syntax</span></span>

<span data-ttu-id="eed42-106">*объект*. CreateRecordset (*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="eed42-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="eed42-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="eed42-107">Parameters</span></span>

|<span data-ttu-id="eed42-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="eed42-108">Parameter</span></span>|<span data-ttu-id="eed42-109">Описание</span><span class="sxs-lookup"><span data-stu-id="eed42-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="eed42-110">*Object*</span><span class="sxs-lookup"><span data-stu-id="eed42-110">*Object*</span></span> |<span data-ttu-id="eed42-111">Объектную переменную, которая представляет [RDSServer.DataFactory](datafactory-object-rdsserver.md) или [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="eed42-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="eed42-112">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="eed42-112">*ColumnsInfos*</span></span> |<span data-ttu-id="eed42-113">Создать **Variant** массив атрибутов, определяющий столбцы в **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="eed42-113">A **Variant** array of attributes that defines each column in the **Recordset** created.</span></span> <span data-ttu-id="eed42-114">Определение каждого столбца содержит массив четыре обязательные атрибуты и один необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="eed42-114">Each column definition contains an array of four required attributes and one optional attribute.</span></span> <span data-ttu-id="eed42-115">Набор столбцов массивов нажмите сгруппированы в массив, который определяет **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="eed42-115">The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span> <span data-ttu-id="eed42-116">Список атрибутов обратитесь к таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="eed42-116">For a list of attributes, see the following table.</span></span>|

### <a name="variant-array-attributes"></a><span data-ttu-id="eed42-117">Атрибуты массив вариантов</span><span class="sxs-lookup"><span data-stu-id="eed42-117">Variant array attributes</span></span>

|<span data-ttu-id="eed42-118">Атрибут</span><span class="sxs-lookup"><span data-stu-id="eed42-118">Attribute</span></span>|<span data-ttu-id="eed42-119">Описание</span><span class="sxs-lookup"><span data-stu-id="eed42-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="eed42-120">Имя</span><span class="sxs-lookup"><span data-stu-id="eed42-120">Name</span></span> |<span data-ttu-id="eed42-121">Имя заголовка столбца.</span><span class="sxs-lookup"><span data-stu-id="eed42-121">Name of the column header.</span></span>|
|<span data-ttu-id="eed42-122">Тип</span><span class="sxs-lookup"><span data-stu-id="eed42-122">Type</span></span> |<span data-ttu-id="eed42-123">Целое число типа данных.</span><span class="sxs-lookup"><span data-stu-id="eed42-123">Integer of the data type.</span></span>|
|<span data-ttu-id="eed42-124">Размер</span><span class="sxs-lookup"><span data-stu-id="eed42-124">Size</span></span> |<span data-ttu-id="eed42-125">Целое число от ширины знаков, независимо от типа данных.</span><span class="sxs-lookup"><span data-stu-id="eed42-125">Integer of the width in characters, regardless of data type.</span></span>|
|<span data-ttu-id="eed42-126">Возможность принимать значение NULL</span><span class="sxs-lookup"><span data-stu-id="eed42-126">Nullability</span></span> |<span data-ttu-id="eed42-127">Логическое значение.</span><span class="sxs-lookup"><span data-stu-id="eed42-127">Boolean value.</span></span>|
|<span data-ttu-id="eed42-128">Масштаб (необязательно)</span><span class="sxs-lookup"><span data-stu-id="eed42-128">Scale (optional)</span></span> |<span data-ttu-id="eed42-129">Этот дополнительный атрибут задает масштаб для числовых полей.</span><span class="sxs-lookup"><span data-stu-id="eed42-129">This optional attribute defines the scale for numeric fields.</span></span> <span data-ttu-id="eed42-130">Если это значение не указано, с горизонтальным трех усекаются числовых значений.</span><span class="sxs-lookup"><span data-stu-id="eed42-130">If this value is not specified, numeric values will be truncated to a scale of three.</span></span> <span data-ttu-id="eed42-131">Количество разрядов после запятой будет усечено до трех, но не повлияет точности.</span><span class="sxs-lookup"><span data-stu-id="eed42-131">Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span>|

## <a name="remarks"></a><span data-ttu-id="eed42-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="eed42-132">Remarks</span></span>

<span data-ttu-id="eed42-133">На сервере бизнес-объекта можно заполнить результирующего **набора записей** с данными из не - поставщиков данных OLE DB, такие как файл операционной системы, содержащий акций.</span><span class="sxs-lookup"><span data-stu-id="eed42-133">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="eed42-134">В следующей таблице перечислены значения [DataTypeEnum](datatypeenum.md) , поддерживаемый метод **CreateRecordset** .</span><span class="sxs-lookup"><span data-stu-id="eed42-134">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method.</span></span> <span data-ttu-id="eed42-135">Номер, указанный является номер ссылки, используемые для определения полей.</span><span class="sxs-lookup"><span data-stu-id="eed42-135">The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="eed42-136">Каждый из типов данных является фиксированной длины или переменной длины.</span><span class="sxs-lookup"><span data-stu-id="eed42-136">Each of the data types is either fixed length or variable length.</span></span> <span data-ttu-id="eed42-137">Типы фиксированной длины должны быть определены с размером – 1, так как предварительно определенный размер и определение размера по-прежнему требуется.</span><span class="sxs-lookup"><span data-stu-id="eed42-137">Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required.</span></span> <span data-ttu-id="eed42-138">Типы данных переменной длины разрешить размер от 1 до 32767.</span><span class="sxs-lookup"><span data-stu-id="eed42-138">Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="eed42-139">Для некоторых типов данных переменной тип может привести к типу, указаны в столбце подстановки.</span><span class="sxs-lookup"><span data-stu-id="eed42-139">For some of the variable data types, the type may be coerced to the type noted in the Substitution column.</span></span> <span data-ttu-id="eed42-140">Вы не увидите замены до того времени, после создания и заполнения **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="eed42-140">You won't see the substitutions until after the **Recordset** is created and filled.</span></span> <span data-ttu-id="eed42-141">Затем следует проверить, тип фактических данных, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="eed42-141">Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eed42-142">Length</span><span class="sxs-lookup"><span data-stu-id="eed42-142">Length</span></span></p></th>
<th><p><span data-ttu-id="eed42-143">Константа</span><span class="sxs-lookup"><span data-stu-id="eed42-143">Constant</span></span></p></th>
<th><p><span data-ttu-id="eed42-144">Число</span><span class="sxs-lookup"><span data-stu-id="eed42-144">Number</span></span></p></th>
<th><p><span data-ttu-id="eed42-145">Замена </span><span class="sxs-lookup"><span data-stu-id="eed42-145">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eed42-146">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-147"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-147"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-148">16</span><span class="sxs-lookup"><span data-stu-id="eed42-148">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed42-149">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-150"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-150"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-151">2</span><span class="sxs-lookup"><span data-stu-id="eed42-151">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed42-152">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-153"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-153"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-154">3</span><span class="sxs-lookup"><span data-stu-id="eed42-154">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed42-155">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-156"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-156"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-157">20</span><span class="sxs-lookup"><span data-stu-id="eed42-157">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed42-158">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-159"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-159"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-160">17</span><span class="sxs-lookup"><span data-stu-id="eed42-160">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed42-161">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-162"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-162"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-163">18</span><span class="sxs-lookup"><span data-stu-id="eed42-163">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed42-164">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-165"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-165"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-166">19</span><span class="sxs-lookup"><span data-stu-id="eed42-166">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed42-167">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-168"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-168"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-169">21</span><span class="sxs-lookup"><span data-stu-id="eed42-169">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed42-170">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-171"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-171"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-172">4</span><span class="sxs-lookup"><span data-stu-id="eed42-172">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed42-173">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-174"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-174"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-175">5</span><span class="sxs-lookup"><span data-stu-id="eed42-175">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed42-176">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-177"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-177"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-178">6</span><span class="sxs-lookup"><span data-stu-id="eed42-178">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed42-179">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-180"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-180"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-181">14</span><span class="sxs-lookup"><span data-stu-id="eed42-181">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed42-182">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-183"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-183"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-184">131</span><span class="sxs-lookup"><span data-stu-id="eed42-184">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed42-185">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-186"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-186"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-187">11</span><span class="sxs-lookup"><span data-stu-id="eed42-187">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed42-188">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-189"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-189"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-190">10</span><span class="sxs-lookup"><span data-stu-id="eed42-190">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed42-191">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-192"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-192"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-193">72</span><span class="sxs-lookup"><span data-stu-id="eed42-193">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed42-194">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-195"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-195"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-196">7</span><span class="sxs-lookup"><span data-stu-id="eed42-196">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed42-197">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-198"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-198"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-199">133</span><span class="sxs-lookup"><span data-stu-id="eed42-199">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed42-200">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-201"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-201"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-202">134</span><span class="sxs-lookup"><span data-stu-id="eed42-202">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed42-203">Фиксация</span><span class="sxs-lookup"><span data-stu-id="eed42-203">Fixed</span></span></p></td>
<td><p><span data-ttu-id="eed42-204"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-204"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-205">135</span><span class="sxs-lookup"><span data-stu-id="eed42-205">135</span></span></p></td>
<td><p><span data-ttu-id="eed42-206">7</span><span class="sxs-lookup"><span data-stu-id="eed42-206">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed42-207">Переменная</span><span class="sxs-lookup"><span data-stu-id="eed42-207">Variable</span></span></p></td>
<td><p><span data-ttu-id="eed42-208"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-208"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-209">8</span><span class="sxs-lookup"><span data-stu-id="eed42-209">8</span></span></p></td>
<td><p><span data-ttu-id="eed42-210">130</span><span class="sxs-lookup"><span data-stu-id="eed42-210">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed42-211">Переменная</span><span class="sxs-lookup"><span data-stu-id="eed42-211">Variable</span></span></p></td>
<td><p><span data-ttu-id="eed42-212"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-212"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-213">129</span><span class="sxs-lookup"><span data-stu-id="eed42-213">129</span></span></p></td>
<td><p><span data-ttu-id="eed42-214">200</span><span class="sxs-lookup"><span data-stu-id="eed42-214">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed42-215">Переменная</span><span class="sxs-lookup"><span data-stu-id="eed42-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="eed42-216"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-216"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-217">200</span><span class="sxs-lookup"><span data-stu-id="eed42-217">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed42-218">Переменная</span><span class="sxs-lookup"><span data-stu-id="eed42-218">Variable</span></span></p></td>
<td><p><span data-ttu-id="eed42-219"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-219"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-220">201</span><span class="sxs-lookup"><span data-stu-id="eed42-220">201</span></span></p></td>
<td><p><span data-ttu-id="eed42-221">200</span><span class="sxs-lookup"><span data-stu-id="eed42-221">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed42-222">Переменная</span><span class="sxs-lookup"><span data-stu-id="eed42-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="eed42-223"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-223"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-224">130</span><span class="sxs-lookup"><span data-stu-id="eed42-224">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed42-225">Переменная</span><span class="sxs-lookup"><span data-stu-id="eed42-225">Variable</span></span></p></td>
<td><p><span data-ttu-id="eed42-226"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-226"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-227">202</span><span class="sxs-lookup"><span data-stu-id="eed42-227">202</span></span></p></td>
<td><p><span data-ttu-id="eed42-228">130</span><span class="sxs-lookup"><span data-stu-id="eed42-228">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed42-229">Переменная</span><span class="sxs-lookup"><span data-stu-id="eed42-229">Variable</span></span></p></td>
<td><p><span data-ttu-id="eed42-230"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-230"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-231">203</span><span class="sxs-lookup"><span data-stu-id="eed42-231">203</span></span></p></td>
<td><p><span data-ttu-id="eed42-232">130</span><span class="sxs-lookup"><span data-stu-id="eed42-232">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed42-233">Переменная</span><span class="sxs-lookup"><span data-stu-id="eed42-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="eed42-234"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-234"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-235">128</span><span class="sxs-lookup"><span data-stu-id="eed42-235">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eed42-236">Переменная</span><span class="sxs-lookup"><span data-stu-id="eed42-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="eed42-237"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-237"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-238">204</span><span class="sxs-lookup"><span data-stu-id="eed42-238">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eed42-239">Переменная</span><span class="sxs-lookup"><span data-stu-id="eed42-239">Variable</span></span></p></td>
<td><p><span data-ttu-id="eed42-240"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="eed42-240"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="eed42-241">205</span><span class="sxs-lookup"><span data-stu-id="eed42-241">205</span></span></p></td>
<td><p><span data-ttu-id="eed42-242">204</span><span class="sxs-lookup"><span data-stu-id="eed42-242">204</span></span></p></td>
</tr>
</tbody>
</table>

