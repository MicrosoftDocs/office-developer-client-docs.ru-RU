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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306057"
---
# <a name="willmove-and-movecomplete-events-ado"></a><span data-ttu-id="1bff5-102">События WillMove и MoveComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="1bff5-102">WillMove and MoveComplete events (ADO)</span></span>

<span data-ttu-id="1bff5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1bff5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1bff5-104">Событие **WillMove** вызвано, прежде чем ожидающая операция изменяет текущую позицию в [наборе записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="1bff5-104">The **WillMove** event is called before a pending operation changes the current position in the [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="1bff5-105">Событие **MoveComplete** вызвано после изменения текущей позиции **в наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="1bff5-105">The **MoveComplete** event is called after the current position in the **Recordset** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bff5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1bff5-106">Syntax</span></span>

<span data-ttu-id="1bff5-107">WillMove *adReason*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="1bff5-107">WillMove *adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="1bff5-108">MoveComplete *adReason,* *pError,* *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="1bff5-108">MoveComplete *adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="1bff5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1bff5-109">Parameters</span></span>

|<span data-ttu-id="1bff5-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="1bff5-110">Parameter</span></span>|<span data-ttu-id="1bff5-111">Описание</span><span class="sxs-lookup"><span data-stu-id="1bff5-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1bff5-112">*adReason*</span><span class="sxs-lookup"><span data-stu-id="1bff5-112">*adReason*</span></span> |<span data-ttu-id="1bff5-113">Значение [EventReasonEnum,](eventreasonenum.md) которое указывает причину этого события.</span><span class="sxs-lookup"><span data-stu-id="1bff5-113">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event.</span></span> <span data-ttu-id="1bff5-114">Его значение может быть **adRsnMoveFirst,** **adRsnMoveLast,** **adRsnMoveNext,** **adRsnMovePrevious,** **adRsnMove** или **adRsnRequery**.</span><span class="sxs-lookup"><span data-stu-id="1bff5-114">Its value can be **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, or **adRsnRequery**.</span></span>|
|<span data-ttu-id="1bff5-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="1bff5-115">*pError*</span></span> |<span data-ttu-id="1bff5-116">Объект [Error.](error-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="1bff5-116">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="1bff5-117">В ней описывается ошибка, которая произошла, если *значением adStatus* является **adStatusErrorsOccurred;** в противном случае он не установлен.</span><span class="sxs-lookup"><span data-stu-id="1bff5-117">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="1bff5-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="1bff5-118">*adStatus*</span></span> |<span data-ttu-id="1bff5-119">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="1bff5-119">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="1bff5-120">При **вызывается WillMove,** этот параметр задан как **adStatusOK,** если операция, которая вызвала событие, была успешной.</span><span class="sxs-lookup"><span data-stu-id="1bff5-120">When **WillMove** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="1bff5-121">Если это событие не может запросить отмену ожидающей операции, ему задается **adStatusCantDeny.**</span><span class="sxs-lookup"><span data-stu-id="1bff5-121">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="1bff5-122">При **вызывается MoveComplete,** этот параметр задан как **adStatusOK,** если операция, которая привела к событию, была успешной, или **adStatusErrorsOccurred,** если операция не удалась.</span><span class="sxs-lookup"><span data-stu-id="1bff5-122">When **MoveComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span> <br/><br/><span data-ttu-id="1bff5-123">Перед возвратом **WillMove** установите для этого параметра параметр **adStatusCancel** запрос отмены ожидающих операций или установите для этого параметра adStatusUnwantedEvent, чтобы запретить последующие нотации.</span><span class="sxs-lookup"><span data-stu-id="1bff5-123">Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span> <br/><br/><span data-ttu-id="1bff5-124">Перед **возвращением MoveComplete** установите для этого параметра **параметр adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="1bff5-124">Before **MoveComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="1bff5-125">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="1bff5-125">*pRecordset*</span></span> |<span data-ttu-id="1bff5-126">Объект [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="1bff5-126">A [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="1bff5-127">Набор **записей,** для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="1bff5-127">The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1bff5-128">Заметки</span><span class="sxs-lookup"><span data-stu-id="1bff5-128">Remarks</span></span>

<span data-ttu-id="1bff5-129">Событие **WillMove** или **MoveComplete** может произойти из-за следующих операций **Recordset:**</span><span class="sxs-lookup"><span data-stu-id="1bff5-129">A **WillMove** or **MoveComplete** event may occur due to the following **Recordset** operations:</span></span>

- [<span data-ttu-id="1bff5-130">Open</span><span class="sxs-lookup"><span data-stu-id="1bff5-130">Open</span></span>](open-method-ado-recordset.md)
- [<span data-ttu-id="1bff5-131">Move</span><span class="sxs-lookup"><span data-stu-id="1bff5-131">Move</span></span>](move-method-ado.md)
- [<span data-ttu-id="1bff5-132">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="1bff5-132">MoveFirst</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="1bff5-133">MoveLast</span><span class="sxs-lookup"><span data-stu-id="1bff5-133">MoveLast</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="1bff5-134">MoveNext</span><span class="sxs-lookup"><span data-stu-id="1bff5-134">MoveNext</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [<span data-ttu-id="1bff5-135">MovePrevious</span><span class="sxs-lookup"><span data-stu-id="1bff5-135">MovePrevious</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="1bff5-136">AddNew</span><span class="sxs-lookup"><span data-stu-id="1bff5-136">AddNew</span></span>](addnew-method-ado.md)
- [<span data-ttu-id="1bff5-137">Requery</span><span class="sxs-lookup"><span data-stu-id="1bff5-137">Requery</span></span>](requery-method-ado.md)

<span data-ttu-id="1bff5-138">Эти события могут возникать из-за следующих свойств:</span><span class="sxs-lookup"><span data-stu-id="1bff5-138">These events may occur because of the following properties:</span></span>

- [<span data-ttu-id="1bff5-139">Фильтр</span><span class="sxs-lookup"><span data-stu-id="1bff5-139">Filter</span></span>](filter-property-ado.md)
- [<span data-ttu-id="1bff5-140">Индекс</span><span class="sxs-lookup"><span data-stu-id="1bff5-140">Index</span></span>](index-property-ado.md)
- [<span data-ttu-id="1bff5-141">Bookmark</span><span class="sxs-lookup"><span data-stu-id="1bff5-141">Bookmark</span></span>](bookmark-property-ado.md)
- [<span data-ttu-id="1bff5-142">AbsolutePage</span><span class="sxs-lookup"><span data-stu-id="1bff5-142">AbsolutePage</span></span>](absolutepage-property-ado.md)
- [<span data-ttu-id="1bff5-143">AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="1bff5-143">AbsolutePosition</span></span>](absoluteposition-property-ado.md)

<span data-ttu-id="1bff5-144">Эти события также происходят, если для родительского **recordset** подключены события **Recordset** и родительский **набор записей.**</span><span class="sxs-lookup"><span data-stu-id="1bff5-144">These events also occur if a child **Recordset** has **Recordset** events connected and the parent **Recordset** is moved.</span></span>

<span data-ttu-id="1bff5-145">Необходимо установить для параметра *adStatus* значение **adStatusUnwantedEvent** для каждого возможного значения *adReason,* чтобы полностью остановить уведомление о событии, которое включает параметр *adReason.*</span><span class="sxs-lookup"><span data-stu-id="1bff5-145">You must set the *adStatus* parameter to **adStatusUnwantedEvent** for each possible *adReason* value in order to completely stop event notification for any event that includes an *adReason* parameter.</span></span>

