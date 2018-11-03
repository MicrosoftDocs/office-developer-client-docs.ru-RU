---
title: Свойство QueryDef.Type (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 42bd391cea721176973ce4dd30c9ddc7d15471b8
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937024"
---
# <a name="querydeftype-property-dao"></a><span data-ttu-id="b4599-102">Свойство QueryDef.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="b4599-102">QueryDef.Type property (DAO)</span></span>


<span data-ttu-id="b4599-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4599-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4599-104">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="b4599-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="b4599-105">Только для чтения**целое число**.</span><span class="sxs-lookup"><span data-stu-id="b4599-105">Read-only**Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4599-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4599-106">Syntax</span></span>

<span data-ttu-id="b4599-107">*выражение* . Тип</span><span class="sxs-lookup"><span data-stu-id="b4599-107">*expression* .Type</span></span>

<span data-ttu-id="b4599-108">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="b4599-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4599-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4599-109">Remarks</span></span>

<span data-ttu-id="b4599-110">Для объекта **QueryDef** возможные параметры и возвращаемые значения показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b4599-110">For a **QueryDef** object, the possible settings and return values are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4599-111">Constant</span><span class="sxs-lookup"><span data-stu-id="b4599-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="b4599-112">Тип запроса</span><span class="sxs-lookup"><span data-stu-id="b4599-112">Query type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4599-113"><strong>dbQAction</strong></span><span class="sxs-lookup"><span data-stu-id="b4599-113"><strong>dbQAction</strong></span></span></p></td>
<td><p><span data-ttu-id="b4599-114">Действие</span><span class="sxs-lookup"><span data-stu-id="b4599-114">Action</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4599-115"><strong>dbQAppend</strong></span><span class="sxs-lookup"><span data-stu-id="b4599-115"><strong>dbQAppend</strong></span></span></p></td>
<td><p><span data-ttu-id="b4599-116">Добавление</span><span class="sxs-lookup"><span data-stu-id="b4599-116">Append</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4599-117"><strong>dbQCompound</strong></span><span class="sxs-lookup"><span data-stu-id="b4599-117"><strong>dbQCompound</strong></span></span></p></td>
<td><p><span data-ttu-id="b4599-118">Составные</span><span class="sxs-lookup"><span data-stu-id="b4599-118">Compound</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4599-119"><strong>dbQCrosstab</strong></span><span class="sxs-lookup"><span data-stu-id="b4599-119"><strong>dbQCrosstab</strong></span></span></p></td>
<td><p><span data-ttu-id="b4599-120">Перекрестный</span><span class="sxs-lookup"><span data-stu-id="b4599-120">Crosstab</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4599-121"><strong>dbQDDL</strong></span><span class="sxs-lookup"><span data-stu-id="b4599-121"><strong>dbQDDL</strong></span></span></p></td>
<td><p><span data-ttu-id="b4599-122">Определение данных</span><span class="sxs-lookup"><span data-stu-id="b4599-122">Data-definition</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4599-123"><strong>dbQDelete</strong></span><span class="sxs-lookup"><span data-stu-id="b4599-123"><strong>dbQDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="b4599-124">Delete</span><span class="sxs-lookup"><span data-stu-id="b4599-124">Delete</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4599-125"><strong>dbQMakeTable</strong></span><span class="sxs-lookup"><span data-stu-id="b4599-125"><strong>dbQMakeTable</strong></span></span></p></td>
<td><p><span data-ttu-id="b4599-126">Создание таблицы</span><span class="sxs-lookup"><span data-stu-id="b4599-126">Make-table</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4599-127"><strong>dbQProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="b4599-127"><strong>dbQProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="b4599-128">Процедура (только для рабочих областей технология ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="b4599-128">Procedure (ODBCDirect workspaces only)</span></span></p>

> [!NOTE]
> <span data-ttu-id="b4599-129">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="b4599-129">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="b4599-130">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b4599-130">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4599-131"><strong>dbQSelect</strong></span><span class="sxs-lookup"><span data-stu-id="b4599-131"><strong>dbQSelect</strong></span></span></p></td>
<td><p><span data-ttu-id="b4599-132">Выберите</span><span class="sxs-lookup"><span data-stu-id="b4599-132">Select</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4599-133"><strong>dbQSetOperation</strong></span><span class="sxs-lookup"><span data-stu-id="b4599-133"><strong>dbQSetOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="b4599-134">Объединение</span><span class="sxs-lookup"><span data-stu-id="b4599-134">Union</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4599-135"><strong>dbQSPTBulk</strong></span><span class="sxs-lookup"><span data-stu-id="b4599-135"><strong>dbQSPTBulk</strong></span></span></p></td>
<td><p><span data-ttu-id="b4599-136">Используется с <strong>dbQSQLPassThrough</strong> для указания запроса, который не возвращает записей (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="b4599-136">Used with <strong>dbQSQLPassThrough</strong> to specify a query that doesn't return records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4599-137"><strong>dbQSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="b4599-137"><strong>dbQSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="b4599-138">К серверу (только для рабочих областей Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="b4599-138">Pass-through (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4599-139"><strong>dbQUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="b4599-139"><strong>dbQUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="b4599-140">Update</span><span class="sxs-lookup"><span data-stu-id="b4599-140">Update</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b4599-141">При добавьте новое **[поле](field-object-dao.md)**, **[параметр](parameter-object-dao.md)** или **[свойство](property-object-dao.md)** объекта в коллекцию **[индекса](index-object-dao.md)**, **QueryDef**, **[набора записей](recordset-object-dao.md)** или **[TableDef](tabledef-object-dao.md)** объекта, если основной базы данных не поддерживает возникает ошибка Тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="b4599-141">When you append a new **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)**, or **[Property](property-object-dao.md)** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)**, or **[TableDef](tabledef-object-dao.md)** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

