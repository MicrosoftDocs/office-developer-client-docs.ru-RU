---
title: Метод Recordset.MoveLast (DAO)
TOCTitle: MoveLast method
ms:assetid: fc0f7a33-1f55-9f5b-b00d-1b81f49b1c3e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837192(v=office.15)
ms:contentKeyID: 48548881
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 22c028601024df79f5ca75c8845decae31935dc3
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998779"
---
# <a name="recordsetmovelast-method-dao"></a><span data-ttu-id="85e81-102">Метод Recordset.MoveLast (DAO)</span><span class="sxs-lookup"><span data-stu-id="85e81-102">Recordset.MoveLast method (DAO)</span></span>

<span data-ttu-id="85e81-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85e81-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85e81-104">Переход к последней записи в указанный объект **набора записей** и сделать эту запись текущей записи.</span><span class="sxs-lookup"><span data-stu-id="85e81-104">Moves to the last record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="85e81-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85e81-105">Syntax</span></span>

<span data-ttu-id="85e81-106">*выражение* . MoveLast (***Параметры***)</span><span class="sxs-lookup"><span data-stu-id="85e81-106">*expression* .MoveLast(***Options***)</span></span>

<span data-ttu-id="85e81-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="85e81-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="85e81-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="85e81-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85e81-109">Имя</span><span class="sxs-lookup"><span data-stu-id="85e81-109">Name</span></span></p></th>
<th><p><span data-ttu-id="85e81-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="85e81-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="85e81-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="85e81-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="85e81-112">Описание</span><span class="sxs-lookup"><span data-stu-id="85e81-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85e81-113"><em>Варианты</em></span><span class="sxs-lookup"><span data-stu-id="85e81-113"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="85e81-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="85e81-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="85e81-115"><strong>Длинный</strong></span><span class="sxs-lookup"><span data-stu-id="85e81-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="85e81-116">Задайте значение <strong>dbRunAsync</strong> для rune вызов <strong>MoveLast</strong> асинхронно.</span><span class="sxs-lookup"><span data-stu-id="85e81-116">Set to <strong>dbRunAsync</strong> to rune the call to <strong>MoveLast</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="85e81-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="85e81-117">Remarks</span></span>

<span data-ttu-id="85e81-118">Используйте методы **перемещения** для перемещения между записями без применения условие.</span><span class="sxs-lookup"><span data-stu-id="85e81-118">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="85e81-119">При изменении текущей записи убедитесь, что использование метода **Update** для сохранения изменений перед переходом к другой записи.</span><span class="sxs-lookup"><span data-stu-id="85e81-119">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record.</span></span> <span data-ttu-id="85e81-120">При перемещении к другой записи без обновления, изменения не сохраняются без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="85e81-120">If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="85e81-121">При открытии **набора записей**первой записи текущего и **BOF** свойство имеет **значение False**.</span><span class="sxs-lookup"><span data-stu-id="85e81-121">When you open a **Recordset**, the first record is current and the **BOF** property is **False**.</span></span> <span data-ttu-id="85e81-122">**Набор записей** не содержит записей, свойство **BOF** имеет **значение True**, и нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="85e81-122">If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="85e81-123">Если первой или последней записи текущего при использовании **MoveFirst** или **MoveLast**, не изменяется при текущей записи.</span><span class="sxs-lookup"><span data-stu-id="85e81-123">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="85e81-124">Если записей относится к таблице типа **записей** (только для рабочих областей Microsoft Access), перемещение за текущий индекс.</span><span class="sxs-lookup"><span data-stu-id="85e81-124">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="85e81-125">Индекс текущей можно задать с помощью свойства **индекса** .</span><span class="sxs-lookup"><span data-stu-id="85e81-125">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="85e81-126">Если не установить текущий индекс, порядок возвращаемых записей не определено.</span><span class="sxs-lookup"><span data-stu-id="85e81-126">If you don't set the current index, the order of returned records is undefined.</span></span>

> [!NOTE]
> <span data-ttu-id="85e81-127">Метод **MoveLast** полностью заполнить или моментальный снимок добавляющий **набора записей** для предоставления текущее число записей в **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="85e81-127">You can use the **MoveLast** method to fully populate a dynaset- or snapshot-type **Recordset** to provide the current number of records in the **Recordset**.</span></span> <span data-ttu-id="85e81-128">Тем не менее если вы используете **MoveLast** таким образом, может снизить производительность приложения.</span><span class="sxs-lookup"><span data-stu-id="85e81-128">However, if you use **MoveLast** in this way, you can slow down your application's performance.</span></span> <span data-ttu-id="85e81-129">**MoveLast** следует использовать только для получения счетчика записей, если это действительно необходимо получить точное число записей на открываемые **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="85e81-129">You should only use **MoveLast** to get a record count if it is absolutely necessary to obtain an accurate record count on a newly opened **Recordset**.</span></span> 
> 
> <span data-ttu-id="85e81-130">При использовании константу **dbRunAsync** с **MoveLast**асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="85e81-130">If you use the **dbRunAsync** constant with **MoveLast**, the method call is asynchronous.</span></span> <span data-ttu-id="85e81-131">Чтобы определить, когда **записей** полностью заполнен, и можно использовать метод **Cancel** для завершения выполнения асинхронного вызова метода **MoveLast** можно использовать свойство **StillExecuting** .</span><span class="sxs-lookup"><span data-stu-id="85e81-131">You can use the **StillExecuting** property to determine when the **Recordset** is fully populated, and you can use the **Cancel** method to terminate execution of the asynchronous **MoveLast** method call.</span></span>

<span data-ttu-id="85e81-132">Нельзя использовать методы **MoveFirst** **MoveLast**и **MovePrevious** для прямого — только – тип объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="85e81-132">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="85e81-133">Для смещения позиции текущего записей в объекте **набора записей** определенного количества записей вперед или назад, используйте метод **Move** .</span><span class="sxs-lookup"><span data-stu-id="85e81-133">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

