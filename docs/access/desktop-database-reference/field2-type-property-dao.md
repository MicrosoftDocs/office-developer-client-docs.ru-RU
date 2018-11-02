---
title: Свойство Field2.Type (DAO)
TOCTitle: Type Property
ms:assetid: 057d6ec9-b72c-cee6-005a-6d916e3dda29
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844921(v=office.15)
ms:contentKeyID: 48543032
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 867f964dab4967bf6f545083e1f53a1419e877d1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920419"
---
# <a name="field2type-property-dao"></a><span data-ttu-id="85e8f-102">Свойство Field2.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="85e8f-102">Field2.Type property (DAO)</span></span>


<span data-ttu-id="85e8f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85e8f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85e8f-104">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="85e8f-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="85e8f-105">Чтение и запись **целое число**.</span><span class="sxs-lookup"><span data-stu-id="85e8f-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="85e8f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85e8f-106">Syntax</span></span>

<span data-ttu-id="85e8f-107">*выражение* . Тип</span><span class="sxs-lookup"><span data-stu-id="85e8f-107">*expression* .Type</span></span>

<span data-ttu-id="85e8f-108">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="85e8f-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="85e8f-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="85e8f-109">Remarks</span></span>

<span data-ttu-id="85e8f-110">Параметр или возвращаемое значение — это константа, которая указывает тип действующие или данных.</span><span class="sxs-lookup"><span data-stu-id="85e8f-110">The setting or return value is a constant that indicates an operational or data type.</span></span> <span data-ttu-id="85e8f-111">Для объекта **поле2** это свойство является чтение и запись, пока объект добавляется к коллекции или другой объект, после чего он доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="85e8f-111">For a **Field2** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="85e8f-112">Для объекта **поле2** в следующей таблице описаны возможные параметры и возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="85e8f-112">For a **Field2** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85e8f-113">Константа</span><span class="sxs-lookup"><span data-stu-id="85e8f-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="85e8f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="85e8f-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85e8f-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-116">Длинное целое число</span><span class="sxs-lookup"><span data-stu-id="85e8f-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e8f-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-118">Двоичный</span><span class="sxs-lookup"><span data-stu-id="85e8f-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e8f-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="85e8f-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e8f-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-122">Байт</span><span class="sxs-lookup"><span data-stu-id="85e8f-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e8f-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-124">(Знак)</span><span class="sxs-lookup"><span data-stu-id="85e8f-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e8f-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-126">Денежный</span><span class="sxs-lookup"><span data-stu-id="85e8f-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e8f-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-128">Дата, время</span><span class="sxs-lookup"><span data-stu-id="85e8f-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e8f-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="85e8f-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e8f-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-132">Double</span><span class="sxs-lookup"><span data-stu-id="85e8f-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e8f-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-134">Float</span><span class="sxs-lookup"><span data-stu-id="85e8f-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e8f-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-136">GUID</span><span class="sxs-lookup"><span data-stu-id="85e8f-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e8f-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-138">Целое число</span><span class="sxs-lookup"><span data-stu-id="85e8f-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e8f-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-140">Длинный</span><span class="sxs-lookup"><span data-stu-id="85e8f-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e8f-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-142">Длинные двоичный файл (объект OLE)</span><span class="sxs-lookup"><span data-stu-id="85e8f-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e8f-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-144">Заметка</span><span class="sxs-lookup"><span data-stu-id="85e8f-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e8f-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-146">Числовой</span><span class="sxs-lookup"><span data-stu-id="85e8f-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e8f-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-148">Single</span><span class="sxs-lookup"><span data-stu-id="85e8f-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e8f-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-150">Текст</span><span class="sxs-lookup"><span data-stu-id="85e8f-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e8f-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-152">Time</span><span class="sxs-lookup"><span data-stu-id="85e8f-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e8f-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-154">Метка времени</span><span class="sxs-lookup"><span data-stu-id="85e8f-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e8f-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="85e8f-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="85e8f-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="85e8f-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="85e8f-157">При добавьте новый **поле2**, **параметр**или **свойство** объекта в коллекцию **индекса**, **QueryDef**, **набора записей**или **TableDef** объекта, если основной базы данных не поддерживает возникает ошибка Тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="85e8f-157">When you append a new **Field2**, **Parameter**, or **Property** object to the collection of an **Index**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

