---
title: CreateRecordset Method (RDS)
TOCTitle: CreateRecordset Method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 696daaeb060387d5f3ca454ef665517a8ff7be74
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480019"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="44578-102">CreateRecordset Method (RDS)</span><span class="sxs-lookup"><span data-stu-id="44578-102">CreateRecordset Method (RDS)</span></span>


<span data-ttu-id="44578-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="44578-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="44578-104">Создает пустой, отключенные [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="44578-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="44578-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44578-105">Syntax</span></span>

<span data-ttu-id="44578-106">*объект*. CreateRecordset (*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="44578-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="44578-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="44578-107">Parameters</span></span>

  - <span data-ttu-id="44578-108">*Объект*</span><span class="sxs-lookup"><span data-stu-id="44578-108">*Object*</span></span>

  - <span data-ttu-id="44578-109">Объектную переменную, которая представляет [RDSServer.DataFactory](datafactory-object-rdsserver.md) или [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="44578-109">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="44578-110">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="44578-110">*ColumnsInfos*</span></span>

  - <span data-ttu-id="44578-111">Создать **Variant** массив атрибутов, определяющий столбцы в **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="44578-111">A **Variant** array of attributes that defines each column in the **Recordset** created.</span></span> <span data-ttu-id="44578-112">Определение каждого столбца содержит массив четыре обязательные атрибуты и один необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="44578-112">Each column definition contains an array of four required attributes and one optional attribute.</span></span> <span data-ttu-id="44578-113">Набор столбцов массивов нажмите сгруппированы в массив, который определяет **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="44578-113">The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="44578-114">Атрибут</span><span class="sxs-lookup"><span data-stu-id="44578-114">Attribute</span></span></p></th>
    <th><p><span data-ttu-id="44578-115">Описание</span><span class="sxs-lookup"><span data-stu-id="44578-115">Description</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="44578-116">Имя</span><span class="sxs-lookup"><span data-stu-id="44578-116">Name</span></span></p></td>
    <td><p><span data-ttu-id="44578-117">Имя заголовка столбца.</span><span class="sxs-lookup"><span data-stu-id="44578-117">Name of the column header.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="44578-118">Тип</span><span class="sxs-lookup"><span data-stu-id="44578-118">Type</span></span></p></td>
    <td><p><span data-ttu-id="44578-119">Целое число типа данных.</span><span class="sxs-lookup"><span data-stu-id="44578-119">Integer of the data type.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="44578-120">Size</span><span class="sxs-lookup"><span data-stu-id="44578-120">Size</span></span></p></td>
    <td><p><span data-ttu-id="44578-121">Целое число от ширины знаков, независимо от типа данных.</span><span class="sxs-lookup"><span data-stu-id="44578-121">Integer of the width in characters, regardless of data type.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="44578-122">Возможность принимать значение NULL</span><span class="sxs-lookup"><span data-stu-id="44578-122">Nullability</span></span></p></td>
    <td><p><span data-ttu-id="44578-123">Логическое значение.</span><span class="sxs-lookup"><span data-stu-id="44578-123">Boolean value.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="44578-124">Масштаб</span><span class="sxs-lookup"><span data-stu-id="44578-124">Scale</span></span><br />
<span data-ttu-id="44578-125">(Необязательно)</span><span class="sxs-lookup"><span data-stu-id="44578-125">(Optional)</span></span></p></td>
    <td><p><span data-ttu-id="44578-126">Этот дополнительный атрибут задает масштаб для числовых полей.</span><span class="sxs-lookup"><span data-stu-id="44578-126">This optional attribute defines the scale for numeric fields.</span></span> <span data-ttu-id="44578-127">Если это значение не указано, с горизонтальным трех усекаются числовых значений.</span><span class="sxs-lookup"><span data-stu-id="44578-127">If this value is not specified, numeric values will be truncated to a scale of three.</span></span> <span data-ttu-id="44578-128">Количество разрядов после запятой будет усечено до трех, но не повлияет точности.</span><span class="sxs-lookup"><span data-stu-id="44578-128">Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span></p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a><span data-ttu-id="44578-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="44578-129">Remarks</span></span>

<span data-ttu-id="44578-130">На сервере бизнес-объекта можно заполнить результирующего **набора записей** с данными из не - поставщиков данных OLE DB, такие как файл операционной системы, содержащий акций.</span><span class="sxs-lookup"><span data-stu-id="44578-130">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="44578-131">В следующей таблице перечислены значения [DataTypeEnum](datatypeenum.md) , поддерживаемый метод **CreateRecordset** .</span><span class="sxs-lookup"><span data-stu-id="44578-131">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method.</span></span> <span data-ttu-id="44578-132">Номер, указанный является номер ссылки, используемые для определения полей.</span><span class="sxs-lookup"><span data-stu-id="44578-132">The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="44578-133">Каждый из типов данных является фиксированной длины или переменной длины.</span><span class="sxs-lookup"><span data-stu-id="44578-133">Each of the data types is either fixed length or variable length.</span></span> <span data-ttu-id="44578-134">Типы фиксированной длины должны быть определены с размером – 1, так как предварительно определенный размер и определение размера по-прежнему требуется.</span><span class="sxs-lookup"><span data-stu-id="44578-134">Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required.</span></span> <span data-ttu-id="44578-135">Типы данных переменной длины разрешить размер от 1 до 32767.</span><span class="sxs-lookup"><span data-stu-id="44578-135">Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="44578-136">Для некоторых типов данных переменной тип может привести к типу, указаны в столбце подстановки.</span><span class="sxs-lookup"><span data-stu-id="44578-136">For some of the variable data types, the type may be coerced to the type noted in the Substitution column.</span></span> <span data-ttu-id="44578-137">Вы не увидите замены до того времени, после создания и заполнения **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="44578-137">You won't see the substitutions until after the **Recordset** is created and filled.</span></span> <span data-ttu-id="44578-138">Затем следует проверить, тип фактических данных, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="44578-138">Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="44578-139">Length</span><span class="sxs-lookup"><span data-stu-id="44578-139">Length</span></span></p></th>
<th><p><span data-ttu-id="44578-140">Constant</span><span class="sxs-lookup"><span data-stu-id="44578-140">Constant</span></span></p></th>
<th><p><span data-ttu-id="44578-141">Number</span><span class="sxs-lookup"><span data-stu-id="44578-141">Number</span></span></p></th>
<th><p><span data-ttu-id="44578-142">Замена </span><span class="sxs-lookup"><span data-stu-id="44578-142">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44578-143">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-143">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-144"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="44578-144"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-145">16</span><span class="sxs-lookup"><span data-stu-id="44578-145">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44578-146">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-147"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="44578-147"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-148">2</span><span class="sxs-lookup"><span data-stu-id="44578-148">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44578-149">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-150"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="44578-150"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-151">3</span><span class="sxs-lookup"><span data-stu-id="44578-151">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44578-152">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-153"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="44578-153"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-154">20</span><span class="sxs-lookup"><span data-stu-id="44578-154">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44578-155">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-156"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="44578-156"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-157">17</span><span class="sxs-lookup"><span data-stu-id="44578-157">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44578-158">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-159"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="44578-159"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-160">18</span><span class="sxs-lookup"><span data-stu-id="44578-160">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44578-161">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-162"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="44578-162"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-163">19</span><span class="sxs-lookup"><span data-stu-id="44578-163">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44578-164">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-165"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="44578-165"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-166">21</span><span class="sxs-lookup"><span data-stu-id="44578-166">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44578-167">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-168"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="44578-168"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-169">4</span><span class="sxs-lookup"><span data-stu-id="44578-169">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44578-170">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-171"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="44578-171"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-172">5</span><span class="sxs-lookup"><span data-stu-id="44578-172">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44578-173">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-174"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="44578-174"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-175">6</span><span class="sxs-lookup"><span data-stu-id="44578-175">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44578-176">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-177"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="44578-177"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-178">14</span><span class="sxs-lookup"><span data-stu-id="44578-178">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44578-179">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-180"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="44578-180"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-181">131</span><span class="sxs-lookup"><span data-stu-id="44578-181">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44578-182">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-183"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="44578-183"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-184">11</span><span class="sxs-lookup"><span data-stu-id="44578-184">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44578-185">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-186"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="44578-186"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-187">10</span><span class="sxs-lookup"><span data-stu-id="44578-187">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44578-188">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-189"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="44578-189"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-190">72</span><span class="sxs-lookup"><span data-stu-id="44578-190">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44578-191">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-192"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="44578-192"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-193">7</span><span class="sxs-lookup"><span data-stu-id="44578-193">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44578-194">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-195"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="44578-195"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-196">133</span><span class="sxs-lookup"><span data-stu-id="44578-196">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44578-197">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-198"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="44578-198"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-199">134</span><span class="sxs-lookup"><span data-stu-id="44578-199">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44578-200">Фиксация</span><span class="sxs-lookup"><span data-stu-id="44578-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="44578-201"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="44578-201"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-202">135</span><span class="sxs-lookup"><span data-stu-id="44578-202">135</span></span></p></td>
<td><p><span data-ttu-id="44578-203">7</span><span class="sxs-lookup"><span data-stu-id="44578-203">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44578-204">Переменная</span><span class="sxs-lookup"><span data-stu-id="44578-204">Variable</span></span></p></td>
<td><p><span data-ttu-id="44578-205"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="44578-205"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-206">8</span><span class="sxs-lookup"><span data-stu-id="44578-206">8</span></span></p></td>
<td><p><span data-ttu-id="44578-207">130</span><span class="sxs-lookup"><span data-stu-id="44578-207">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44578-208">Переменная</span><span class="sxs-lookup"><span data-stu-id="44578-208">Variable</span></span></p></td>
<td><p><span data-ttu-id="44578-209"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="44578-209"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-210">129</span><span class="sxs-lookup"><span data-stu-id="44578-210">129</span></span></p></td>
<td><p><span data-ttu-id="44578-211">200</span><span class="sxs-lookup"><span data-stu-id="44578-211">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44578-212">Переменная</span><span class="sxs-lookup"><span data-stu-id="44578-212">Variable</span></span></p></td>
<td><p><span data-ttu-id="44578-213"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="44578-213"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-214">200</span><span class="sxs-lookup"><span data-stu-id="44578-214">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44578-215">Переменная</span><span class="sxs-lookup"><span data-stu-id="44578-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="44578-216"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="44578-216"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-217">201</span><span class="sxs-lookup"><span data-stu-id="44578-217">201</span></span></p></td>
<td><p><span data-ttu-id="44578-218">200</span><span class="sxs-lookup"><span data-stu-id="44578-218">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44578-219">Переменная</span><span class="sxs-lookup"><span data-stu-id="44578-219">Variable</span></span></p></td>
<td><p><span data-ttu-id="44578-220"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="44578-220"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-221">130</span><span class="sxs-lookup"><span data-stu-id="44578-221">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44578-222">Переменная</span><span class="sxs-lookup"><span data-stu-id="44578-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="44578-223"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="44578-223"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-224">202</span><span class="sxs-lookup"><span data-stu-id="44578-224">202</span></span></p></td>
<td><p><span data-ttu-id="44578-225">130</span><span class="sxs-lookup"><span data-stu-id="44578-225">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44578-226">Переменная</span><span class="sxs-lookup"><span data-stu-id="44578-226">Variable</span></span></p></td>
<td><p><span data-ttu-id="44578-227"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="44578-227"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-228">203</span><span class="sxs-lookup"><span data-stu-id="44578-228">203</span></span></p></td>
<td><p><span data-ttu-id="44578-229">130</span><span class="sxs-lookup"><span data-stu-id="44578-229">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44578-230">Переменная</span><span class="sxs-lookup"><span data-stu-id="44578-230">Variable</span></span></p></td>
<td><p><span data-ttu-id="44578-231"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="44578-231"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-232">128</span><span class="sxs-lookup"><span data-stu-id="44578-232">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44578-233">Переменная</span><span class="sxs-lookup"><span data-stu-id="44578-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="44578-234"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="44578-234"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-235">204</span><span class="sxs-lookup"><span data-stu-id="44578-235">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44578-236">Переменная</span><span class="sxs-lookup"><span data-stu-id="44578-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="44578-237"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="44578-237"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="44578-238">205</span><span class="sxs-lookup"><span data-stu-id="44578-238">205</span></span></p></td>
<td><p><span data-ttu-id="44578-239">204</span><span class="sxs-lookup"><span data-stu-id="44578-239">204</span></span></p></td>
</tr>
</tbody>
</table>

