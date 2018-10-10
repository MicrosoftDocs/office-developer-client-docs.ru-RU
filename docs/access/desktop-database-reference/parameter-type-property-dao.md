---
title: Parameter.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: 68205cd6-eb45-56a3-593f-e1203472037b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195248(v=office.15)
ms:contentKeyID: 48545377
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a1efe394193b9f8e74c02ecb71758d94fac9259a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480363"
---
# <a name="parametertype-property-dao"></a><span data-ttu-id="a44e0-102">Parameter.Type Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="a44e0-102">Parameter.Type Property (DAO)</span></span>


<span data-ttu-id="a44e0-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a44e0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a44e0-104">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="a44e0-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="a44e0-105">Чтение и запись **целое число**.</span><span class="sxs-lookup"><span data-stu-id="a44e0-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a44e0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a44e0-106">Syntax</span></span>

<span data-ttu-id="a44e0-107">*выражение* . Тип</span><span class="sxs-lookup"><span data-stu-id="a44e0-107">*expression* .Type</span></span>

<span data-ttu-id="a44e0-108">*выражение* Переменная, которая представляет собой объект- **параметр** .</span><span class="sxs-lookup"><span data-stu-id="a44e0-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a44e0-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="a44e0-109">Remarks</span></span>

<span data-ttu-id="a44e0-110">Параметр или возвращаемое значение — это константа, которая указывает тип действующие или данных.</span><span class="sxs-lookup"><span data-stu-id="a44e0-110">The setting or return value is a constant that indicates an operational or data type.</span></span> <span data-ttu-id="a44e0-111">Для объекта **[параметра](parameter-object-dao.md)** в рабочей области Microsoft Access свойство только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a44e0-111">For a **[Parameter](parameter-object-dao.md)** object in a Microsoft Access workspace the property is read-only.</span></span>

<span data-ttu-id="a44e0-112">Для **параметра** объекта в следующей таблице описаны возможные параметры и возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="a44e0-112">For a **Parameter** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a44e0-113">Константа</span><span class="sxs-lookup"><span data-stu-id="a44e0-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="a44e0-114">Описание</span><span class="sxs-lookup"><span data-stu-id="a44e0-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a44e0-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-116">Длинное целое число</span><span class="sxs-lookup"><span data-stu-id="a44e0-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e0-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-118">Двоичный</span><span class="sxs-lookup"><span data-stu-id="a44e0-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e0-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="a44e0-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e0-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-122">Байт</span><span class="sxs-lookup"><span data-stu-id="a44e0-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e0-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-124">(Знак)</span><span class="sxs-lookup"><span data-stu-id="a44e0-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e0-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-126">Денежный</span><span class="sxs-lookup"><span data-stu-id="a44e0-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e0-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-128">Дата, время</span><span class="sxs-lookup"><span data-stu-id="a44e0-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e0-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="a44e0-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e0-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-132">Double</span><span class="sxs-lookup"><span data-stu-id="a44e0-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e0-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-134">Float</span><span class="sxs-lookup"><span data-stu-id="a44e0-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e0-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-136">GUID</span><span class="sxs-lookup"><span data-stu-id="a44e0-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e0-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-138">Целое число</span><span class="sxs-lookup"><span data-stu-id="a44e0-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e0-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-140">Длинный</span><span class="sxs-lookup"><span data-stu-id="a44e0-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e0-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-142">Длинные двоичный файл (объект OLE)</span><span class="sxs-lookup"><span data-stu-id="a44e0-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e0-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-144">Заметка</span><span class="sxs-lookup"><span data-stu-id="a44e0-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e0-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-146">Числовой</span><span class="sxs-lookup"><span data-stu-id="a44e0-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e0-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-148">Single</span><span class="sxs-lookup"><span data-stu-id="a44e0-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e0-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-150">Текст</span><span class="sxs-lookup"><span data-stu-id="a44e0-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e0-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-152">Time</span><span class="sxs-lookup"><span data-stu-id="a44e0-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a44e0-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-154">Метка времени</span><span class="sxs-lookup"><span data-stu-id="a44e0-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a44e0-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a44e0-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a44e0-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="a44e0-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a44e0-157">При добавьте новое **поле**, **параметр**или **свойство** объекта в коллекцию **[индекса](index-object-dao.md)**, **QueryDef**, **набора записей**или **TableDef** объекта, если основной базы данных не поддерживает возникает ошибка Тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="a44e0-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

