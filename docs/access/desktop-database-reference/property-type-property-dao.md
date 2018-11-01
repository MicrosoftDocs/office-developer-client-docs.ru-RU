---
title: Property.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: bf8258ca-08b5-c4f9-e6d7-114e4300b2ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822796(v=office.15)
ms:contentKeyID: 48547490
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 15a1ac18a504a723948b8f1539c1bf002cf9833a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888148"
---
# <a name="propertytype-property-dao"></a><span data-ttu-id="64ccd-102">Property.Type Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="64ccd-102">Property.Type Property (DAO)</span></span>


<span data-ttu-id="64ccd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64ccd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64ccd-104">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="64ccd-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="64ccd-105">Чтение и запись **целое число**.</span><span class="sxs-lookup"><span data-stu-id="64ccd-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="64ccd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64ccd-106">Syntax</span></span>

<span data-ttu-id="64ccd-107">*выражение* . Тип</span><span class="sxs-lookup"><span data-stu-id="64ccd-107">*expression* .Type</span></span>

<span data-ttu-id="64ccd-108">*выражение* Переменная, которая представляет собой объект- **свойство** .</span><span class="sxs-lookup"><span data-stu-id="64ccd-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="64ccd-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="64ccd-109">Remarks</span></span>

<span data-ttu-id="64ccd-110">Параметр или возвращаемое значение — это константа, которая указывает тип действующие или данных.</span><span class="sxs-lookup"><span data-stu-id="64ccd-110">The setting or return value is a constant that indicates an operational or data type.</span></span> <span data-ttu-id="64ccd-111">Для **[Свойства](property-object-dao.md)** объекта это свойство является чтение и запись, пока объект добавляется к коллекции или другой объект, после чего он доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="64ccd-111">For a **[Property](property-object-dao.md)** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="64ccd-112">Для **Свойства** объекта в следующей таблице описаны возможные параметры и возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="64ccd-112">For a **Property** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64ccd-113">Константа</span><span class="sxs-lookup"><span data-stu-id="64ccd-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="64ccd-114">Описание</span><span class="sxs-lookup"><span data-stu-id="64ccd-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64ccd-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-116">Длинное целое число</span><span class="sxs-lookup"><span data-stu-id="64ccd-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64ccd-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-118">Двоичный</span><span class="sxs-lookup"><span data-stu-id="64ccd-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64ccd-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="64ccd-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64ccd-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-122">Байт</span><span class="sxs-lookup"><span data-stu-id="64ccd-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64ccd-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-124">(Знак)</span><span class="sxs-lookup"><span data-stu-id="64ccd-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64ccd-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-126">Денежный</span><span class="sxs-lookup"><span data-stu-id="64ccd-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64ccd-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-128">Дата, время</span><span class="sxs-lookup"><span data-stu-id="64ccd-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64ccd-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="64ccd-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64ccd-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-132">Double</span><span class="sxs-lookup"><span data-stu-id="64ccd-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64ccd-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-134">Float</span><span class="sxs-lookup"><span data-stu-id="64ccd-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64ccd-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-136">GUID</span><span class="sxs-lookup"><span data-stu-id="64ccd-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64ccd-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-138">Целое число</span><span class="sxs-lookup"><span data-stu-id="64ccd-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64ccd-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-140">Длинный</span><span class="sxs-lookup"><span data-stu-id="64ccd-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64ccd-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-142">Длинные двоичный файл (объект OLE)</span><span class="sxs-lookup"><span data-stu-id="64ccd-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64ccd-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-144">Заметка</span><span class="sxs-lookup"><span data-stu-id="64ccd-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64ccd-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-146">Числовой</span><span class="sxs-lookup"><span data-stu-id="64ccd-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64ccd-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-148">Single</span><span class="sxs-lookup"><span data-stu-id="64ccd-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64ccd-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-150">Текст</span><span class="sxs-lookup"><span data-stu-id="64ccd-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64ccd-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-152">Time</span><span class="sxs-lookup"><span data-stu-id="64ccd-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64ccd-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-154">Метка времени</span><span class="sxs-lookup"><span data-stu-id="64ccd-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64ccd-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="64ccd-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="64ccd-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="64ccd-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="64ccd-157">При добавьте новое **поле**, **параметр**или **свойство** объекта в коллекцию **[индекса](index-object-dao.md)**, **QueryDef**, **набора записей**или **TableDef** объекта, если основной базы данных не поддерживает возникает ошибка Тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="64ccd-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

