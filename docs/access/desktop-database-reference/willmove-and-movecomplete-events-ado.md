---
title: События WillMove и MoveComplete (ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e663e18a13803097d490e0e315d139e6e15400da
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705962"
---
# <a name="willmove-and-movecomplete-events-ado"></a><span data-ttu-id="a3a3c-102">События WillMove и MoveComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="a3a3c-102">WillMove and MoveComplete events (ADO)</span></span>

<span data-ttu-id="a3a3c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3a3c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3a3c-104">Событие **WillMove** вызывается перед ожидающие операции изменяет текущую позицию в наборе [записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a3a3c-104">The **WillMove** event is called before a pending operation changes the current position in the [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="a3a3c-105">Событие **MoveComplete** вызывается после текущей позиции в изменения **записей** .</span><span class="sxs-lookup"><span data-stu-id="a3a3c-105">The **MoveComplete** event is called after the current position in the **Recordset** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3a3c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3a3c-106">Syntax</span></span>

<span data-ttu-id="a3a3c-107">WillMove*adReason*, *adStatus* *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="a3a3c-107">WillMove*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="a3a3c-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="a3a3c-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="a3a3c-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="a3a3c-109">Parameters</span></span>

|<span data-ttu-id="a3a3c-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="a3a3c-110">Parameter</span></span>|<span data-ttu-id="a3a3c-111">Описание</span><span class="sxs-lookup"><span data-stu-id="a3a3c-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a3a3c-112">*adReason*</span><span class="sxs-lookup"><span data-stu-id="a3a3c-112">*adReason*</span></span> |<span data-ttu-id="a3a3c-113">Значение [EventReasonEnum](eventreasonenum.md) , указывает причину это событие.</span><span class="sxs-lookup"><span data-stu-id="a3a3c-113">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event.</span></span> <span data-ttu-id="a3a3c-114">Его значение может быть **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**или **adRsnRequery**.</span><span class="sxs-lookup"><span data-stu-id="a3a3c-114">Its value can be **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, or **adRsnRequery**.</span></span>|
|<span data-ttu-id="a3a3c-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="a3a3c-115">*pError*</span></span> |<span data-ttu-id="a3a3c-116">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a3a3c-116">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="a3a3c-117">Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="a3a3c-117">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="a3a3c-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="a3a3c-118">*adStatus*</span></span> |<span data-ttu-id="a3a3c-119">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="a3a3c-119">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="a3a3c-120">При вызове **WillMove** этот параметр имеет значение **adStatusOK** , если операция, которая вызвала событие прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="a3a3c-120">When **WillMove** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="a3a3c-121">Если это событие не могут запрашивать отмену ожидающие операции перейдут в **adStatusCantDeny** .</span><span class="sxs-lookup"><span data-stu-id="a3a3c-121">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="a3a3c-122">При вызове **MoveComplete** этот параметр имеет значение **adStatusOK** в случае успешного операцию, которая вызвала событие или **adStatusErrorsOccurred** , если операция завершилась неудачно.</span><span class="sxs-lookup"><span data-stu-id="a3a3c-122">When **MoveComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span> <br/><br/><span data-ttu-id="a3a3c-123">Прежде чем возвращает **WillMove** , присвойте этому параметру значение **adStatusCancel** для запроса отмены ожидающие операции или присвойте этому параметру значение adStatusUnwantedEvent, чтобы запретить последующие notications.</span><span class="sxs-lookup"><span data-stu-id="a3a3c-123">Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span> <br/><br/><span data-ttu-id="a3a3c-124">Прежде чем возвращает **MoveComplete** , присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="a3a3c-124">Before **MoveComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="a3a3c-125">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="a3a3c-125">*pRecordset*</span></span> |<span data-ttu-id="a3a3c-126">Объект [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a3a3c-126">A [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="a3a3c-127">**Набор записей** , для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="a3a3c-127">The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a3a3c-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="a3a3c-128">Remarks</span></span>

<span data-ttu-id="a3a3c-129">Событие **WillMove** или **MoveComplete** могут быть вызваны следующие операции **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="a3a3c-129">A **WillMove** or **MoveComplete** event may occur due to the following **Recordset** operations:</span></span>

- [<span data-ttu-id="a3a3c-130">Open</span><span class="sxs-lookup"><span data-stu-id="a3a3c-130">Open</span></span>](open-method-ado-recordset.md)
- [<span data-ttu-id="a3a3c-131">Move</span><span class="sxs-lookup"><span data-stu-id="a3a3c-131">Move</span></span>](move-method-ado.md)
- [<span data-ttu-id="a3a3c-132">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="a3a3c-132">MoveFirst</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="a3a3c-133">MoveLast</span><span class="sxs-lookup"><span data-stu-id="a3a3c-133">MoveLast</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="a3a3c-134">MoveNext</span><span class="sxs-lookup"><span data-stu-id="a3a3c-134">MoveNext</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [<span data-ttu-id="a3a3c-135">MovePrevious</span><span class="sxs-lookup"><span data-stu-id="a3a3c-135">MovePrevious</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="a3a3c-136">AddNew</span><span class="sxs-lookup"><span data-stu-id="a3a3c-136">AddNew</span></span>](addnew-method-ado.md)
- [<span data-ttu-id="a3a3c-137">Requery</span><span class="sxs-lookup"><span data-stu-id="a3a3c-137">Requery</span></span>](requery-method-ado.md)

<span data-ttu-id="a3a3c-138">Эти события могут возникнуть из-за следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="a3a3c-138">These events may occur because of the following properties:</span></span>

- [<span data-ttu-id="a3a3c-139">Фильтр</span><span class="sxs-lookup"><span data-stu-id="a3a3c-139">Filter</span></span>](filter-property-ado.md)
- [<span data-ttu-id="a3a3c-140">Index</span><span class="sxs-lookup"><span data-stu-id="a3a3c-140">Index</span></span>](index-property-ado.md)
- [<span data-ttu-id="a3a3c-141">Bookmark</span><span class="sxs-lookup"><span data-stu-id="a3a3c-141">Bookmark</span></span>](bookmark-property-ado.md)
- [<span data-ttu-id="a3a3c-142">AbsolutePage</span><span class="sxs-lookup"><span data-stu-id="a3a3c-142">AbsolutePage</span></span>](absolutepage-property-ado.md)
- [<span data-ttu-id="a3a3c-143">AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="a3a3c-143">AbsolutePosition</span></span>](absoluteposition-property-ado.md)

<span data-ttu-id="a3a3c-144">Эти события также возникают при дочерних **записей** имеет **записей** событий подключенных и родительский перемещены **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="a3a3c-144">These events also occur if a child **Recordset** has **Recordset** events connected and the parent **Recordset** is moved.</span></span>

<span data-ttu-id="a3a3c-145">Параметр *adStatus* должен значение **adStatusUnwantedEvent** для каждого *adReason* возможные значения для полностью остановите уведомления о событиях для любого события, которое включает параметр *adReason* .</span><span class="sxs-lookup"><span data-stu-id="a3a3c-145">You must set the *adStatus* parameter to **adStatusUnwantedEvent** for each possible *adReason* value in order to completely stop event notification for any event that includes an *adReason* parameter.</span></span>

