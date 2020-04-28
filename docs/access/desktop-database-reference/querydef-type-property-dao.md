---
title: Свойство QueryDef. Type (DAO)
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
# <a name="querydeftype-property-dao"></a><span data-ttu-id="9a38d-102">Свойство QueryDef. Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="9a38d-102">QueryDef.Type property (DAO)</span></span>


<span data-ttu-id="9a38d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a38d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a38d-104">Задает или возвращает значение, указывающее операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="9a38d-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="9a38d-105">**Целое число**, доступное только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9a38d-105">Read-only**Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a38d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a38d-106">Syntax</span></span>

<span data-ttu-id="9a38d-107">*выражение* .Type</span><span class="sxs-lookup"><span data-stu-id="9a38d-107">*expression* .Type</span></span>

<span data-ttu-id="9a38d-108">*выражение*: переменная, представляющая объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="9a38d-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a38d-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a38d-109">Remarks</span></span>

<span data-ttu-id="9a38d-110">В приведенной ниже таблице представлены возможные параметры и возвращаемые значения для объекта **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="9a38d-110">For a **QueryDef** object, the possible settings and return values are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a38d-111">Константа</span><span class="sxs-lookup"><span data-stu-id="9a38d-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="9a38d-112">Тип запроса</span><span class="sxs-lookup"><span data-stu-id="9a38d-112">Query type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a38d-113"><strong>дбкактион</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-113"><strong>dbQAction</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-114">Action</span><span class="sxs-lookup"><span data-stu-id="9a38d-114">Action</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a38d-115"><strong>дбкаппенд</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-115"><strong>dbQAppend</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-116">Error</span><span class="sxs-lookup"><span data-stu-id="9a38d-116">Append</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a38d-117"><strong>дбккомпаунд</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-117"><strong>dbQCompound</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-118">Состав</span><span class="sxs-lookup"><span data-stu-id="9a38d-118">Compound</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a38d-119"><strong>дбккросстаб</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-119"><strong>dbQCrosstab</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-120">Перекрестный</span><span class="sxs-lookup"><span data-stu-id="9a38d-120">Crosstab</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a38d-121"><strong>дбкддл</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-121"><strong>dbQDDL</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-122">Определение данных</span><span class="sxs-lookup"><span data-stu-id="9a38d-122">Data-definition</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a38d-123"><strong>дбкделете</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-123"><strong>dbQDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-124">Удаление</span><span class="sxs-lookup"><span data-stu-id="9a38d-124">Delete</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a38d-125"><strong>дбкмакетабле</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-125"><strong>dbQMakeTable</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-126">Создание таблицы</span><span class="sxs-lookup"><span data-stu-id="9a38d-126">Make-table</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a38d-127"><strong>дбкпроцедуре</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-127"><strong>dbQProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-128">Процедура (только для рабочих областей ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="9a38d-128">Procedure (ODBCDirect workspaces only)</span></span></p><p><span data-ttu-id="9a38d-129"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="9a38d-129"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="9a38d-130">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9a38d-130">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a38d-131"><strong>дбкселект</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-131"><strong>dbQSelect</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-132">Выбор</span><span class="sxs-lookup"><span data-stu-id="9a38d-132">Select</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a38d-133"><strong>дбксетоператион</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-133"><strong>dbQSetOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-134">Union</span><span class="sxs-lookup"><span data-stu-id="9a38d-134">Union</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a38d-135"><strong>дбксптбулк</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-135"><strong>dbQSPTBulk</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-136">Используется с <strong>дбксклпасссраугх</strong> , чтобы указать запрос, который не возвращает записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9a38d-136">Used with <strong>dbQSQLPassThrough</strong> to specify a query that doesn't return records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a38d-137"><strong>дбксклпасссраугх</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-137"><strong>dbQSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-138">Сквозная передача (только для рабочих областей Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="9a38d-138">Pass-through (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a38d-139"><strong>дбкупдате</strong></span><span class="sxs-lookup"><span data-stu-id="9a38d-139"><strong>dbQUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="9a38d-140">Update</span><span class="sxs-lookup"><span data-stu-id="9a38d-140">Update</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9a38d-141">При добавлении нового **[поля](field-object-dao.md)**, **[параметра](parameter-object-dao.md)** или объекта **[Свойства](property-object-dao.md)** в коллекцию объекта **[index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)** или **[tabledef](tabledef-object-dao.md)** возникает ошибка, если базовая база данных не поддерживает тип данных, указанный для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="9a38d-141">When you append a new **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)**, or **[Property](property-object-dao.md)** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)**, or **[TableDef](tabledef-object-dao.md)** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

