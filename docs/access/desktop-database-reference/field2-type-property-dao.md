---
title: Свойство Field2.Type (DAO)
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
# <a name="field2type-property-dao"></a><span data-ttu-id="49e1e-102">Свойство Field2.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="49e1e-102">Field2.Type property (DAO)</span></span>


<span data-ttu-id="49e1e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49e1e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49e1e-104">Задает или возвращает значение, указывающее операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="49e1e-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="49e1e-105">Для чтения и записи, **Integer**.</span><span class="sxs-lookup"><span data-stu-id="49e1e-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="49e1e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49e1e-106">Syntax</span></span>

<span data-ttu-id="49e1e-107">*выражение* .Type</span><span class="sxs-lookup"><span data-stu-id="49e1e-107">*expression* .Type</span></span>

<span data-ttu-id="49e1e-108">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="49e1e-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="49e1e-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="49e1e-109">Remarks</span></span>

<span data-ttu-id="49e1e-110">Параметр или возвращаемое значение является константой, указывающей операционный тип или тип данных.</span><span class="sxs-lookup"><span data-stu-id="49e1e-110">The setting or return value is a constant that indicates an operational or data type.</span></span> <span data-ttu-id="49e1e-111">Для объекта **Field2** это свойство считывать и записывать, пока объект не будет appended к коллекции или другому объекту, после чего он будет только для чтения.</span><span class="sxs-lookup"><span data-stu-id="49e1e-111">For a **Field2** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="49e1e-112">Для объекта **Field2** возможные параметры и возвращаемые значения описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="49e1e-112">For a **Field2** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49e1e-113">Константа</span><span class="sxs-lookup"><span data-stu-id="49e1e-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="49e1e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="49e1e-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49e1e-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-116">Большое целое</span><span class="sxs-lookup"><span data-stu-id="49e1e-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e1e-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-118">Двоичный</span><span class="sxs-lookup"><span data-stu-id="49e1e-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e1e-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-120">Логический</span><span class="sxs-lookup"><span data-stu-id="49e1e-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e1e-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-122">Байт</span><span class="sxs-lookup"><span data-stu-id="49e1e-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e1e-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-124">Знак</span><span class="sxs-lookup"><span data-stu-id="49e1e-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e1e-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-126">Денежный</span><span class="sxs-lookup"><span data-stu-id="49e1e-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e1e-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-128">Дата и время</span><span class="sxs-lookup"><span data-stu-id="49e1e-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e1e-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-130">Десятичный</span><span class="sxs-lookup"><span data-stu-id="49e1e-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e1e-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-132">Двойное</span><span class="sxs-lookup"><span data-stu-id="49e1e-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e1e-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-134">С плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="49e1e-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e1e-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-136">Глобальный уникальный идентификатор (GUID)</span><span class="sxs-lookup"><span data-stu-id="49e1e-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e1e-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-138">Целое</span><span class="sxs-lookup"><span data-stu-id="49e1e-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e1e-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-140">Длинное целое</span><span class="sxs-lookup"><span data-stu-id="49e1e-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e1e-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-142">Длинное двоичное (объект OLE)</span><span class="sxs-lookup"><span data-stu-id="49e1e-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e1e-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-144">Memo</span><span class="sxs-lookup"><span data-stu-id="49e1e-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e1e-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-146">Числовой</span><span class="sxs-lookup"><span data-stu-id="49e1e-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e1e-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-148">Одинарное</span><span class="sxs-lookup"><span data-stu-id="49e1e-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e1e-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-150">Текст</span><span class="sxs-lookup"><span data-stu-id="49e1e-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e1e-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-152">Время</span><span class="sxs-lookup"><span data-stu-id="49e1e-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49e1e-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-154">Метка времени</span><span class="sxs-lookup"><span data-stu-id="49e1e-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49e1e-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="49e1e-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="49e1e-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="49e1e-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49e1e-157">При приложении нового объекта **Field2**, **Parameter** или **Property** к коллекции объекта **Index,** **QueryDef,** **Recordset** или **TableDef** возникает ошибка, если базовая база данных не поддерживает тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="49e1e-157">When you append a new **Field2**, **Parameter**, or **Property** object to the collection of an **Index**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

