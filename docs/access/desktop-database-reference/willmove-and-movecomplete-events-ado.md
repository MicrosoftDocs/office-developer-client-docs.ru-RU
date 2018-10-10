---
title: WillMove and MoveComplete Events (ADO)
TOCTitle: WillMove and MoveComplete Events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 875b9825b1482bbd33808cafc6df626b2e78b81b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480539"
---
# <a name="willmove-and-movecomplete-events-ado"></a><span data-ttu-id="5d3d1-102">WillMove and MoveComplete Events (ADO)</span><span class="sxs-lookup"><span data-stu-id="5d3d1-102">WillMove and MoveComplete Events (ADO)</span></span>


<span data-ttu-id="5d3d1-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d3d1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5d3d1-104">Событие **WillMove** вызывается перед ожидающие операции изменяет текущую позицию в наборе [записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5d3d1-104">The **WillMove** event is called before a pending operation changes the current position in the [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="5d3d1-105">Событие **MoveComplete** вызывается после текущей позиции в изменения **записей** .</span><span class="sxs-lookup"><span data-stu-id="5d3d1-105">The **MoveComplete** event is called after the current position in the **Recordset** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d3d1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d3d1-106">Syntax</span></span>

<span data-ttu-id="5d3d1-107">WillMove*adReason*, *adStatus* *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="5d3d1-107">WillMove*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="5d3d1-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="5d3d1-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="5d3d1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d3d1-109">Parameters</span></span>

  - <span data-ttu-id="5d3d1-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="5d3d1-110">*adReason*</span></span>

  - <span data-ttu-id="5d3d1-111">Значение [EventReasonEnum](eventreasonenum.md) , указывает причину это событие.</span><span class="sxs-lookup"><span data-stu-id="5d3d1-111">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event.</span></span> <span data-ttu-id="5d3d1-112">Его значение может быть **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**или **adRsnRequery**.</span><span class="sxs-lookup"><span data-stu-id="5d3d1-112">Its value can be **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, or **adRsnRequery**.</span></span>

  - <span data-ttu-id="5d3d1-113">*pError*</span><span class="sxs-lookup"><span data-stu-id="5d3d1-113">*pError*</span></span>

  - <span data-ttu-id="5d3d1-114">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="5d3d1-114">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="5d3d1-115">Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="5d3d1-115">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="5d3d1-116">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="5d3d1-116">*adStatus*</span></span>

  - [<span data-ttu-id="5d3d1-117">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="5d3d1-117">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="5d3d1-118">При вызове **WillMove** этот параметр имеет значение **adStatusOK** , если операция, которая вызвала событие прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="5d3d1-118">When **WillMove** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="5d3d1-119">Если это событие не могут запрашивать отмену ожидающие операции перейдут в **adStatusCantDeny** .</span><span class="sxs-lookup"><span data-stu-id="5d3d1-119">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="5d3d1-120">При вызове **MoveComplete** этот параметр имеет значение **adStatusOK** в случае успешного операцию, которая вызвала событие или **adStatusErrorsOccurred** , если операция завершилась неудачно.</span><span class="sxs-lookup"><span data-stu-id="5d3d1-120">When **MoveComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span>
    
    <span data-ttu-id="5d3d1-121">Прежде чем возвращает **WillMove** , присвойте этому параметру значение **adStatusCancel** для запроса отмены ожидающие операции или присвойте этому параметру значение adStatusUnwantedEvent, чтобы запретить последующие notications.</span><span class="sxs-lookup"><span data-stu-id="5d3d1-121">Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span>
    
    <span data-ttu-id="5d3d1-122">Прежде чем возвращает **MoveComplete** , присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="5d3d1-122">Before **MoveComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="5d3d1-123">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="5d3d1-123">*pRecordset*</span></span>

  - <span data-ttu-id="5d3d1-124">Объект [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="5d3d1-124">A [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="5d3d1-125">**Набор записей** , для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="5d3d1-125">The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d3d1-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="5d3d1-126">Remarks</span></span>

<span data-ttu-id="5d3d1-127">Событие **WillMove** или **MoveComplete** могут быть вызваны следующие операции **записей** : [Открытие](open-method-ado-recordset.md), [Перемещение](move-method-ado.md), [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [AddNew](addnew-method-ado.md)и [Повторный запрос](requery-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5d3d1-127">A **WillMove** or **MoveComplete** event may occur due to the following **Recordset** operations: [Open](open-method-ado-recordset.md), [Move](move-method-ado.md), [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [AddNew](addnew-method-ado.md), and [Requery](requery-method-ado.md).</span></span> <span data-ttu-id="5d3d1-128">Эти события могут возникнуть из-за следующие свойства: [Фильтр](filter-property-ado.md), [индекса](index-property-ado.md), [закладки](bookmark-property-ado.md), [AbsolutePage](absolutepage-property-ado.md)и [AbsolutePosition](absoluteposition-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5d3d1-128">These events may occur because of the following properties: [Filter](filter-property-ado.md), [Index](index-property-ado.md), [Bookmark](bookmark-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), and [AbsolutePosition](absoluteposition-property-ado.md).</span></span> <span data-ttu-id="5d3d1-129">Эти события также возникают при дочерних **записей** имеет **записей** событий подключенных и родительский перемещены **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5d3d1-129">These events also occur if a child **Recordset** has **Recordset** events connected and the parent **Recordset** is moved.</span></span>

<span data-ttu-id="5d3d1-130">Параметр **adStatus** должен значение **adStatusUnwantedEvent** для каждого adReason возможные значения для полностью остановите уведомления о событиях для любого события, которое включает параметр adReason.</span><span class="sxs-lookup"><span data-stu-id="5d3d1-130">You must set the **adStatus** parameter to **adStatusUnwantedEvent** for each possible adReason value in order to completely stop event notification for any event that includes an adReason parameter.</span></span>

