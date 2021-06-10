---
title: Метод Recordset.MoveLast (DAO)
TOCTitle: MoveLast method
ms:assetid: fc0f7a33-1f55-9f5b-b00d-1b81f49b1c3e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837192(v=office.15)
ms:contentKeyID: 48548881
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 79799742499e163a43d51a2d8553adcadf27b36d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284534"
---
# <a name="recordsetmovelast-method-dao"></a><span data-ttu-id="9be67-102">Метод Recordset.MoveLast (DAO)</span><span class="sxs-lookup"><span data-stu-id="9be67-102">Recordset.MoveLast method (DAO)</span></span>

<span data-ttu-id="9be67-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9be67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9be67-104">Выполняет перемещение к последней записи в указанном объекте **Recordset** и делает запись текущей.</span><span class="sxs-lookup"><span data-stu-id="9be67-104">Moves to the last record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9be67-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9be67-105">Syntax</span></span>

<span data-ttu-id="9be67-106">*выражения* . MoveLast ***(Параметры)***</span><span class="sxs-lookup"><span data-stu-id="9be67-106">*expression* .MoveLast(***Options***)</span></span>

<span data-ttu-id="9be67-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9be67-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="9be67-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9be67-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9be67-109">Имя</span><span class="sxs-lookup"><span data-stu-id="9be67-109">Name</span></span></p></th>
<th><p><span data-ttu-id="9be67-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="9be67-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="9be67-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9be67-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="9be67-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9be67-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9be67-113"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="9be67-113"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="9be67-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="9be67-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="9be67-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="9be67-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="9be67-116">Установите <strong>dbRunAsync, чтобы</strong> выполнить вызов <strong>в MoveLast</strong> асинхронно.</span><span class="sxs-lookup"><span data-stu-id="9be67-116">Set to <strong>dbRunAsync</strong> to rune the call to <strong>MoveLast</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9be67-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9be67-117">Remarks</span></span>

<span data-ttu-id="9be67-118">Используйте методы **Move**, чтобы перейти от записи к записи, не применяя условие.</span><span class="sxs-lookup"><span data-stu-id="9be67-118">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="9be67-119">Если вы редактируете текущую запись, убедитесь, что вы используете метод **Update**, чтобы сохранить изменения, перед переходом к другой записи.</span><span class="sxs-lookup"><span data-stu-id="9be67-119">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record.</span></span> <span data-ttu-id="9be67-120">Если перейти к другой записи без обновления, изменения будут потеряны без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="9be67-120">If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="9be67-121">Когда вы открываете **Recordset**, первую запись является текущей, а свойство **BOF** имеет значение **False**.</span><span class="sxs-lookup"><span data-stu-id="9be67-121">When you open a **Recordset**, the first record is current and the **BOF** property is **False**.</span></span> <span data-ttu-id="9be67-122">Если **Recordset** не содержит записей, свойство **BOF** имеет значение **True**, а текущая запись отсутствует.</span><span class="sxs-lookup"><span data-stu-id="9be67-122">If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="9be67-123">Если первая или последняя запись уже является текущей при использовании **MoveFirst** или **MoveLast**, текущая запись не меняется.</span><span class="sxs-lookup"><span data-stu-id="9be67-123">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="9be67-124">Если recordset указывает на табличный тип объекта **Recordset** (только для рабочих областей Microsoft Access), перемещение отвечает текущему индексу.</span><span class="sxs-lookup"><span data-stu-id="9be67-124">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="9be67-125">Вы можете задать текущий индекс с помощью свойства **Index**.</span><span class="sxs-lookup"><span data-stu-id="9be67-125">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="9be67-126">Если не задать текущей индекс, порядок возвращаемых записей будет не определен.</span><span class="sxs-lookup"><span data-stu-id="9be67-126">If you don't set the current index, the order of returned records is undefined.</span></span>

> [!NOTE]
> <span data-ttu-id="9be67-127">С помощью метода **MoveLast** можно полностью заполнить набор записей dynaset или snapshot-type, чтобы предоставить текущее число записей **в Наборе записей.** </span><span class="sxs-lookup"><span data-stu-id="9be67-127">You can use the **MoveLast** method to fully populate a dynaset- or snapshot-type **Recordset** to provide the current number of records in the **Recordset**.</span></span> <span data-ttu-id="9be67-128">Однако, если вы используете **MoveLast** таким образом, вы можете замедлить производительность приложения.</span><span class="sxs-lookup"><span data-stu-id="9be67-128">However, if you use **MoveLast** in this way, you can slow down your application's performance.</span></span> <span data-ttu-id="9be67-129">Чтобы получить количество записей, необходимо использовать **MoveLast** только в том случае, если для получения точного подсчета записей на недавно открытом Наборе записей необходимо получить **точное количество записей.**</span><span class="sxs-lookup"><span data-stu-id="9be67-129">You should only use **MoveLast** to get a record count if it is absolutely necessary to obtain an accurate record count on a newly opened **Recordset**.</span></span> 
> 
> <span data-ttu-id="9be67-130">Если вы используете констант **dbRunAsync** с **MoveLast,** вызов метода является асинхронным.</span><span class="sxs-lookup"><span data-stu-id="9be67-130">If you use the **dbRunAsync** constant with **MoveLast**, the method call is asynchronous.</span></span> <span data-ttu-id="9be67-131">Свойство **StillExecuting** можно использовать для  определения полного заполнения наборов записей,  а для прекращения выполнения асинхронного вызова **метода MoveLast** можно использовать метод Cancel.</span><span class="sxs-lookup"><span data-stu-id="9be67-131">You can use the **StillExecuting** property to determine when the **Recordset** is fully populated, and you can use the **Cancel** method to terminate execution of the asynchronous **MoveLast** method call.</span></span>

<span data-ttu-id="9be67-132">Вы не можете использовать методы **MoveFirst**, **MoveLast** и **MovePrevious** для объекта **Recordset** однонаправленного типа.</span><span class="sxs-lookup"><span data-stu-id="9be67-132">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="9be67-133">Чтобы переместить положение текущей записи в объекте **Recordset** на определенное количество записей вперед или назад, используйте метод **Move**.</span><span class="sxs-lookup"><span data-stu-id="9be67-133">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

