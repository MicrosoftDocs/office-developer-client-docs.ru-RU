---
title: Свойство Field.Type (DAO)
TOCTitle: Type Property
ms:assetid: 1295ca40-78c1-bdd0-d407-e1b5be8adfd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845405(v=office.15)
ms:contentKeyID: 48543345
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3f532897ca20dda7b8ca82d831398e20cfa6b9da
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923156"
---
# <a name="fieldtype-property-dao"></a><span data-ttu-id="2d635-102">Свойство Field.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="2d635-102">Field.Type property (DAO)</span></span>


<span data-ttu-id="2d635-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d635-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d635-104">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="2d635-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="2d635-105">Чтение и запись **целое число**.</span><span class="sxs-lookup"><span data-stu-id="2d635-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d635-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d635-106">Syntax</span></span>

<span data-ttu-id="2d635-107">*выражение* . Тип</span><span class="sxs-lookup"><span data-stu-id="2d635-107">*expression* .Type</span></span>

<span data-ttu-id="2d635-108">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="2d635-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d635-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="2d635-109">Remarks</span></span>

<span data-ttu-id="2d635-110">Параметр или возвращаемое значение — это константа, которая указывает тип действующие или данных.</span><span class="sxs-lookup"><span data-stu-id="2d635-110">The setting or return value is a constant that indicates an operational or data type.</span></span> <span data-ttu-id="2d635-111">Для объекта **поля** это свойство является чтение и запись, пока объект добавляется к коллекции или другой объект, после чего он доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2d635-111">For a **Field** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="2d635-112">Для объекта **поля** в следующей таблице описаны возможные параметры и возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="2d635-112">For a **Field** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d635-113">Константа</span><span class="sxs-lookup"><span data-stu-id="2d635-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="2d635-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2d635-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d635-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-116">Длинное целое число</span><span class="sxs-lookup"><span data-stu-id="2d635-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d635-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-118">Двоичный</span><span class="sxs-lookup"><span data-stu-id="2d635-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d635-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="2d635-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d635-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-122">Байт</span><span class="sxs-lookup"><span data-stu-id="2d635-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d635-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-124">(Знак)</span><span class="sxs-lookup"><span data-stu-id="2d635-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d635-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-126">Денежный</span><span class="sxs-lookup"><span data-stu-id="2d635-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d635-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-128">Дата, время</span><span class="sxs-lookup"><span data-stu-id="2d635-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d635-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="2d635-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d635-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-132">Double</span><span class="sxs-lookup"><span data-stu-id="2d635-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d635-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-134">Float</span><span class="sxs-lookup"><span data-stu-id="2d635-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d635-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-136">GUID</span><span class="sxs-lookup"><span data-stu-id="2d635-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d635-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-138">Целое число</span><span class="sxs-lookup"><span data-stu-id="2d635-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d635-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-140">Длинный</span><span class="sxs-lookup"><span data-stu-id="2d635-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d635-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-142">Длинные двоичный файл (объект OLE)</span><span class="sxs-lookup"><span data-stu-id="2d635-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d635-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-144">Заметка</span><span class="sxs-lookup"><span data-stu-id="2d635-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d635-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-146">Числовой</span><span class="sxs-lookup"><span data-stu-id="2d635-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d635-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-148">Single</span><span class="sxs-lookup"><span data-stu-id="2d635-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d635-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-150">Текст</span><span class="sxs-lookup"><span data-stu-id="2d635-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d635-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-152">Time</span><span class="sxs-lookup"><span data-stu-id="2d635-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d635-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-154">Метка времени</span><span class="sxs-lookup"><span data-stu-id="2d635-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d635-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="2d635-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2d635-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="2d635-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2d635-157">При добавьте новое **поле**, **параметр**или **свойство** объекта в коллекцию **[индекса](index-object-dao.md)**, **QueryDef**, **набора записей**или **TableDef** объекта, если основной базы данных не поддерживает возникает ошибка Тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="2d635-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

