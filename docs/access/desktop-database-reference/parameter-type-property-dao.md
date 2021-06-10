---
title: Свойство Parameter.Type (DAO)
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
# <a name="parametertype-property-dao"></a><span data-ttu-id="d45a5-102">Свойство Parameter.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="d45a5-102">Parameter.Type property (DAO)</span></span>


<span data-ttu-id="d45a5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d45a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d45a5-104">Задает или возвращает значение, указывающее операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="d45a5-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="d45a5-105">Для чтения и записи, **Integer**.</span><span class="sxs-lookup"><span data-stu-id="d45a5-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d45a5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d45a5-106">Syntax</span></span>

<span data-ttu-id="d45a5-107">*выражение* .Type</span><span class="sxs-lookup"><span data-stu-id="d45a5-107">*expression* .Type</span></span>

<span data-ttu-id="d45a5-108">*выражение* Переменная, представляюная **объект Параметр.**</span><span class="sxs-lookup"><span data-stu-id="d45a5-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d45a5-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="d45a5-109">Remarks</span></span>

<span data-ttu-id="d45a5-110">Параметр или возвращаемое значение является константой, указывающей операционный тип или тип данных.</span><span class="sxs-lookup"><span data-stu-id="d45a5-110">The setting or return value is a constant that indicates an operational or data type.</span></span> <span data-ttu-id="d45a5-111">Для объекта **[Parameter](parameter-object-dao.md)** в рабочей области Microsoft Access свойство только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d45a5-111">For a **[Parameter](parameter-object-dao.md)** object in a Microsoft Access workspace the property is read-only.</span></span>

<span data-ttu-id="d45a5-112">Для объекта **Parameter** возможные параметры и значения возврата описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d45a5-112">For a **Parameter** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d45a5-113">Константа</span><span class="sxs-lookup"><span data-stu-id="d45a5-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="d45a5-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d45a5-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d45a5-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-116">Большое целое</span><span class="sxs-lookup"><span data-stu-id="d45a5-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d45a5-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-118">Двоичный</span><span class="sxs-lookup"><span data-stu-id="d45a5-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d45a5-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-120">Логический</span><span class="sxs-lookup"><span data-stu-id="d45a5-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d45a5-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-122">Байт</span><span class="sxs-lookup"><span data-stu-id="d45a5-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d45a5-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-124">Знак</span><span class="sxs-lookup"><span data-stu-id="d45a5-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d45a5-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-126">Денежный</span><span class="sxs-lookup"><span data-stu-id="d45a5-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d45a5-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-128">Дата и время</span><span class="sxs-lookup"><span data-stu-id="d45a5-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d45a5-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-130">Десятичный</span><span class="sxs-lookup"><span data-stu-id="d45a5-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d45a5-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-132">Двойное</span><span class="sxs-lookup"><span data-stu-id="d45a5-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d45a5-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-134">С плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="d45a5-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d45a5-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-136">Глобальный уникальный идентификатор (GUID)</span><span class="sxs-lookup"><span data-stu-id="d45a5-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d45a5-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-138">Целое</span><span class="sxs-lookup"><span data-stu-id="d45a5-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d45a5-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-140">Длинное целое</span><span class="sxs-lookup"><span data-stu-id="d45a5-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d45a5-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-142">Длинное двоичное (объект OLE)</span><span class="sxs-lookup"><span data-stu-id="d45a5-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d45a5-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-144">Memo</span><span class="sxs-lookup"><span data-stu-id="d45a5-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d45a5-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-146">Числовой</span><span class="sxs-lookup"><span data-stu-id="d45a5-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d45a5-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-148">Одинарное</span><span class="sxs-lookup"><span data-stu-id="d45a5-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d45a5-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-150">Текст</span><span class="sxs-lookup"><span data-stu-id="d45a5-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d45a5-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-152">Время</span><span class="sxs-lookup"><span data-stu-id="d45a5-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d45a5-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-154">Метка времени</span><span class="sxs-lookup"><span data-stu-id="d45a5-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d45a5-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="d45a5-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="d45a5-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="d45a5-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d45a5-157">Когда новый объект **Field**, **Parameter** или **Property** добавляется в коллекцию объектов **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** или **TableDef**, возникает ошибка, если основная база данных не поддерживает тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="d45a5-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

