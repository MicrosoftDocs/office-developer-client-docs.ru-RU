---
title: Свойство Parameter. Type (DAO)
TOCTitle: Type Property
ms:assetid: 68205cd6-eb45-56a3-593f-e1203472037b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195248(v=office.15)
ms:contentKeyID: 48545377
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 208d0a5097b8473fef60b94f972f2c8579150fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288023"
---
# <a name="parametertype-property-dao"></a><span data-ttu-id="b5494-102">Свойство Parameter. Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="b5494-102">Parameter.Type property (DAO)</span></span>


<span data-ttu-id="b5494-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5494-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5494-104">Задает или возвращает значение, которое указывает операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="b5494-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="b5494-105">Чтение и запись **целоГо числа**.</span><span class="sxs-lookup"><span data-stu-id="b5494-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5494-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5494-106">Syntax</span></span>

<span data-ttu-id="b5494-107">*Expression* . Тип</span><span class="sxs-lookup"><span data-stu-id="b5494-107">*expression* .Type</span></span>

<span data-ttu-id="b5494-108">*Expression (выражение* ) Переменная, представляющая объект **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="b5494-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5494-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="b5494-109">Remarks</span></span>

<span data-ttu-id="b5494-110">Параметр или возвращаемое значение — это константа, указывающая операционный тип данных.</span><span class="sxs-lookup"><span data-stu-id="b5494-110">The setting or return value is a constant that indicates an operational or data type.</span></span> <span data-ttu-id="b5494-111">Для объекта **[Parameter](parameter-object-dao.md)** в рабочей области Microsoft Access свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b5494-111">For a **[Parameter](parameter-object-dao.md)** object in a Microsoft Access workspace the property is read-only.</span></span>

<span data-ttu-id="b5494-112">В приведенной ниже таблице описаны возможные параметры и возвращаемые значения для объекта **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="b5494-112">For a **Parameter** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5494-113">Константа</span><span class="sxs-lookup"><span data-stu-id="b5494-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="b5494-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b5494-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5494-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-116">Большое целое число</span><span class="sxs-lookup"><span data-stu-id="b5494-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5494-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-118">Binary</span><span class="sxs-lookup"><span data-stu-id="b5494-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5494-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="b5494-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5494-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-122">Байт</span><span class="sxs-lookup"><span data-stu-id="b5494-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5494-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-124">Char</span><span class="sxs-lookup"><span data-stu-id="b5494-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5494-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-126">Денежный</span><span class="sxs-lookup"><span data-stu-id="b5494-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5494-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-128">Дата/время</span><span class="sxs-lookup"><span data-stu-id="b5494-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5494-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-130">Десятичное число</span><span class="sxs-lookup"><span data-stu-id="b5494-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5494-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-132">Двойное с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="b5494-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5494-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-134">Float</span><span class="sxs-lookup"><span data-stu-id="b5494-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5494-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-136">GUID</span><span class="sxs-lookup"><span data-stu-id="b5494-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5494-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-138">Целое число</span><span class="sxs-lookup"><span data-stu-id="b5494-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5494-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-140">Long</span><span class="sxs-lookup"><span data-stu-id="b5494-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5494-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-142">Большой двоичный файл (объект OLE)</span><span class="sxs-lookup"><span data-stu-id="b5494-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5494-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-144">Memo</span><span class="sxs-lookup"><span data-stu-id="b5494-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5494-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-146">Numeric</span><span class="sxs-lookup"><span data-stu-id="b5494-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5494-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-148">Одинарное с плавающей точкой</span><span class="sxs-lookup"><span data-stu-id="b5494-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5494-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-150">Text</span><span class="sxs-lookup"><span data-stu-id="b5494-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5494-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-152">Time</span><span class="sxs-lookup"><span data-stu-id="b5494-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5494-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-154">ОтМетка времени</span><span class="sxs-lookup"><span data-stu-id="b5494-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5494-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="b5494-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="b5494-156">Типа</span><span class="sxs-lookup"><span data-stu-id="b5494-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b5494-157">При добавлении нового **поля**, **параметра**или объекта **Свойства** в коллекцию объекта **[index](index-object-dao.md)**, **QueryDef**, **Recordset**или **tabledef** возникает ошибка, если базовая база данных не поддерживается. тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="b5494-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

