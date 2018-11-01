---
title: Recordset2.MoveLast Method (DAO)
TOCTitle: MoveLast Method
ms:assetid: 32717786-c59c-ec22-666b-fc78e4265c5a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192306(v=office.15)
ms:contentKeyID: 48544079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e48e4816be8342165dba17d7ab4d478d53962114
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874596"
---
# <a name="recordset2movelast-method-dao"></a><span data-ttu-id="05072-102">Recordset2.MoveLast Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="05072-102">Recordset2.MoveLast Method (DAO)</span></span>


<span data-ttu-id="05072-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05072-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05072-104">Переход к последней записи в указанный объект **набора записей** и сделать эту запись текущей записи.</span><span class="sxs-lookup"><span data-stu-id="05072-104">Moves to the last record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="05072-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05072-105">Syntax</span></span>

<span data-ttu-id="05072-106">*выражение* . MoveLast (***Параметры***)</span><span class="sxs-lookup"><span data-stu-id="05072-106">*expression* .MoveLast(***Options***)</span></span>

<span data-ttu-id="05072-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="05072-107">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="05072-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="05072-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05072-109">Имя</span><span class="sxs-lookup"><span data-stu-id="05072-109">Name</span></span></p></th>
<th><p><span data-ttu-id="05072-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="05072-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="05072-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="05072-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="05072-112">Описание</span><span class="sxs-lookup"><span data-stu-id="05072-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05072-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="05072-113">Options</span></span></p></td>
<td><p><span data-ttu-id="05072-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="05072-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="05072-115"><strong>Длинный</strong></span><span class="sxs-lookup"><span data-stu-id="05072-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="05072-116">Задайте значение <strong>dbRunAsync</strong> для rune вызов <strong>MoveLast</strong> асинхронно.</span><span class="sxs-lookup"><span data-stu-id="05072-116">Set to <strong>dbRunAsync</strong> to rune the call to <strong>MoveLast</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="05072-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="05072-117">Remarks</span></span>

<span data-ttu-id="05072-118">Используйте методы **перемещения** для перемещения между записями без применения условие.</span><span class="sxs-lookup"><span data-stu-id="05072-118">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="05072-119">При изменении текущей записи убедитесь, что использование метода **Update** для сохранения изменений перед переходом к другой записи.</span><span class="sxs-lookup"><span data-stu-id="05072-119">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record.</span></span> <span data-ttu-id="05072-120">При перемещении к другой записи без обновления, изменения не сохраняются без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="05072-120">If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="05072-121">При открытии **набора записей**первой записи текущего и **BOF** свойство имеет **значение False**.</span><span class="sxs-lookup"><span data-stu-id="05072-121">When you open a **Recordset**, the first record is current and the **BOF** property is **False**.</span></span> <span data-ttu-id="05072-122">**Набор записей** не содержит записей, свойство **BOF** имеет **значение True**, и нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="05072-122">If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="05072-123">Если первой или последней записи текущего при использовании **MoveFirst** или **MoveLast**, не изменяется при текущей записи.</span><span class="sxs-lookup"><span data-stu-id="05072-123">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="05072-124">Если записей относится к таблице типа **записей** (только для рабочих областей Microsoft Access), перемещение за текущий индекс.</span><span class="sxs-lookup"><span data-stu-id="05072-124">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="05072-125">Индекс текущей можно задать с помощью свойства **индекса** .</span><span class="sxs-lookup"><span data-stu-id="05072-125">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="05072-126">Если не установить текущий индекс, порядок возвращаемых записей не определено.</span><span class="sxs-lookup"><span data-stu-id="05072-126">If you don't set the current index, the order of returned records is undefined.</span></span>


> [!NOTE]
> <P><span data-ttu-id="05072-127">Метод <STRONG>MoveLast</STRONG> полностью заполнить или моментальный снимок добавляющий <STRONG>набора записей</STRONG> для предоставления текущее число записей в <STRONG>набора записей</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="05072-127">You can use the <STRONG>MoveLast</STRONG> method to fully populate a dynaset- or snapshot-type <STRONG>Recordset</STRONG> to provide the current number of records in the <STRONG>Recordset</STRONG>.</span></span> <span data-ttu-id="05072-128">Тем не менее если вы используете <STRONG>MoveLast</STRONG> таким образом, может снизить производительность приложения.</span><span class="sxs-lookup"><span data-stu-id="05072-128">However, if you use <STRONG>MoveLast</STRONG> in this way, you can slow down your application's performance.</span></span> <span data-ttu-id="05072-129"><STRONG>MoveLast</STRONG> следует использовать только для получения счетчика записей, если это действительно необходимо получить точное число записей на открываемые <STRONG>набора записей</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="05072-129">You should only use <STRONG>MoveLast</STRONG> to get a record count if it is absolutely necessary to obtain an accurate record count on a newly opened <STRONG>Recordset</STRONG>.</span></span> <span data-ttu-id="05072-130">При использовании константу <STRONG>dbRunAsync</STRONG> с <STRONG>MoveLast</STRONG>асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="05072-130">If you use the <STRONG>dbRunAsync</STRONG> constant with <STRONG>MoveLast</STRONG>, the method call is asynchronous.</span></span> <span data-ttu-id="05072-131">Чтобы определить, когда <STRONG>записей</STRONG> полностью заполнен, и можно использовать метод <STRONG>Cancel</STRONG> для завершения выполнения асинхронного вызова метода <STRONG>MoveLast</STRONG> можно использовать свойство <STRONG>StillExecuting</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="05072-131">You can use the <STRONG>StillExecuting</STRONG> property to determine when the <STRONG>Recordset</STRONG> is fully populated, and you can use the <STRONG>Cancel</STRONG> method to terminate execution of the asynchronous <STRONG>MoveLast</STRONG> method call.</span></span></P>



<span data-ttu-id="05072-132">Нельзя использовать методы **MoveFirst** **MoveLast**и **MovePrevious** для прямого — только – тип объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="05072-132">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="05072-133">Для смещения позиции текущего записей в объекте **набора записей** определенного количества записей вперед или назад, используйте метод **Move** .</span><span class="sxs-lookup"><span data-stu-id="05072-133">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

