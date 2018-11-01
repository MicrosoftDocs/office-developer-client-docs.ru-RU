---
title: Метод CreateRecordset (RDS)
TOCTitle: CreateRecordset Method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d975faf45cf6a16bdae9f800084ebbbbaec3127d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868534"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="6c74d-102">Метод CreateRecordset (RDS)</span><span class="sxs-lookup"><span data-stu-id="6c74d-102">CreateRecordset Method (RDS)</span></span>


<span data-ttu-id="6c74d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c74d-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="6c74d-104">Создает пустой, отключенные [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6c74d-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c74d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c74d-105">Syntax</span></span>

<span data-ttu-id="6c74d-106">*объект*. CreateRecordset (*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="6c74d-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="6c74d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c74d-107">Parameters</span></span>

  - <span data-ttu-id="6c74d-108">*Объект*</span><span class="sxs-lookup"><span data-stu-id="6c74d-108">*Object*</span></span>

  - <span data-ttu-id="6c74d-109">Объектную переменную, которая представляет [RDSServer.DataFactory](datafactory-object-rdsserver.md) или [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="6c74d-109">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="6c74d-110">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="6c74d-110">*ColumnsInfos*</span></span>

  - <span data-ttu-id="6c74d-111">Создать **Variant** массив атрибутов, определяющий столбцы в **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="6c74d-111">A **Variant** array of attributes that defines each column in the **Recordset** created.</span></span> <span data-ttu-id="6c74d-112">Определение каждого столбца содержит массив четыре обязательные атрибуты и один необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="6c74d-112">Each column definition contains an array of four required attributes and one optional attribute.</span></span> <span data-ttu-id="6c74d-113">Набор столбцов массивов нажмите сгруппированы в массив, который определяет **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="6c74d-113">The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="6c74d-114">Атрибут</span><span class="sxs-lookup"><span data-stu-id="6c74d-114">Attribute</span></span></p></th>
    <th><p><span data-ttu-id="6c74d-115">Описание</span><span class="sxs-lookup"><span data-stu-id="6c74d-115">Description</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="6c74d-116">Имя</span><span class="sxs-lookup"><span data-stu-id="6c74d-116">Name</span></span></p></td>
    <td><p><span data-ttu-id="6c74d-117">Имя заголовка столбца.</span><span class="sxs-lookup"><span data-stu-id="6c74d-117">Name of the column header.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="6c74d-118">Тип</span><span class="sxs-lookup"><span data-stu-id="6c74d-118">Type</span></span></p></td>
    <td><p><span data-ttu-id="6c74d-119">Целое число типа данных.</span><span class="sxs-lookup"><span data-stu-id="6c74d-119">Integer of the data type.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="6c74d-120">Size</span><span class="sxs-lookup"><span data-stu-id="6c74d-120">Size</span></span></p></td>
    <td><p><span data-ttu-id="6c74d-121">Целое число от ширины знаков, независимо от типа данных.</span><span class="sxs-lookup"><span data-stu-id="6c74d-121">Integer of the width in characters, regardless of data type.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="6c74d-122">Возможность принимать значение NULL</span><span class="sxs-lookup"><span data-stu-id="6c74d-122">Nullability</span></span></p></td>
    <td><p><span data-ttu-id="6c74d-123">Логическое значение.</span><span class="sxs-lookup"><span data-stu-id="6c74d-123">Boolean value.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="6c74d-124">Масштаб</span><span class="sxs-lookup"><span data-stu-id="6c74d-124">Scale</span></span><br />
<span data-ttu-id="6c74d-125">(Необязательно)</span><span class="sxs-lookup"><span data-stu-id="6c74d-125">(Optional)</span></span></p></td>
    <td><p><span data-ttu-id="6c74d-126">Этот дополнительный атрибут задает масштаб для числовых полей.</span><span class="sxs-lookup"><span data-stu-id="6c74d-126">This optional attribute defines the scale for numeric fields.</span></span> <span data-ttu-id="6c74d-127">Если это значение не указано, с горизонтальным трех усекаются числовых значений.</span><span class="sxs-lookup"><span data-stu-id="6c74d-127">If this value is not specified, numeric values will be truncated to a scale of three.</span></span> <span data-ttu-id="6c74d-128">Количество разрядов после запятой будет усечено до трех, но не повлияет точности.</span><span class="sxs-lookup"><span data-stu-id="6c74d-128">Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span></p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a><span data-ttu-id="6c74d-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="6c74d-129">Remarks</span></span>

<span data-ttu-id="6c74d-130">На сервере бизнес-объекта можно заполнить результирующего **набора записей** с данными из не - поставщиков данных OLE DB, такие как файл операционной системы, содержащий акций.</span><span class="sxs-lookup"><span data-stu-id="6c74d-130">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="6c74d-131">В следующей таблице перечислены значения [DataTypeEnum](datatypeenum.md) , поддерживаемый метод **CreateRecordset** .</span><span class="sxs-lookup"><span data-stu-id="6c74d-131">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method.</span></span> <span data-ttu-id="6c74d-132">Номер, указанный является номер ссылки, используемые для определения полей.</span><span class="sxs-lookup"><span data-stu-id="6c74d-132">The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="6c74d-133">Каждый из типов данных является фиксированной длины или переменной длины.</span><span class="sxs-lookup"><span data-stu-id="6c74d-133">Each of the data types is either fixed length or variable length.</span></span> <span data-ttu-id="6c74d-134">Типы фиксированной длины должны быть определены с размером – 1, так как предварительно определенный размер и определение размера по-прежнему требуется.</span><span class="sxs-lookup"><span data-stu-id="6c74d-134">Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required.</span></span> <span data-ttu-id="6c74d-135">Типы данных переменной длины разрешить размер от 1 до 32767.</span><span class="sxs-lookup"><span data-stu-id="6c74d-135">Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="6c74d-136">Для некоторых типов данных переменной тип может привести к типу, указаны в столбце подстановки.</span><span class="sxs-lookup"><span data-stu-id="6c74d-136">For some of the variable data types, the type may be coerced to the type noted in the Substitution column.</span></span> <span data-ttu-id="6c74d-137">Вы не увидите замены до того времени, после создания и заполнения **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="6c74d-137">You won't see the substitutions until after the **Recordset** is created and filled.</span></span> <span data-ttu-id="6c74d-138">Затем следует проверить, тип фактических данных, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="6c74d-138">Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c74d-139">Length</span><span class="sxs-lookup"><span data-stu-id="6c74d-139">Length</span></span></p></th>
<th><p><span data-ttu-id="6c74d-140">Constant</span><span class="sxs-lookup"><span data-stu-id="6c74d-140">Constant</span></span></p></th>
<th><p><span data-ttu-id="6c74d-141">Number</span><span class="sxs-lookup"><span data-stu-id="6c74d-141">Number</span></span></p></th>
<th><p><span data-ttu-id="6c74d-142">Замена </span><span class="sxs-lookup"><span data-stu-id="6c74d-142">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c74d-143">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-143">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-144"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-144"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-145">16</span><span class="sxs-lookup"><span data-stu-id="6c74d-145">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c74d-146">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-147"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-147"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-148">2</span><span class="sxs-lookup"><span data-stu-id="6c74d-148">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c74d-149">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-150"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-150"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-151">3</span><span class="sxs-lookup"><span data-stu-id="6c74d-151">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c74d-152">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-153"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-153"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-154">20</span><span class="sxs-lookup"><span data-stu-id="6c74d-154">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c74d-155">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-156"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-156"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-157">17</span><span class="sxs-lookup"><span data-stu-id="6c74d-157">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c74d-158">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-159"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-159"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-160">18</span><span class="sxs-lookup"><span data-stu-id="6c74d-160">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c74d-161">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-162"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-162"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-163">19</span><span class="sxs-lookup"><span data-stu-id="6c74d-163">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c74d-164">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-165"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-165"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-166">21</span><span class="sxs-lookup"><span data-stu-id="6c74d-166">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c74d-167">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-168"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-168"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-169">4</span><span class="sxs-lookup"><span data-stu-id="6c74d-169">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c74d-170">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-171"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-171"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-172">5</span><span class="sxs-lookup"><span data-stu-id="6c74d-172">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c74d-173">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-174"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-174"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-175">6</span><span class="sxs-lookup"><span data-stu-id="6c74d-175">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c74d-176">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-177"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-177"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-178">14</span><span class="sxs-lookup"><span data-stu-id="6c74d-178">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c74d-179">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-180"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-180"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-181">131</span><span class="sxs-lookup"><span data-stu-id="6c74d-181">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c74d-182">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-183"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-183"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-184">11</span><span class="sxs-lookup"><span data-stu-id="6c74d-184">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c74d-185">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-186"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-186"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-187">10</span><span class="sxs-lookup"><span data-stu-id="6c74d-187">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c74d-188">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-189"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-189"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-190">72</span><span class="sxs-lookup"><span data-stu-id="6c74d-190">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c74d-191">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-192"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-192"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-193">7</span><span class="sxs-lookup"><span data-stu-id="6c74d-193">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c74d-194">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-195"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-195"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-196">133</span><span class="sxs-lookup"><span data-stu-id="6c74d-196">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c74d-197">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-198"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-198"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-199">134</span><span class="sxs-lookup"><span data-stu-id="6c74d-199">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c74d-200">Фиксация</span><span class="sxs-lookup"><span data-stu-id="6c74d-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="6c74d-201"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-201"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-202">135</span><span class="sxs-lookup"><span data-stu-id="6c74d-202">135</span></span></p></td>
<td><p><span data-ttu-id="6c74d-203">7</span><span class="sxs-lookup"><span data-stu-id="6c74d-203">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c74d-204">Переменная</span><span class="sxs-lookup"><span data-stu-id="6c74d-204">Variable</span></span></p></td>
<td><p><span data-ttu-id="6c74d-205"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-205"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-206">8</span><span class="sxs-lookup"><span data-stu-id="6c74d-206">8</span></span></p></td>
<td><p><span data-ttu-id="6c74d-207">130</span><span class="sxs-lookup"><span data-stu-id="6c74d-207">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c74d-208">Переменная</span><span class="sxs-lookup"><span data-stu-id="6c74d-208">Variable</span></span></p></td>
<td><p><span data-ttu-id="6c74d-209"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-209"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-210">129</span><span class="sxs-lookup"><span data-stu-id="6c74d-210">129</span></span></p></td>
<td><p><span data-ttu-id="6c74d-211">200</span><span class="sxs-lookup"><span data-stu-id="6c74d-211">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c74d-212">Переменная</span><span class="sxs-lookup"><span data-stu-id="6c74d-212">Variable</span></span></p></td>
<td><p><span data-ttu-id="6c74d-213"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-213"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-214">200</span><span class="sxs-lookup"><span data-stu-id="6c74d-214">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c74d-215">Переменная</span><span class="sxs-lookup"><span data-stu-id="6c74d-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="6c74d-216"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-216"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-217">201</span><span class="sxs-lookup"><span data-stu-id="6c74d-217">201</span></span></p></td>
<td><p><span data-ttu-id="6c74d-218">200</span><span class="sxs-lookup"><span data-stu-id="6c74d-218">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c74d-219">Переменная</span><span class="sxs-lookup"><span data-stu-id="6c74d-219">Variable</span></span></p></td>
<td><p><span data-ttu-id="6c74d-220"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-220"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-221">130</span><span class="sxs-lookup"><span data-stu-id="6c74d-221">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c74d-222">Переменная</span><span class="sxs-lookup"><span data-stu-id="6c74d-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="6c74d-223"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-223"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-224">202</span><span class="sxs-lookup"><span data-stu-id="6c74d-224">202</span></span></p></td>
<td><p><span data-ttu-id="6c74d-225">130</span><span class="sxs-lookup"><span data-stu-id="6c74d-225">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c74d-226">Переменная</span><span class="sxs-lookup"><span data-stu-id="6c74d-226">Variable</span></span></p></td>
<td><p><span data-ttu-id="6c74d-227"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-227"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-228">203</span><span class="sxs-lookup"><span data-stu-id="6c74d-228">203</span></span></p></td>
<td><p><span data-ttu-id="6c74d-229">130</span><span class="sxs-lookup"><span data-stu-id="6c74d-229">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c74d-230">Переменная</span><span class="sxs-lookup"><span data-stu-id="6c74d-230">Variable</span></span></p></td>
<td><p><span data-ttu-id="6c74d-231"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-231"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-232">128</span><span class="sxs-lookup"><span data-stu-id="6c74d-232">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c74d-233">Переменная</span><span class="sxs-lookup"><span data-stu-id="6c74d-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="6c74d-234"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-234"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-235">204</span><span class="sxs-lookup"><span data-stu-id="6c74d-235">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c74d-236">Переменная</span><span class="sxs-lookup"><span data-stu-id="6c74d-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="6c74d-237"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="6c74d-237"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="6c74d-238">205</span><span class="sxs-lookup"><span data-stu-id="6c74d-238">205</span></span></p></td>
<td><p><span data-ttu-id="6c74d-239">204</span><span class="sxs-lookup"><span data-stu-id="6c74d-239">204</span></span></p></td>
</tr>
</tbody>
</table>

