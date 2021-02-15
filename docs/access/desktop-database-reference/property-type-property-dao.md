---
title: Свойство Property.Type (DAO)
TOCTitle: Type Property
ms:assetid: bf8258ca-08b5-c4f9-e6d7-114e4300b2ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822796(v=office.15)
ms:contentKeyID: 48547490
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4280b89102e06b2ecc09a783840e671b0af9ff73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302902"
---
# <a name="propertytype-property-dao"></a><span data-ttu-id="1f894-102">Свойство Property.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="1f894-102">Property.Type property (DAO)</span></span>


<span data-ttu-id="1f894-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f894-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f894-104">Задает или возвращает значение, указывающее операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="1f894-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="1f894-105">Для чтения и записи, **Integer**.</span><span class="sxs-lookup"><span data-stu-id="1f894-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f894-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f894-106">Syntax</span></span>

<span data-ttu-id="1f894-107">*выражение* .Type</span><span class="sxs-lookup"><span data-stu-id="1f894-107">*expression* .Type</span></span>

<span data-ttu-id="1f894-108">*выражение* Переменная, представляюная объект **Property.**</span><span class="sxs-lookup"><span data-stu-id="1f894-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f894-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="1f894-109">Remarks</span></span>

<span data-ttu-id="1f894-110">Параметр или возвращаемое значение является константой, указывающей операционный тип или тип данных.</span><span class="sxs-lookup"><span data-stu-id="1f894-110">The setting or return value is a constant that indicates an operational or data type.</span></span> <span data-ttu-id="1f894-111">Для объекта **[Property](property-object-dao.md)** это свойство считывать и записывать, пока объект не будет appended к коллекции или другому объекту, после чего он будет только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1f894-111">For a **[Property](property-object-dao.md)** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="1f894-112">Для объекта **Property** возможные параметры и возвращаемые значения описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1f894-112">For a **Property** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f894-113">Константа</span><span class="sxs-lookup"><span data-stu-id="1f894-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="1f894-114">Описание</span><span class="sxs-lookup"><span data-stu-id="1f894-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f894-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-116">Большое целое</span><span class="sxs-lookup"><span data-stu-id="1f894-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f894-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-118">Двоичный</span><span class="sxs-lookup"><span data-stu-id="1f894-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f894-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-120">Логический</span><span class="sxs-lookup"><span data-stu-id="1f894-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f894-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-122">Байт</span><span class="sxs-lookup"><span data-stu-id="1f894-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f894-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-124">Знак</span><span class="sxs-lookup"><span data-stu-id="1f894-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f894-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-126">Денежный</span><span class="sxs-lookup"><span data-stu-id="1f894-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f894-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-128">Дата и время</span><span class="sxs-lookup"><span data-stu-id="1f894-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f894-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-130">Десятичный</span><span class="sxs-lookup"><span data-stu-id="1f894-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f894-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-132">Двойное</span><span class="sxs-lookup"><span data-stu-id="1f894-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f894-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-134">С плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="1f894-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f894-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-136">Глобальный уникальный идентификатор (GUID)</span><span class="sxs-lookup"><span data-stu-id="1f894-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f894-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-138">Целое</span><span class="sxs-lookup"><span data-stu-id="1f894-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f894-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-140">Длинное целое</span><span class="sxs-lookup"><span data-stu-id="1f894-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f894-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-142">Длинное двоичное (объект OLE)</span><span class="sxs-lookup"><span data-stu-id="1f894-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f894-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-144">Memo</span><span class="sxs-lookup"><span data-stu-id="1f894-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f894-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-146">Числовой</span><span class="sxs-lookup"><span data-stu-id="1f894-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f894-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-148">Одинарное</span><span class="sxs-lookup"><span data-stu-id="1f894-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f894-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-150">Текст</span><span class="sxs-lookup"><span data-stu-id="1f894-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f894-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-152">Время</span><span class="sxs-lookup"><span data-stu-id="1f894-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f894-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-154">Метка времени</span><span class="sxs-lookup"><span data-stu-id="1f894-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f894-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="1f894-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="1f894-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="1f894-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1f894-157">Когда новый объект **Field**, **Parameter** или **Property** добавляется в коллекцию объектов **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** или **TableDef**, возникает ошибка, если основная база данных не поддерживает тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="1f894-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

