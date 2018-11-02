---
title: Свойство Parameter.Type (DAO)
TOCTitle: Type Property
ms:assetid: 68205cd6-eb45-56a3-593f-e1203472037b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195248(v=office.15)
ms:contentKeyID: 48545377
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 294d61ba964958d7933a68919df940cb7501ec0d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927034"
---
# <a name="parametertype-property-dao"></a><span data-ttu-id="65499-102">Свойство Parameter.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="65499-102">Parameter.Type property (DAO)</span></span>


<span data-ttu-id="65499-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="65499-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="65499-104">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="65499-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="65499-105">Чтение и запись **целое число**.</span><span class="sxs-lookup"><span data-stu-id="65499-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="65499-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65499-106">Syntax</span></span>

<span data-ttu-id="65499-107">*выражение* . Тип</span><span class="sxs-lookup"><span data-stu-id="65499-107">*expression* .Type</span></span>

<span data-ttu-id="65499-108">*выражение* Переменная, которая представляет собой объект- **параметр** .</span><span class="sxs-lookup"><span data-stu-id="65499-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="65499-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="65499-109">Remarks</span></span>

<span data-ttu-id="65499-110">Параметр или возвращаемое значение — это константа, которая указывает тип действующие или данных.</span><span class="sxs-lookup"><span data-stu-id="65499-110">The setting or return value is a constant that indicates an operational or data type.</span></span> <span data-ttu-id="65499-111">Для объекта **[параметра](parameter-object-dao.md)** в рабочей области Microsoft Access свойство только для чтения.</span><span class="sxs-lookup"><span data-stu-id="65499-111">For a **[Parameter](parameter-object-dao.md)** object in a Microsoft Access workspace the property is read-only.</span></span>

<span data-ttu-id="65499-112">Для **параметра** объекта в следующей таблице описаны возможные параметры и возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="65499-112">For a **Parameter** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65499-113">Константа</span><span class="sxs-lookup"><span data-stu-id="65499-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="65499-114">Описание</span><span class="sxs-lookup"><span data-stu-id="65499-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65499-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="65499-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-116">Длинное целое число</span><span class="sxs-lookup"><span data-stu-id="65499-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65499-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="65499-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-118">Двоичный</span><span class="sxs-lookup"><span data-stu-id="65499-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65499-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="65499-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="65499-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65499-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="65499-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-122">Байт</span><span class="sxs-lookup"><span data-stu-id="65499-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65499-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="65499-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-124">(Знак)</span><span class="sxs-lookup"><span data-stu-id="65499-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65499-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="65499-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-126">Денежный</span><span class="sxs-lookup"><span data-stu-id="65499-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65499-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="65499-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-128">Дата, время</span><span class="sxs-lookup"><span data-stu-id="65499-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65499-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="65499-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="65499-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65499-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="65499-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-132">Double</span><span class="sxs-lookup"><span data-stu-id="65499-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65499-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="65499-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-134">Float</span><span class="sxs-lookup"><span data-stu-id="65499-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65499-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="65499-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-136">GUID</span><span class="sxs-lookup"><span data-stu-id="65499-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65499-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="65499-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-138">Целое число</span><span class="sxs-lookup"><span data-stu-id="65499-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65499-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="65499-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-140">Длинный</span><span class="sxs-lookup"><span data-stu-id="65499-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65499-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="65499-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-142">Длинные двоичный файл (объект OLE)</span><span class="sxs-lookup"><span data-stu-id="65499-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65499-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="65499-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-144">Заметка</span><span class="sxs-lookup"><span data-stu-id="65499-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65499-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="65499-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-146">Числовой</span><span class="sxs-lookup"><span data-stu-id="65499-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65499-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="65499-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-148">Single</span><span class="sxs-lookup"><span data-stu-id="65499-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65499-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="65499-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-150">Текст</span><span class="sxs-lookup"><span data-stu-id="65499-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65499-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="65499-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-152">Time</span><span class="sxs-lookup"><span data-stu-id="65499-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65499-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="65499-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-154">Метка времени</span><span class="sxs-lookup"><span data-stu-id="65499-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65499-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="65499-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="65499-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="65499-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="65499-157">При добавьте новое **поле**, **параметр**или **свойство** объекта в коллекцию **[индекса](index-object-dao.md)**, **QueryDef**, **набора записей**или **TableDef** объекта, если основной базы данных не поддерживает возникает ошибка Тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="65499-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

