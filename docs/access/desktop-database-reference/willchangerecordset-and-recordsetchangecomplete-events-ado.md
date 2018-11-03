---
title: События WillChangeRecordset и RecordsetChangeComplete (ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ac85cd672a07d65b19578daa8ca737af584972a2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919145"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a><span data-ttu-id="ec835-102">События WillChangeRecordset и RecordsetChangeComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="ec835-102">WillChangeRecordset and RecordsetChangeComplete events (ADO)</span></span>


<span data-ttu-id="ec835-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec835-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="ec835-104">Событие **WillChangeRecordset** вызывается перед операцию ожидающие изменения [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ec835-104">The **WillChangeRecordset** event is called before a pending operation changes the [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="ec835-105">Событие **RecordsetChangeComplete** вызывается после изменения **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ec835-105">The **RecordsetChangeComplete** event is called after the **Recordset** has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec835-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec835-106">Syntax</span></span>

<span data-ttu-id="ec835-107">WillChangeRecordset*adReason*, *adStatus* *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="ec835-107">WillChangeRecordset*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="ec835-108">RecordsetChangeComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="ec835-108">RecordsetChangeComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="ec835-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec835-109">Parameters</span></span>

  - <span data-ttu-id="ec835-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="ec835-110">*adReason*</span></span>

  - <span data-ttu-id="ec835-111">Значение [EventReasonEnum](eventreasonenum.md) , указывает причину это событие.</span><span class="sxs-lookup"><span data-stu-id="ec835-111">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event.</span></span> <span data-ttu-id="ec835-112">Его значение может быть **adRsnRequery**, **adRsnResynch**, **adRsnClose**, **adRsnOpen**.</span><span class="sxs-lookup"><span data-stu-id="ec835-112">Its value can be **adRsnRequery**, **adRsnResynch**, **adRsnClose**, **adRsnOpen**.</span></span>

  - <span data-ttu-id="ec835-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="ec835-113">*adStatus*</span></span>

  - [<span data-ttu-id="ec835-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="ec835-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="ec835-115">При вызове **WillChangeRecordset** этот параметр имеет значение **adStatusOK** , если операция, которая вызвала событие прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="ec835-115">When **WillChangeRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="ec835-116">Если это событие не могут запрашивать отмену ожидающие операции перейдут в **adStatusCantDeny** .</span><span class="sxs-lookup"><span data-stu-id="ec835-116">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="ec835-117">При вызове **RecordsetChangeComplete** этот параметр имеет значение **adStatusOK** , если операция, которая вызвала событие прошла успешно, **adStatusErrorsOccurred** , если операция завершилась неудачно или **adStatusCancel** при операции связанные с ранее обслуживаемых событие **WillChangeRecordset** было отменено.</span><span class="sxs-lookup"><span data-stu-id="ec835-117">When **RecordsetChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, **adStatusErrorsOccurred** if the operation failed, or **adStatusCancel** if the operation associated with the previously accepted **WillChangeRecordset** event has been canceled.</span></span>
    
    <span data-ttu-id="ec835-118">Прежде чем возвращает **WillChangeRecordset** , присвойте этому параметру значение **adStatusCancel** для запроса отмены ожидающие операции или присвойте этому параметру значение adStatusUnwantedEvent, чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="ec835-118">Before **WillChangeRecordset** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notifications.</span></span>
    
    <span data-ttu-id="ec835-119">Прежде чем **WillChangeRecordset** или возвращает **RecordsetChangeComplete** присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="ec835-119">Before **WillChangeRecordset** or **RecordsetChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="ec835-120">*pError*</span><span class="sxs-lookup"><span data-stu-id="ec835-120">*pError*</span></span>

  - <span data-ttu-id="ec835-121">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="ec835-121">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="ec835-122">Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="ec835-122">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="ec835-123">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="ec835-123">*pRecordset*</span></span>

  - <span data-ttu-id="ec835-124">Объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ec835-124">A **Recordset** object.</span></span> <span data-ttu-id="ec835-125">**Набор записей** , для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="ec835-125">The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec835-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="ec835-126">Remarks</span></span>

<span data-ttu-id="ec835-127">**WillChangeRecordset** или **RecordsetChangeComplete** события могут быть вызваны методы **записей** [повторный запрос](requery-method-ado.md) или [Открыть](open-method-ado-recordset.md) .</span><span class="sxs-lookup"><span data-stu-id="ec835-127">A **WillChangeRecordset** or **RecordsetChangeComplete** event may occur due to the **Recordset** [Requery](requery-method-ado.md) or [Open](open-method-ado-recordset.md) methods.</span></span>

<span data-ttu-id="ec835-128">Если поставщик поддерживает закладки, уведомления о событии **RecordsetChange** возникает каждый раз, когда новые строки извлекаются из поставщика.</span><span class="sxs-lookup"><span data-stu-id="ec835-128">If the provider does not support bookmarks, a **RecordsetChange** event notification occurs each time new rows are retrieved from the provider.</span></span> <span data-ttu-id="ec835-129">Частота это событие зависит от свойства **RecordsetCacheSize** .</span><span class="sxs-lookup"><span data-stu-id="ec835-129">The frequency of this event depends on the **RecordsetCacheSize** property.</span></span>

<span data-ttu-id="ec835-130">Параметр **adStatus** должен значение **adStatusUnwantedEvent** для каждого **adReason** возможные значения для полностью остановите уведомления о событиях для любого события, которое включает параметр **adReason** .</span><span class="sxs-lookup"><span data-stu-id="ec835-130">You must set the **adStatus** parameter to **adStatusUnwantedEvent** for each possible **adReason** value in order to completely stop event notification for any event that includes an **adReason** parameter.</span></span>

