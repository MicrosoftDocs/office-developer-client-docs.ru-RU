---
title: Свойство Property. Type (DAO)
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
# <a name="propertytype-property-dao"></a><span data-ttu-id="b6933-102">Свойство Property. Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="b6933-102">Property.Type property (DAO)</span></span>


<span data-ttu-id="b6933-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b6933-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b6933-104">Задает или возвращает значение, указывающее операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="b6933-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="b6933-105">Для чтения и записи, **Integer**.</span><span class="sxs-lookup"><span data-stu-id="b6933-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6933-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6933-106">Syntax</span></span>

<span data-ttu-id="b6933-107">*выражение* .Type</span><span class="sxs-lookup"><span data-stu-id="b6933-107">*expression* .Type</span></span>

<span data-ttu-id="b6933-108">*Expression (выражение* ) Переменная, представляющая объект **Property** .</span><span class="sxs-lookup"><span data-stu-id="b6933-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6933-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="b6933-109">Remarks</span></span>

<span data-ttu-id="b6933-110">Параметр или возвращаемое значение является константой, указывающей операционный тип или тип данных.</span><span class="sxs-lookup"><span data-stu-id="b6933-110">The setting or return value is a constant that indicates an operational or data type.</span></span> <span data-ttu-id="b6933-111">Для объекта **[Property](property-object-dao.md)** это свойство доступно для чтения и записи до тех пор, пока объект не будет добавлен в коллекцию или другой объект, после которого он доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b6933-111">For a **[Property](property-object-dao.md)** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="b6933-112">В приведенной ниже таблице описаны возможные параметры и возвращаемые значения для объекта **Property** .</span><span class="sxs-lookup"><span data-stu-id="b6933-112">For a **Property** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b6933-113">Константа</span><span class="sxs-lookup"><span data-stu-id="b6933-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="b6933-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b6933-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6933-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-116">Большое целое</span><span class="sxs-lookup"><span data-stu-id="b6933-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6933-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-118">Двоичный</span><span class="sxs-lookup"><span data-stu-id="b6933-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6933-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-120">Логический</span><span class="sxs-lookup"><span data-stu-id="b6933-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6933-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-122">Байт</span><span class="sxs-lookup"><span data-stu-id="b6933-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6933-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-124">Знак</span><span class="sxs-lookup"><span data-stu-id="b6933-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6933-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-126">Денежный</span><span class="sxs-lookup"><span data-stu-id="b6933-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6933-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-128">Дата и время</span><span class="sxs-lookup"><span data-stu-id="b6933-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6933-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-130">Десятичный</span><span class="sxs-lookup"><span data-stu-id="b6933-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6933-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-132">Двойное</span><span class="sxs-lookup"><span data-stu-id="b6933-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6933-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-134">С плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="b6933-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6933-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-136">Глобальный уникальный идентификатор (GUID)</span><span class="sxs-lookup"><span data-stu-id="b6933-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6933-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-138">Целое</span><span class="sxs-lookup"><span data-stu-id="b6933-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6933-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-140">Длинное целое</span><span class="sxs-lookup"><span data-stu-id="b6933-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6933-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-142">Длинное двоичное (объект OLE)</span><span class="sxs-lookup"><span data-stu-id="b6933-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6933-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-144">Memo</span><span class="sxs-lookup"><span data-stu-id="b6933-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6933-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-146">Числовой</span><span class="sxs-lookup"><span data-stu-id="b6933-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6933-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-148">Одинарное</span><span class="sxs-lookup"><span data-stu-id="b6933-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6933-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-150">Текст</span><span class="sxs-lookup"><span data-stu-id="b6933-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6933-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-152">Время</span><span class="sxs-lookup"><span data-stu-id="b6933-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6933-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-154">Метка времени</span><span class="sxs-lookup"><span data-stu-id="b6933-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6933-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="b6933-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="b6933-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="b6933-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b6933-157">Когда новый объект **Field**, **Parameter** или **Property** добавляется в коллекцию объектов **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** или **TableDef**, возникает ошибка, если основная база данных не поддерживает тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="b6933-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

