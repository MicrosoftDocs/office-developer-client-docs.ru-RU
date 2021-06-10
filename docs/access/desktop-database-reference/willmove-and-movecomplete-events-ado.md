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
# <a name="willmove-and-movecomplete-events-ado"></a><span data-ttu-id="12271-102">События WillMove и MoveComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="12271-102">WillMove and MoveComplete events (ADO)</span></span>

<span data-ttu-id="12271-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="12271-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="12271-104">Событие **WillMove вызвано** до того, как ожидающая операция изменяет текущую позицию в [Наборе записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="12271-104">The **WillMove** event is called before a pending operation changes the current position in the [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="12271-105">Событие **MoveComplete** вызвано после изменения текущей позиции **в Recordset.**</span><span class="sxs-lookup"><span data-stu-id="12271-105">The **MoveComplete** event is called after the current position in the **Recordset** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="12271-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12271-106">Syntax</span></span>

<span data-ttu-id="12271-107">WillMove *adReason*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="12271-107">WillMove *adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="12271-108">MoveComplete *adReason*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="12271-108">MoveComplete *adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="12271-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="12271-109">Parameters</span></span>

|<span data-ttu-id="12271-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="12271-110">Parameter</span></span>|<span data-ttu-id="12271-111">Описание</span><span class="sxs-lookup"><span data-stu-id="12271-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="12271-112">*adReason*</span><span class="sxs-lookup"><span data-stu-id="12271-112">*adReason*</span></span> |<span data-ttu-id="12271-113">Значение [EventReasonEnum,](eventreasonenum.md) которое указывает причину этого события.</span><span class="sxs-lookup"><span data-stu-id="12271-113">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event.</span></span> <span data-ttu-id="12271-114">Его значение может быть **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, или **adRsnRequery**.</span><span class="sxs-lookup"><span data-stu-id="12271-114">Its value can be **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, or **adRsnRequery**.</span></span>|
|<span data-ttu-id="12271-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="12271-115">*pError*</span></span> |<span data-ttu-id="12271-116">Объект [Ошибки.](error-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="12271-116">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="12271-117">Он описывает ошибку, которая произошла, если значение *adStatus* **является adStatusErrorsOccurred;** в противном случае она не установлена.</span><span class="sxs-lookup"><span data-stu-id="12271-117">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="12271-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="12271-118">*adStatus*</span></span> |<span data-ttu-id="12271-119">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="12271-119">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="12271-120">Когда **вызывается WillMove,** этот параметр задан **adStatusOK,** если операция, которая вызвала событие, была успешной.</span><span class="sxs-lookup"><span data-stu-id="12271-120">When **WillMove** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="12271-121">Оно устанавливается **для adStatusCantDeny,** если это событие не может запросить отмену ожидающей операции.</span><span class="sxs-lookup"><span data-stu-id="12271-121">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="12271-122">Когда **вызывается MoveComplete,** этот параметр задан **adStatusOK,** если операция, вызвавла событие, была успешной, или **adStatusErrorsOccurred,** если операция не удалась.</span><span class="sxs-lookup"><span data-stu-id="12271-122">When **MoveComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span> <br/><br/><span data-ttu-id="12271-123">Перед возвращением **WillMove** установите этот параметр **adStatusCancel** для запроса отмены ожидаемой операции или установите этот параметр adStatusUnwantedEvent для предотвращения последующих замений.</span><span class="sxs-lookup"><span data-stu-id="12271-123">Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span> <br/><br/><span data-ttu-id="12271-124">Перед **возвращением MoveComplete** установите этот параметр **adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="12271-124">Before **MoveComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="12271-125">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="12271-125">*pRecordset*</span></span> |<span data-ttu-id="12271-126">Объект [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="12271-126">A [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="12271-127">**Набор записей,** для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="12271-127">The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="12271-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="12271-128">Remarks</span></span>

<span data-ttu-id="12271-129">Событие **WillMove или** **MoveComplete** может произойти из-за следующих операций **Recordset:**</span><span class="sxs-lookup"><span data-stu-id="12271-129">A **WillMove** or **MoveComplete** event may occur due to the following **Recordset** operations:</span></span>

- [<span data-ttu-id="12271-130">Open</span><span class="sxs-lookup"><span data-stu-id="12271-130">Open</span></span>](open-method-ado-recordset.md)
- [<span data-ttu-id="12271-131">Move</span><span class="sxs-lookup"><span data-stu-id="12271-131">Move</span></span>](move-method-ado.md)
- [<span data-ttu-id="12271-132">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="12271-132">MoveFirst</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="12271-133">MoveLast</span><span class="sxs-lookup"><span data-stu-id="12271-133">MoveLast</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="12271-134">MoveNext</span><span class="sxs-lookup"><span data-stu-id="12271-134">MoveNext</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [<span data-ttu-id="12271-135">MovePrevious</span><span class="sxs-lookup"><span data-stu-id="12271-135">MovePrevious</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="12271-136">AddNew</span><span class="sxs-lookup"><span data-stu-id="12271-136">AddNew</span></span>](addnew-method-ado.md)
- [<span data-ttu-id="12271-137">Requery</span><span class="sxs-lookup"><span data-stu-id="12271-137">Requery</span></span>](requery-method-ado.md)

<span data-ttu-id="12271-138">Эти события могут возникать из-за следующих свойств:</span><span class="sxs-lookup"><span data-stu-id="12271-138">These events may occur because of the following properties:</span></span>

- [<span data-ttu-id="12271-139">Filter</span><span class="sxs-lookup"><span data-stu-id="12271-139">Filter</span></span>](filter-property-ado.md)
- [<span data-ttu-id="12271-140">Index</span><span class="sxs-lookup"><span data-stu-id="12271-140">Index</span></span>](index-property-ado.md)
- [<span data-ttu-id="12271-141">Bookmark</span><span class="sxs-lookup"><span data-stu-id="12271-141">Bookmark</span></span>](bookmark-property-ado.md)
- [<span data-ttu-id="12271-142">AbsolutePage</span><span class="sxs-lookup"><span data-stu-id="12271-142">AbsolutePage</span></span>](absolutepage-property-ado.md)
- [<span data-ttu-id="12271-143">AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="12271-143">AbsolutePosition</span></span>](absoluteposition-property-ado.md)

<span data-ttu-id="12271-144">Эти события также происходят, если у ребенка **Recordset** подключены события **Recordset** и родительский **набор записей** перемещается.</span><span class="sxs-lookup"><span data-stu-id="12271-144">These events also occur if a child **Recordset** has **Recordset** events connected and the parent **Recordset** is moved.</span></span>

<span data-ttu-id="12271-145">Параметр *adStatus* необходимо задать **adStatusUnwantedEvent** для каждого возможного значения *adReason,* чтобы полностью остановить уведомление о событии для любого события, которое включает параметр *adReason.*</span><span class="sxs-lookup"><span data-stu-id="12271-145">You must set the *adStatus* parameter to **adStatusUnwantedEvent** for each possible *adReason* value in order to completely stop event notification for any event that includes an *adReason* parameter.</span></span>

