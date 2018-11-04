---
title: Метод CreateRecordset (RDS)
TOCTitle: CreateRecordset method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0b4d68ac2dfca344cb98885846f2cd09fafd0ea0
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950239"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="84824-102">Метод CreateRecordset (RDS)</span><span class="sxs-lookup"><span data-stu-id="84824-102">CreateRecordset method (RDS)</span></span>

<span data-ttu-id="84824-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="84824-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="84824-104">Создает пустой, отключенные [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="84824-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="84824-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84824-105">Syntax</span></span>

<span data-ttu-id="84824-106">*объект*. CreateRecordset (*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="84824-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="84824-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="84824-107">Parameters</span></span>

|<span data-ttu-id="84824-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="84824-108">Parameter</span></span>|<span data-ttu-id="84824-109">Описание</span><span class="sxs-lookup"><span data-stu-id="84824-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="84824-110">*Объект*</span><span class="sxs-lookup"><span data-stu-id="84824-110">*Object*</span></span> |<span data-ttu-id="84824-111">Объектную переменную, которая представляет [RDSServer.DataFactory](datafactory-object-rdsserver.md) или [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="84824-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="84824-112">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="84824-112">*ColumnsInfos*</span></span> |<span data-ttu-id="84824-113">Создать **Variant** массив атрибутов, определяющий столбцы в **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="84824-113">A **Variant** array of attributes that defines each column in the **Recordset** created.</span></span> <span data-ttu-id="84824-114">Определение каждого столбца содержит массив четыре обязательные атрибуты и один необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="84824-114">Each column definition contains an array of four required attributes and one optional attribute.</span></span> <span data-ttu-id="84824-115">Набор столбцов массивов нажмите сгруппированы в массив, который определяет **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="84824-115">The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span> <span data-ttu-id="84824-116">Список атрибутов обратитесь к таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="84824-116">For a list of attributes, see the following table.</span></span>|

### <a name="variant-array-attributes"></a><span data-ttu-id="84824-117">Атрибуты массив вариантов</span><span class="sxs-lookup"><span data-stu-id="84824-117">Variant array attributes</span></span>

|<span data-ttu-id="84824-118">Атрибут</span><span class="sxs-lookup"><span data-stu-id="84824-118">Attribute</span></span>|<span data-ttu-id="84824-119">Описание</span><span class="sxs-lookup"><span data-stu-id="84824-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="84824-120">Имя</span><span class="sxs-lookup"><span data-stu-id="84824-120">Name</span></span> |<span data-ttu-id="84824-121">Имя заголовка столбца.</span><span class="sxs-lookup"><span data-stu-id="84824-121">Name of the column header.</span></span>|
|<span data-ttu-id="84824-122">Тип</span><span class="sxs-lookup"><span data-stu-id="84824-122">Type</span></span> |<span data-ttu-id="84824-123">Целое число типа данных.</span><span class="sxs-lookup"><span data-stu-id="84824-123">Integer of the data type.</span></span>|
|<span data-ttu-id="84824-124">Size</span><span class="sxs-lookup"><span data-stu-id="84824-124">Size</span></span> |<span data-ttu-id="84824-125">Целое число от ширины знаков, независимо от типа данных.</span><span class="sxs-lookup"><span data-stu-id="84824-125">Integer of the width in characters, regardless of data type.</span></span>|
|<span data-ttu-id="84824-126">Возможность принимать значение NULL</span><span class="sxs-lookup"><span data-stu-id="84824-126">Nullability</span></span> |<span data-ttu-id="84824-127">Логическое значение.</span><span class="sxs-lookup"><span data-stu-id="84824-127">Boolean value.</span></span>|
|<span data-ttu-id="84824-128">Масштаб (необязательно)</span><span class="sxs-lookup"><span data-stu-id="84824-128">Scale (optional)</span></span> |<span data-ttu-id="84824-129">Этот дополнительный атрибут задает масштаб для числовых полей.</span><span class="sxs-lookup"><span data-stu-id="84824-129">This optional attribute defines the scale for numeric fields.</span></span> <span data-ttu-id="84824-130">Если это значение не указано, с горизонтальным трех усекаются числовых значений.</span><span class="sxs-lookup"><span data-stu-id="84824-130">If this value is not specified, numeric values will be truncated to a scale of three.</span></span> <span data-ttu-id="84824-131">Количество разрядов после запятой будет усечено до трех, но не повлияет точности.</span><span class="sxs-lookup"><span data-stu-id="84824-131">Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span>|

## <a name="remarks"></a><span data-ttu-id="84824-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="84824-132">Remarks</span></span>

<span data-ttu-id="84824-133">На сервере бизнес-объекта можно заполнить результирующего **набора записей** с данными из не - поставщиков данных OLE DB, такие как файл операционной системы, содержащий акций.</span><span class="sxs-lookup"><span data-stu-id="84824-133">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="84824-134">В следующей таблице перечислены значения [DataTypeEnum](datatypeenum.md) , поддерживаемый метод **CreateRecordset** .</span><span class="sxs-lookup"><span data-stu-id="84824-134">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method.</span></span> <span data-ttu-id="84824-135">Номер, указанный является номер ссылки, используемые для определения полей.</span><span class="sxs-lookup"><span data-stu-id="84824-135">The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="84824-136">Каждый из типов данных является фиксированной длины или переменной длины.</span><span class="sxs-lookup"><span data-stu-id="84824-136">Each of the data types is either fixed length or variable length.</span></span> <span data-ttu-id="84824-137">Типы фиксированной длины должны быть определены с размером – 1, так как предварительно определенный размер и определение размера по-прежнему требуется.</span><span class="sxs-lookup"><span data-stu-id="84824-137">Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required.</span></span> <span data-ttu-id="84824-138">Типы данных переменной длины разрешить размер от 1 до 32767.</span><span class="sxs-lookup"><span data-stu-id="84824-138">Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="84824-139">Для некоторых типов данных переменной тип может привести к типу, указаны в столбце подстановки.</span><span class="sxs-lookup"><span data-stu-id="84824-139">For some of the variable data types, the type may be coerced to the type noted in the Substitution column.</span></span> <span data-ttu-id="84824-140">Вы не увидите замены до того времени, после создания и заполнения **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="84824-140">You won't see the substitutions until after the **Recordset** is created and filled.</span></span> <span data-ttu-id="84824-141">Затем следует проверить, тип фактических данных, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="84824-141">Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="84824-142">Length</span><span class="sxs-lookup"><span data-stu-id="84824-142">Length</span></span></p></th>
<th><p><span data-ttu-id="84824-143">Constant</span><span class="sxs-lookup"><span data-stu-id="84824-143">Constant</span></span></p></th>
<th><p><span data-ttu-id="84824-144">Number</span><span class="sxs-lookup"><span data-stu-id="84824-144">Number</span></span></p></th>
<th><p><span data-ttu-id="84824-145">Замена </span><span class="sxs-lookup"><span data-stu-id="84824-145">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84824-146">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-147"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="84824-147"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-148">16</span><span class="sxs-lookup"><span data-stu-id="84824-148">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84824-149">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-150"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="84824-150"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-151">2</span><span class="sxs-lookup"><span data-stu-id="84824-151">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84824-152">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-153"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="84824-153"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-154">3</span><span class="sxs-lookup"><span data-stu-id="84824-154">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84824-155">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-156"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="84824-156"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-157">20</span><span class="sxs-lookup"><span data-stu-id="84824-157">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84824-158">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-159"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="84824-159"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-160">17</span><span class="sxs-lookup"><span data-stu-id="84824-160">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84824-161">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-162"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="84824-162"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-163">18</span><span class="sxs-lookup"><span data-stu-id="84824-163">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84824-164">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-165"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="84824-165"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-166">19</span><span class="sxs-lookup"><span data-stu-id="84824-166">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84824-167">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-168"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="84824-168"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-169">21</span><span class="sxs-lookup"><span data-stu-id="84824-169">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84824-170">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-171"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="84824-171"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-172">4</span><span class="sxs-lookup"><span data-stu-id="84824-172">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84824-173">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-174"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="84824-174"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-175">5</span><span class="sxs-lookup"><span data-stu-id="84824-175">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84824-176">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-177"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="84824-177"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-178">6</span><span class="sxs-lookup"><span data-stu-id="84824-178">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84824-179">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-180"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="84824-180"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-181">14</span><span class="sxs-lookup"><span data-stu-id="84824-181">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84824-182">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-183"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="84824-183"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-184">131</span><span class="sxs-lookup"><span data-stu-id="84824-184">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84824-185">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-186"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="84824-186"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-187">11</span><span class="sxs-lookup"><span data-stu-id="84824-187">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84824-188">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-189"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="84824-189"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-190">10</span><span class="sxs-lookup"><span data-stu-id="84824-190">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84824-191">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-192"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="84824-192"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-193">72</span><span class="sxs-lookup"><span data-stu-id="84824-193">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84824-194">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-195"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="84824-195"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-196">7</span><span class="sxs-lookup"><span data-stu-id="84824-196">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84824-197">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-198"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="84824-198"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-199">133</span><span class="sxs-lookup"><span data-stu-id="84824-199">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84824-200">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-201"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="84824-201"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-202">134</span><span class="sxs-lookup"><span data-stu-id="84824-202">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84824-203">Фиксация</span><span class="sxs-lookup"><span data-stu-id="84824-203">Fixed</span></span></p></td>
<td><p><span data-ttu-id="84824-204"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="84824-204"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-205">135</span><span class="sxs-lookup"><span data-stu-id="84824-205">135</span></span></p></td>
<td><p><span data-ttu-id="84824-206">7</span><span class="sxs-lookup"><span data-stu-id="84824-206">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84824-207">Переменная</span><span class="sxs-lookup"><span data-stu-id="84824-207">Variable</span></span></p></td>
<td><p><span data-ttu-id="84824-208"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="84824-208"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-209">8</span><span class="sxs-lookup"><span data-stu-id="84824-209">8</span></span></p></td>
<td><p><span data-ttu-id="84824-210">130</span><span class="sxs-lookup"><span data-stu-id="84824-210">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84824-211">Переменная</span><span class="sxs-lookup"><span data-stu-id="84824-211">Variable</span></span></p></td>
<td><p><span data-ttu-id="84824-212"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="84824-212"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-213">129</span><span class="sxs-lookup"><span data-stu-id="84824-213">129</span></span></p></td>
<td><p><span data-ttu-id="84824-214">200</span><span class="sxs-lookup"><span data-stu-id="84824-214">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84824-215">Переменная</span><span class="sxs-lookup"><span data-stu-id="84824-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="84824-216"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="84824-216"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-217">200</span><span class="sxs-lookup"><span data-stu-id="84824-217">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84824-218">Переменная</span><span class="sxs-lookup"><span data-stu-id="84824-218">Variable</span></span></p></td>
<td><p><span data-ttu-id="84824-219"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="84824-219"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-220">201</span><span class="sxs-lookup"><span data-stu-id="84824-220">201</span></span></p></td>
<td><p><span data-ttu-id="84824-221">200</span><span class="sxs-lookup"><span data-stu-id="84824-221">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84824-222">Переменная</span><span class="sxs-lookup"><span data-stu-id="84824-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="84824-223"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="84824-223"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-224">130</span><span class="sxs-lookup"><span data-stu-id="84824-224">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84824-225">Переменная</span><span class="sxs-lookup"><span data-stu-id="84824-225">Variable</span></span></p></td>
<td><p><span data-ttu-id="84824-226"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="84824-226"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-227">202</span><span class="sxs-lookup"><span data-stu-id="84824-227">202</span></span></p></td>
<td><p><span data-ttu-id="84824-228">130</span><span class="sxs-lookup"><span data-stu-id="84824-228">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84824-229">Переменная</span><span class="sxs-lookup"><span data-stu-id="84824-229">Variable</span></span></p></td>
<td><p><span data-ttu-id="84824-230"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="84824-230"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-231">203</span><span class="sxs-lookup"><span data-stu-id="84824-231">203</span></span></p></td>
<td><p><span data-ttu-id="84824-232">130</span><span class="sxs-lookup"><span data-stu-id="84824-232">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84824-233">Переменная</span><span class="sxs-lookup"><span data-stu-id="84824-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="84824-234"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="84824-234"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-235">128</span><span class="sxs-lookup"><span data-stu-id="84824-235">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84824-236">Переменная</span><span class="sxs-lookup"><span data-stu-id="84824-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="84824-237"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="84824-237"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-238">204</span><span class="sxs-lookup"><span data-stu-id="84824-238">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84824-239">Переменная</span><span class="sxs-lookup"><span data-stu-id="84824-239">Variable</span></span></p></td>
<td><p><span data-ttu-id="84824-240"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="84824-240"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="84824-241">205</span><span class="sxs-lookup"><span data-stu-id="84824-241">205</span></span></p></td>
<td><p><span data-ttu-id="84824-242">204</span><span class="sxs-lookup"><span data-stu-id="84824-242">204</span></span></p></td>
</tr>
</tbody>
</table>

