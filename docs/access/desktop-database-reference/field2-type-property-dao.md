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
# <a name="field2type-property-dao"></a><span data-ttu-id="73eec-102">Свойство field2. Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="73eec-102">Field2.Type property (DAO)</span></span>


<span data-ttu-id="73eec-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="73eec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="73eec-104">Задает или возвращает значение, которое указывает операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="73eec-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="73eec-105">Чтение и запись **целоГо числа**.</span><span class="sxs-lookup"><span data-stu-id="73eec-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="73eec-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73eec-106">Syntax</span></span>

<span data-ttu-id="73eec-107">*Expression* . Тип</span><span class="sxs-lookup"><span data-stu-id="73eec-107">*expression* .Type</span></span>

<span data-ttu-id="73eec-108">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="73eec-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="73eec-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="73eec-109">Remarks</span></span>

<span data-ttu-id="73eec-110">Параметр или возвращаемое значение — это константа, указывающая операционный тип данных.</span><span class="sxs-lookup"><span data-stu-id="73eec-110">The setting or return value is a constant that indicates an operational or data type.</span></span> <span data-ttu-id="73eec-111">Для объекта **field2** это свойство доступно для чтения и записи до тех пор, пока объект не будет добавлен в коллекцию или другой объект, после которого он доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="73eec-111">For a **Field2** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="73eec-112">В приведенной ниже таблице описаны возможные параметры и возвращаемые значения для объекта **field2** .</span><span class="sxs-lookup"><span data-stu-id="73eec-112">For a **Field2** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73eec-113">Константа</span><span class="sxs-lookup"><span data-stu-id="73eec-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="73eec-114">Описание</span><span class="sxs-lookup"><span data-stu-id="73eec-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73eec-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-116">Большое целое число</span><span class="sxs-lookup"><span data-stu-id="73eec-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73eec-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-118">Binary</span><span class="sxs-lookup"><span data-stu-id="73eec-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73eec-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="73eec-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73eec-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-122">Байт</span><span class="sxs-lookup"><span data-stu-id="73eec-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73eec-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-124">Char</span><span class="sxs-lookup"><span data-stu-id="73eec-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73eec-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-126">Денежный</span><span class="sxs-lookup"><span data-stu-id="73eec-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73eec-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-128">Дата/время</span><span class="sxs-lookup"><span data-stu-id="73eec-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73eec-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-130">Десятичное число</span><span class="sxs-lookup"><span data-stu-id="73eec-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73eec-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-132">Двойное с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="73eec-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73eec-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-134">Float</span><span class="sxs-lookup"><span data-stu-id="73eec-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73eec-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-136">GUID</span><span class="sxs-lookup"><span data-stu-id="73eec-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73eec-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-138">Целое число</span><span class="sxs-lookup"><span data-stu-id="73eec-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73eec-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-140">Long</span><span class="sxs-lookup"><span data-stu-id="73eec-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73eec-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-142">Большой двоичный файл (объект OLE)</span><span class="sxs-lookup"><span data-stu-id="73eec-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73eec-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-144">Memo</span><span class="sxs-lookup"><span data-stu-id="73eec-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73eec-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-146">Numeric</span><span class="sxs-lookup"><span data-stu-id="73eec-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73eec-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-148">Одинарное с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="73eec-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73eec-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-150">Text</span><span class="sxs-lookup"><span data-stu-id="73eec-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73eec-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-152">Time</span><span class="sxs-lookup"><span data-stu-id="73eec-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73eec-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-154">ОтМетка времени</span><span class="sxs-lookup"><span data-stu-id="73eec-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73eec-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="73eec-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="73eec-156">Типа</span><span class="sxs-lookup"><span data-stu-id="73eec-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73eec-157">При добавлении нового объекта **field2**, **параметра**или **Свойства** в коллекцию объекта **index**, **QueryDef**, **Recordset**или **tabledef** возникает ошибка, если базовая база данных не поддерживается. тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="73eec-157">When you append a new **Field2**, **Parameter**, or **Property** object to the collection of an **Index**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

