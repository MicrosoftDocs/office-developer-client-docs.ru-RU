---
title: События события WillMove и MoveComplete (ADO)
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
# <a name="willmove-and-movecomplete-events-ado"></a><span data-ttu-id="1ebfe-102">События события WillMove и MoveComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="1ebfe-102">WillMove and MoveComplete events (ADO)</span></span>

<span data-ttu-id="1ebfe-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ebfe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ebfe-104">Событие **события WillMove** вызывается до того, как ожидающая операция меняет текущую позицию в [наборе записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1ebfe-104">The **WillMove** event is called before a pending operation changes the current position in the [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="1ebfe-105">Событие **MoveComplete** вызывается после изменения текущей позиции в **наборе записей** .</span><span class="sxs-lookup"><span data-stu-id="1ebfe-105">The **MoveComplete** event is called after the current position in the **Recordset** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ebfe-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ebfe-106">Syntax</span></span>

<span data-ttu-id="1ebfe-107">События WillMove*адреасон*, *адстатус*, *pRecordset* пред</span><span class="sxs-lookup"><span data-stu-id="1ebfe-107">WillMove*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="1ebfe-108">MoveComplete*адреасон*, *перрор*, *адстатус*, *pRecordset* пред</span><span class="sxs-lookup"><span data-stu-id="1ebfe-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="1ebfe-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ebfe-109">Parameters</span></span>

|<span data-ttu-id="1ebfe-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="1ebfe-110">Parameter</span></span>|<span data-ttu-id="1ebfe-111">Описание</span><span class="sxs-lookup"><span data-stu-id="1ebfe-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1ebfe-112">*адреасон*</span><span class="sxs-lookup"><span data-stu-id="1ebfe-112">*adReason*</span></span> |<span data-ttu-id="1ebfe-113">Значение [евентреасоненум](eventreasonenum.md) , указывающее причину этого события.</span><span class="sxs-lookup"><span data-stu-id="1ebfe-113">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event.</span></span> <span data-ttu-id="1ebfe-114">Возможные значения: **адрснмовефирст**, **адрснмовеласт**, **адрснмовенекст**, **адрснмовепревиаус**, **адрснмове**или **адрснрекуери**.</span><span class="sxs-lookup"><span data-stu-id="1ebfe-114">Its value can be **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, or **adRsnRequery**.</span></span>|
|<span data-ttu-id="1ebfe-115">*перрор*</span><span class="sxs-lookup"><span data-stu-id="1ebfe-115">*pError*</span></span> |<span data-ttu-id="1ebfe-116">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1ebfe-116">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="1ebfe-117">В нем описывается ошибка, которая возникла, если значение *адстатус* равно **адстатусеррорсоккурред**; в противном случае он не задается.</span><span class="sxs-lookup"><span data-stu-id="1ebfe-117">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="1ebfe-118">*адстатус*</span><span class="sxs-lookup"><span data-stu-id="1ebfe-118">*adStatus*</span></span> |<span data-ttu-id="1ebfe-119">[Евентстатусенум](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="1ebfe-119">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="1ebfe-120">При вызове **события WillMove** этот параметр имеет значение **адстатусок** , если операция, вызвавшая событие, прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="1ebfe-120">When **WillMove** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="1ebfe-121">Он имеет значение **адстатускантдени** , если данное событие не может запрашивать отмену ожидающей операции.</span><span class="sxs-lookup"><span data-stu-id="1ebfe-121">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="1ebfe-122">При вызове **MoveComplete** этот параметр имеет значение **адстатусок** , если операция, вызвавшая событие, прошла успешно, или значение **адстатусеррорсоккурред** , если операция завершилась неудачно.</span><span class="sxs-lookup"><span data-stu-id="1ebfe-122">When **MoveComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span> <br/><br/><span data-ttu-id="1ebfe-123">Перед возвратом **события WillMove** присвойте этому параметру значение **адстатусканцел** , чтобы запросить отмену ожидающей операции, или присвойте этому параметру значение адстатусунвантедевент, чтобы предотвратить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="1ebfe-123">Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span> <br/><br/><span data-ttu-id="1ebfe-124">Перед возвратом **MoveComplete** присвойте этому параметру значение **адстатусунвантедевент** , чтобы предотвратить появление последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1ebfe-124">Before **MoveComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="1ebfe-125">*предшнур*</span><span class="sxs-lookup"><span data-stu-id="1ebfe-125">*pRecordset*</span></span> |<span data-ttu-id="1ebfe-126">Объект [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1ebfe-126">A [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="1ebfe-127">Объект **Recordset** , для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="1ebfe-127">The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1ebfe-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="1ebfe-128">Remarks</span></span>

<span data-ttu-id="1ebfe-129">События **события WillMove** или **MoveComplete** могут возникать из-за следующих операций с **набором записей** :</span><span class="sxs-lookup"><span data-stu-id="1ebfe-129">A **WillMove** or **MoveComplete** event may occur due to the following **Recordset** operations:</span></span>

- [<span data-ttu-id="1ebfe-130">Open</span><span class="sxs-lookup"><span data-stu-id="1ebfe-130">Open</span></span>](open-method-ado-recordset.md)
- [<span data-ttu-id="1ebfe-131">Move</span><span class="sxs-lookup"><span data-stu-id="1ebfe-131">Move</span></span>](move-method-ado.md)
- [<span data-ttu-id="1ebfe-132">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="1ebfe-132">MoveFirst</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="1ebfe-133">MoveLast</span><span class="sxs-lookup"><span data-stu-id="1ebfe-133">MoveLast</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="1ebfe-134">MoveNext</span><span class="sxs-lookup"><span data-stu-id="1ebfe-134">MoveNext</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [<span data-ttu-id="1ebfe-135">MovePrevious</span><span class="sxs-lookup"><span data-stu-id="1ebfe-135">MovePrevious</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="1ebfe-136">AddNew</span><span class="sxs-lookup"><span data-stu-id="1ebfe-136">AddNew</span></span>](addnew-method-ado.md)
- [<span data-ttu-id="1ebfe-137">Requery</span><span class="sxs-lookup"><span data-stu-id="1ebfe-137">Requery</span></span>](requery-method-ado.md)

<span data-ttu-id="1ebfe-138">Эти события могут возникать из-за следующих свойств:</span><span class="sxs-lookup"><span data-stu-id="1ebfe-138">These events may occur because of the following properties:</span></span>

- [<span data-ttu-id="1ebfe-139">Filter</span><span class="sxs-lookup"><span data-stu-id="1ebfe-139">Filter</span></span>](filter-property-ado.md)
- [<span data-ttu-id="1ebfe-140">Индекс</span><span class="sxs-lookup"><span data-stu-id="1ebfe-140">Index</span></span>](index-property-ado.md)
- [<span data-ttu-id="1ebfe-141">Bookmark</span><span class="sxs-lookup"><span data-stu-id="1ebfe-141">Bookmark</span></span>](bookmark-property-ado.md)
- [<span data-ttu-id="1ebfe-142">AbsolutePage</span><span class="sxs-lookup"><span data-stu-id="1ebfe-142">AbsolutePage</span></span>](absolutepage-property-ado.md)
- [<span data-ttu-id="1ebfe-143">AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="1ebfe-143">AbsolutePosition</span></span>](absoluteposition-property-ado.md)

<span data-ttu-id="1ebfe-144">Эти события также возникают, если для дочернего объекта **Recordset** имеются связанные события **Recordset** и перемещен родительский **набор записей** .</span><span class="sxs-lookup"><span data-stu-id="1ebfe-144">These events also occur if a child **Recordset** has **Recordset** events connected and the parent **Recordset** is moved.</span></span>

<span data-ttu-id="1ebfe-145">Необходимо задать для параметра *адстатус* значение **адстатусунвантедевент** для каждого возможного значения *адреасон* , чтобы полностью остановить уведомление о событии для любого события, включающего параметр *адреасон* .</span><span class="sxs-lookup"><span data-stu-id="1ebfe-145">You must set the *adStatus* parameter to **adStatusUnwantedEvent** for each possible *adReason* value in order to completely stop event notification for any event that includes an *adReason* parameter.</span></span>

