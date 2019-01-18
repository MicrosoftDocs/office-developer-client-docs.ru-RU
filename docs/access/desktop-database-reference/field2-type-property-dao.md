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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699788"
---
# <a name="field2type-property-dao"></a><span data-ttu-id="4f7dd-102">Свойство Field2.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="4f7dd-102">Field2.Type property (DAO)</span></span>


<span data-ttu-id="4f7dd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f7dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4f7dd-104">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="4f7dd-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="4f7dd-105">Чтение и запись **целое число**.</span><span class="sxs-lookup"><span data-stu-id="4f7dd-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f7dd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f7dd-106">Syntax</span></span>

<span data-ttu-id="4f7dd-107">*выражение* . Тип</span><span class="sxs-lookup"><span data-stu-id="4f7dd-107">*expression* .Type</span></span>

<span data-ttu-id="4f7dd-108">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="4f7dd-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f7dd-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="4f7dd-109">Remarks</span></span>

<span data-ttu-id="4f7dd-110">Параметр или возвращаемое значение — это константа, которая указывает тип действующие или данных.</span><span class="sxs-lookup"><span data-stu-id="4f7dd-110">The setting or return value is a constant that indicates an operational or data type.</span></span> <span data-ttu-id="4f7dd-111">Для объекта **поле2** это свойство является чтение и запись, пока объект добавляется к коллекции или другой объект, после чего он доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4f7dd-111">For a **Field2** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="4f7dd-112">Для объекта **поле2** в следующей таблице описаны возможные параметры и возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="4f7dd-112">For a **Field2** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f7dd-113">Константа</span><span class="sxs-lookup"><span data-stu-id="4f7dd-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="4f7dd-114">Описание</span><span class="sxs-lookup"><span data-stu-id="4f7dd-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f7dd-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-116">Длинное целое число</span><span class="sxs-lookup"><span data-stu-id="4f7dd-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f7dd-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-118">Binary</span><span class="sxs-lookup"><span data-stu-id="4f7dd-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f7dd-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-120">Логический</span><span class="sxs-lookup"><span data-stu-id="4f7dd-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f7dd-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-122">Байт</span><span class="sxs-lookup"><span data-stu-id="4f7dd-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f7dd-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-124">Char</span><span class="sxs-lookup"><span data-stu-id="4f7dd-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f7dd-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-126">Денежный</span><span class="sxs-lookup"><span data-stu-id="4f7dd-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f7dd-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-128">Дата, время</span><span class="sxs-lookup"><span data-stu-id="4f7dd-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f7dd-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="4f7dd-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f7dd-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-132">Double</span><span class="sxs-lookup"><span data-stu-id="4f7dd-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f7dd-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-134">Float</span><span class="sxs-lookup"><span data-stu-id="4f7dd-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f7dd-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-136">Идентификатор GUID</span><span class="sxs-lookup"><span data-stu-id="4f7dd-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f7dd-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-138">Целое число</span><span class="sxs-lookup"><span data-stu-id="4f7dd-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f7dd-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-140">Long</span><span class="sxs-lookup"><span data-stu-id="4f7dd-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f7dd-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-142">Длинные двоичный файл (объект OLE)</span><span class="sxs-lookup"><span data-stu-id="4f7dd-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f7dd-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-144">Заметка</span><span class="sxs-lookup"><span data-stu-id="4f7dd-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f7dd-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-146">Числовой</span><span class="sxs-lookup"><span data-stu-id="4f7dd-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f7dd-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-148">Single</span><span class="sxs-lookup"><span data-stu-id="4f7dd-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f7dd-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-150">Текст</span><span class="sxs-lookup"><span data-stu-id="4f7dd-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f7dd-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-152">Time</span><span class="sxs-lookup"><span data-stu-id="4f7dd-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f7dd-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-154">Метка времени</span><span class="sxs-lookup"><span data-stu-id="4f7dd-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f7dd-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="4f7dd-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="4f7dd-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="4f7dd-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4f7dd-157">При добавьте новый **поле2**, **параметр**или **свойство** объекта в коллекцию **индекса**, **QueryDef**, **набора записей**или **TableDef** объекта, если основной базы данных не поддерживает возникает ошибка Тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="4f7dd-157">When you append a new **Field2**, **Parameter**, or **Property** object to the collection of an **Index**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

