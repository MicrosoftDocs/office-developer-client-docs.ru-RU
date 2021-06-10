---
title: Свойство QueryDef.Type (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cb8856194d0b2ed14577bdc275adeb50ebdde212
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300947"
---
# <a name="querydeftype-property-dao"></a><span data-ttu-id="8a6b5-102">Свойство QueryDef.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="8a6b5-102">QueryDef.Type property (DAO)</span></span>


<span data-ttu-id="8a6b5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a6b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8a6b5-104">Задает или возвращает значение, указывающее операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="8a6b5-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="8a6b5-105">Только для чтения **в integer**.</span><span class="sxs-lookup"><span data-stu-id="8a6b5-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a6b5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a6b5-106">Syntax</span></span>

<span data-ttu-id="8a6b5-107">*выражение* .Type</span><span class="sxs-lookup"><span data-stu-id="8a6b5-107">*expression* .Type</span></span>

<span data-ttu-id="8a6b5-108">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="8a6b5-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a6b5-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="8a6b5-109">Remarks</span></span>

<span data-ttu-id="8a6b5-110">Для объекта **QueryDef** возможные параметры и значения возврата показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8a6b5-110">For a **QueryDef** object, the possible settings and return values are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a6b5-111">Константа</span><span class="sxs-lookup"><span data-stu-id="8a6b5-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="8a6b5-112">Тип запроса</span><span class="sxs-lookup"><span data-stu-id="8a6b5-112">Query type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a6b5-113"><strong>dbQAction</strong></span><span class="sxs-lookup"><span data-stu-id="8a6b5-113"><strong>dbQAction</strong></span></span></p></td>
<td><p><span data-ttu-id="8a6b5-114">Action</span><span class="sxs-lookup"><span data-stu-id="8a6b5-114">Action</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a6b5-115"><strong>dbQAppend</strong></span><span class="sxs-lookup"><span data-stu-id="8a6b5-115"><strong>dbQAppend</strong></span></span></p></td>
<td><p><span data-ttu-id="8a6b5-116">Приложение</span><span class="sxs-lookup"><span data-stu-id="8a6b5-116">Append</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a6b5-117"><strong>dbQCompound</strong></span><span class="sxs-lookup"><span data-stu-id="8a6b5-117"><strong>dbQCompound</strong></span></span></p></td>
<td><p><span data-ttu-id="8a6b5-118">Compound</span><span class="sxs-lookup"><span data-stu-id="8a6b5-118">Compound</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a6b5-119"><strong>dbQCrosstab</strong></span><span class="sxs-lookup"><span data-stu-id="8a6b5-119"><strong>dbQCrosstab</strong></span></span></p></td>
<td><p><span data-ttu-id="8a6b5-120">Crosstab</span><span class="sxs-lookup"><span data-stu-id="8a6b5-120">Crosstab</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a6b5-121"><strong>dbQDDL</strong></span><span class="sxs-lookup"><span data-stu-id="8a6b5-121"><strong>dbQDDL</strong></span></span></p></td>
<td><p><span data-ttu-id="8a6b5-122">Определение данных</span><span class="sxs-lookup"><span data-stu-id="8a6b5-122">Data-definition</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a6b5-123"><strong>dbQDelete</strong></span><span class="sxs-lookup"><span data-stu-id="8a6b5-123"><strong>dbQDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="8a6b5-124">Удалить</span><span class="sxs-lookup"><span data-stu-id="8a6b5-124">Delete</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a6b5-125"><strong>dbQMakeTable</strong></span><span class="sxs-lookup"><span data-stu-id="8a6b5-125"><strong>dbQMakeTable</strong></span></span></p></td>
<td><p><span data-ttu-id="8a6b5-126">Make-table</span><span class="sxs-lookup"><span data-stu-id="8a6b5-126">Make-table</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a6b5-127"><strong>dbQProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="8a6b5-127"><strong>dbQProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="8a6b5-128">Процедура (только в рабочей области ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="8a6b5-128">Procedure (ODBCDirect workspaces only)</span></span></p><p><span data-ttu-id="8a6b5-129"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="8a6b5-129"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="8a6b5-130">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8a6b5-130">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a6b5-131"><strong>dbQSelect</strong></span><span class="sxs-lookup"><span data-stu-id="8a6b5-131"><strong>dbQSelect</strong></span></span></p></td>
<td><p><span data-ttu-id="8a6b5-132">Выбор</span><span class="sxs-lookup"><span data-stu-id="8a6b5-132">Select</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a6b5-133"><strong>dbQSetOperation</strong></span><span class="sxs-lookup"><span data-stu-id="8a6b5-133"><strong>dbQSetOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="8a6b5-134">Union</span><span class="sxs-lookup"><span data-stu-id="8a6b5-134">Union</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a6b5-135"><strong>dbQSPTBulk</strong></span><span class="sxs-lookup"><span data-stu-id="8a6b5-135"><strong>dbQSPTBulk</strong></span></span></p></td>
<td><p><span data-ttu-id="8a6b5-136">Используется в <strong>dbQSQQLPassThrough</strong> для указания запроса, который не возвращает записи (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8a6b5-136">Used with <strong>dbQSQLPassThrough</strong> to specify a query that doesn't return records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a6b5-137"><strong>dbQSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="8a6b5-137"><strong>dbQSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="8a6b5-138">Pass-through (только для рабочей области Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="8a6b5-138">Pass-through (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a6b5-139"><strong>dbQUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="8a6b5-139"><strong>dbQUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="8a6b5-140">Update</span><span class="sxs-lookup"><span data-stu-id="8a6b5-140">Update</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8a6b5-141">При приложении нового объекта **[Field,](field-object-dao.md)** **[Parameter](parameter-object-dao.md)** или **[Property](property-object-dao.md)** **[](index-object-dao.md)** к коллекции объекта **Index, QueryDef,** **[Recordset](recordset-object-dao.md)** или **[TableDef](tabledef-object-dao.md)** возникает ошибка, если базовая база данных не поддерживает тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="8a6b5-141">When you append a new **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)**, or **[Property](property-object-dao.md)** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)**, or **[TableDef](tabledef-object-dao.md)** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

