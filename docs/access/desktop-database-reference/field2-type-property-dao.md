---
title: Свойство field2. Type (DAO)
TOCTitle: Type Property
ms:assetid: 057d6ec9-b72c-cee6-005a-6d916e3dda29
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844921(v=office.15)
ms:contentKeyID: 48543032
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4da32f18a2b3e9dddbb0ae04e3257de34ba09761
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292666"
---
# <a name="field2type-property-dao"></a><span data-ttu-id="c0ebe-102">Свойство field2. Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="c0ebe-102">Field2.Type property (DAO)</span></span>


<span data-ttu-id="c0ebe-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0ebe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c0ebe-104">Задает или возвращает значение, указывающее операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="c0ebe-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="c0ebe-105">Для чтения и записи, **Integer**.</span><span class="sxs-lookup"><span data-stu-id="c0ebe-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ebe-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0ebe-106">Syntax</span></span>

<span data-ttu-id="c0ebe-107">*выражение* .Type</span><span class="sxs-lookup"><span data-stu-id="c0ebe-107">*expression* .Type</span></span>

<span data-ttu-id="c0ebe-108">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="c0ebe-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0ebe-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="c0ebe-109">Remarks</span></span>

<span data-ttu-id="c0ebe-110">Параметр или возвращаемое значение является константой, указывающей операционный тип или тип данных.</span><span class="sxs-lookup"><span data-stu-id="c0ebe-110">The setting or return value is a constant that indicates an operational or data type.</span></span> <span data-ttu-id="c0ebe-111">Для объекта **field2** это свойство доступно для чтения и записи до тех пор, пока объект не будет добавлен в коллекцию или другой объект, после которого он доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c0ebe-111">For a **Field2** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="c0ebe-112">В приведенной ниже таблице описаны возможные параметры и возвращаемые значения для объекта **field2** .</span><span class="sxs-lookup"><span data-stu-id="c0ebe-112">For a **Field2** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c0ebe-113">Константа</span><span class="sxs-lookup"><span data-stu-id="c0ebe-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="c0ebe-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c0ebe-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0ebe-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-116">Большое целое</span><span class="sxs-lookup"><span data-stu-id="c0ebe-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0ebe-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-118">Двоичный</span><span class="sxs-lookup"><span data-stu-id="c0ebe-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0ebe-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-120">Логический</span><span class="sxs-lookup"><span data-stu-id="c0ebe-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0ebe-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-122">Байт</span><span class="sxs-lookup"><span data-stu-id="c0ebe-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0ebe-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-124">Знак</span><span class="sxs-lookup"><span data-stu-id="c0ebe-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0ebe-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-126">Денежный</span><span class="sxs-lookup"><span data-stu-id="c0ebe-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0ebe-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-128">Дата и время</span><span class="sxs-lookup"><span data-stu-id="c0ebe-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0ebe-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-130">Десятичный</span><span class="sxs-lookup"><span data-stu-id="c0ebe-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0ebe-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-132">Двойное</span><span class="sxs-lookup"><span data-stu-id="c0ebe-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0ebe-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-134">С плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="c0ebe-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0ebe-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-136">Глобальный уникальный идентификатор (GUID)</span><span class="sxs-lookup"><span data-stu-id="c0ebe-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0ebe-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-138">Целое</span><span class="sxs-lookup"><span data-stu-id="c0ebe-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0ebe-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-140">Длинное целое</span><span class="sxs-lookup"><span data-stu-id="c0ebe-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0ebe-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-142">Длинное двоичное (объект OLE)</span><span class="sxs-lookup"><span data-stu-id="c0ebe-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0ebe-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-144">Memo</span><span class="sxs-lookup"><span data-stu-id="c0ebe-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0ebe-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-146">Числовой</span><span class="sxs-lookup"><span data-stu-id="c0ebe-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0ebe-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-148">Одинарное</span><span class="sxs-lookup"><span data-stu-id="c0ebe-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0ebe-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-150">Текст</span><span class="sxs-lookup"><span data-stu-id="c0ebe-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0ebe-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-152">Время</span><span class="sxs-lookup"><span data-stu-id="c0ebe-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0ebe-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-154">Метка времени</span><span class="sxs-lookup"><span data-stu-id="c0ebe-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0ebe-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="c0ebe-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="c0ebe-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="c0ebe-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c0ebe-157">При добавлении нового объекта **field2**, **параметра**или **Свойства** в коллекцию объекта **index**, **QueryDef**, **Recordset**или **tabledef** возникает ошибка, если базовая база данных не поддерживает тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="c0ebe-157">When you append a new **Field2**, **Parameter**, or **Property** object to the collection of an **Index**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

