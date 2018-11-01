---
title: WillChangeRecord и RecordChangeComplete события (ADO)
TOCTitle: WillChangeRecord and RecordChangeComplete Events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 895a80cf4810088b5f18f4a9416e7eadc54a004f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878131"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a><span data-ttu-id="9d4e2-102">WillChangeRecord и RecordChangeComplete события (ADO)</span><span class="sxs-lookup"><span data-stu-id="9d4e2-102">WillChangeRecord and RecordChangeComplete Events (ADO)</span></span>


<span data-ttu-id="9d4e2-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d4e2-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="9d4e2-104">Событие **WillChangeRecord** вызывается перед измените один или несколько записей (строк) в [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="9d4e2-104">The **WillChangeRecord** event is called before one or more records (rows) in the [Recordset](recordset-object-ado.md) change.</span></span> <span data-ttu-id="9d4e2-105">Событие **RecordChangeComplete** вызывается после изменения одной или нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-105">The **RecordChangeComplete** event is called after one or more records change.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d4e2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d4e2-106">Syntax</span></span>

<span data-ttu-id="9d4e2-107">WillChangeRecord*adReason*, *cRecords*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="9d4e2-107">WillChangeRecord*adReason*, *cRecords*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="9d4e2-108">RecordChangeComplete*adReason*, *cRecords*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="9d4e2-108">RecordChangeComplete*adReason*, *cRecords*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="9d4e2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d4e2-109">Parameters</span></span>

  - <span data-ttu-id="9d4e2-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="9d4e2-110">*adReason*</span></span>

  - <span data-ttu-id="9d4e2-111">Значение [EventReasonEnum](eventreasonenum.md) , указывает причину это событие.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-111">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event.</span></span> <span data-ttu-id="9d4e2-112">Его значение может быть **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**или **adRsnFirstChange**.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-112">Its value can be **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**, or **adRsnFirstChange**.</span></span>

  - <span data-ttu-id="9d4e2-113">*cRecords*</span><span class="sxs-lookup"><span data-stu-id="9d4e2-113">*cRecords*</span></span>

  - <span data-ttu-id="9d4e2-114">Значение типа **Long** , показывает, сколько изменение записей (влияет на).</span><span class="sxs-lookup"><span data-stu-id="9d4e2-114">A **Long** value that indicates the number of records changing (affected).</span></span>

  - <span data-ttu-id="9d4e2-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="9d4e2-115">*pError*</span></span>

  - <span data-ttu-id="9d4e2-116">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="9d4e2-116">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="9d4e2-117">Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-117">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="9d4e2-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="9d4e2-118">*adStatus*</span></span>

  - [<span data-ttu-id="9d4e2-119">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="9d4e2-119">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="9d4e2-120">При вызове **WillChangeRecord** этот параметр имеет значение **adStatusOK** , если операция, которая вызвала событие прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-120">When **WillChangeRecord** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="9d4e2-121">Если это событие не могут запрашивать отмену ожидающие операции перейдут в **adStatusCantDeny** .</span><span class="sxs-lookup"><span data-stu-id="9d4e2-121">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="9d4e2-122">При вызове **RecordChangeComplete** этот параметр имеет значение **adStatusOK** в случае успешного операцию, которая вызвала событие или **adStatusErrorsOccurred** , если операция завершилась неудачно.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-122">When **RecordChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span>
    
    <span data-ttu-id="9d4e2-123">Прежде чем возвращает **WillChangeRecord** , присвойте этому параметру значение **adStatusCancel** для отмены запроса, которое вызвало это событие или присвойте этому параметру значение adStatusUnwantedEvent, чтобы запретить последующие notications операции.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-123">Before **WillChangeRecord** returns, set this parameter to **adStatusCancel** to request cancellation of the operation that caused this event or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span>
    
    <span data-ttu-id="9d4e2-124">Прежде чем возвращает **RecordChangeComplete** , присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-124">Before **RecordChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="9d4e2-125">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="9d4e2-125">*pRecordset*</span></span>

  - <span data-ttu-id="9d4e2-126">Объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="9d4e2-126">A **Recordset** object.</span></span> <span data-ttu-id="9d4e2-127">**Набор записей** , для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-127">The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d4e2-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="9d4e2-128">Remarks</span></span>

<span data-ttu-id="9d4e2-129">**WillChangeRecord** или **RecordChangeComplete** событие может произойти для первого измененные поля в строке из-за следующие операции **записей** : [обновление](update-method-ado.md), [Удаление](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [ UpdateBatch](updatebatch-method-ado.md)и [CancelBatch](cancelbatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9d4e2-129">A **WillChangeRecord** or **RecordChangeComplete** event may occur for the first changed field in a row due to the following **Recordset** operations: [Update](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), and [CancelBatch](cancelbatch-method-ado.md).</span></span> <span data-ttu-id="9d4e2-130">Значение **набора записей** [CursorType](cursortype-property-ado.md) определяет, какие операции приводят к возникновении событий.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-130">The value of the **Recordset** [CursorType](cursortype-property-ado.md) determines which operations cause the events to occur.</span></span>

<span data-ttu-id="9d4e2-131">Во время события **WillChangeRecord** **записей** [фильтра](filter-property-ado.md) задано значение **adFilterAffectedRecords**.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-131">During the **WillChangeRecord** event, the **Recordset** [Filter](filter-property-ado.md) property is set to **adFilterAffectedRecords**.</span></span> <span data-ttu-id="9d4e2-132">Это свойство не может изменить при обработке события.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-132">You cannot change this property while processing the event.</span></span>

<span data-ttu-id="9d4e2-133">Параметр adStatus должен значение adStatusUnwantedEvent для каждого adReason возможные значения для полностью остановите noticiation событий для всех событий, который включает параметр adReason.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-133">You must set the adStatus parameter to adStatusUnwantedEvent for each possible adReason value in order to completely stop event noticiation for any event that includes an adReason parameter.</span></span>

