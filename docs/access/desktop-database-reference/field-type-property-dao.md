---
title: Свойство Field.Type (DAO)
TOCTitle: Type Property
ms:assetid: 1295ca40-78c1-bdd0-d407-e1b5be8adfd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845405(v=office.15)
ms:contentKeyID: 48543345
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c8f212c5e1f10f4270987c9453802575d88cebfa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292953"
---
# <a name="fieldtype-property-dao"></a><span data-ttu-id="d62b0-102">Свойство Field.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="d62b0-102">Field.Type Property (DAO)</span></span>


<span data-ttu-id="d62b0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d62b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d62b0-104">Задает или возвращает значение, указывающее операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="d62b0-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="d62b0-105">Для чтения и записи, **Integer**.</span><span class="sxs-lookup"><span data-stu-id="d62b0-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d62b0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d62b0-106">Syntax</span></span>

<span data-ttu-id="d62b0-107">*выражение* .Type</span><span class="sxs-lookup"><span data-stu-id="d62b0-107">*expression* .Type</span></span>

<span data-ttu-id="d62b0-108">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="d62b0-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d62b0-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="d62b0-109">Remarks</span></span>

<span data-ttu-id="d62b0-110">Параметр или возвращаемое значение является константой, указывающей операционный тип или тип данных.</span><span class="sxs-lookup"><span data-stu-id="d62b0-110">The setting or return value is a constant that indicates an operational or data type.</span></span> <span data-ttu-id="d62b0-111">Для объекта **Field** это свойство предназначено для чтения и записи, пока объект не добавляется в коллекцию или к другому объекту, после чего он доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d62b0-111">For a **Field** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="d62b0-112">Для объекта **Field** возможные параметры и возвращаемые значения описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d62b0-112">For a **Field** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d62b0-113">Константа</span><span class="sxs-lookup"><span data-stu-id="d62b0-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="d62b0-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d62b0-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d62b0-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-116">Большое целое</span><span class="sxs-lookup"><span data-stu-id="d62b0-116">big integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d62b0-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-118">Двоичный</span><span class="sxs-lookup"><span data-stu-id="d62b0-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d62b0-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-120">Логический</span><span class="sxs-lookup"><span data-stu-id="d62b0-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d62b0-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-122">Байт</span><span class="sxs-lookup"><span data-stu-id="d62b0-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d62b0-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-124">Знак</span><span class="sxs-lookup"><span data-stu-id="d62b0-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d62b0-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-126">Денежный</span><span class="sxs-lookup"><span data-stu-id="d62b0-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d62b0-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-128">Дата и время</span><span class="sxs-lookup"><span data-stu-id="d62b0-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d62b0-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-130">Десятичный</span><span class="sxs-lookup"><span data-stu-id="d62b0-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d62b0-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-132">Двойное</span><span class="sxs-lookup"><span data-stu-id="d62b0-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d62b0-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-134">С плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="d62b0-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d62b0-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-136">Глобальный уникальный идентификатор (GUID)</span><span class="sxs-lookup"><span data-stu-id="d62b0-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d62b0-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-138">Целое</span><span class="sxs-lookup"><span data-stu-id="d62b0-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d62b0-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-140">Длинное целое</span><span class="sxs-lookup"><span data-stu-id="d62b0-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d62b0-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-142">Длинное двоичное (объект OLE)</span><span class="sxs-lookup"><span data-stu-id="d62b0-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d62b0-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-144">Memo</span><span class="sxs-lookup"><span data-stu-id="d62b0-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d62b0-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-146">Числовой</span><span class="sxs-lookup"><span data-stu-id="d62b0-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d62b0-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-148">Одинарное</span><span class="sxs-lookup"><span data-stu-id="d62b0-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d62b0-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-150">Текст</span><span class="sxs-lookup"><span data-stu-id="d62b0-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d62b0-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-152">Время</span><span class="sxs-lookup"><span data-stu-id="d62b0-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d62b0-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-154">Метка времени</span><span class="sxs-lookup"><span data-stu-id="d62b0-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d62b0-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="d62b0-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="d62b0-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="d62b0-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d62b0-157">Когда новый объект **Field**, **Parameter** или **Property** добавляется в коллекцию объектов **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** или **TableDef**, возникает ошибка, если основная база данных не поддерживает тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="d62b0-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

