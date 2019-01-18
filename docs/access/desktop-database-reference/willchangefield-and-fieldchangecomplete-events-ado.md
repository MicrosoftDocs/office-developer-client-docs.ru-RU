---
title: События WillChangeField и FieldChangeComplete (ADO)
TOCTitle: WillChangeField and FieldChangeComplete events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fd952cc09f410752f3eb7b5963059f8d6ee7c2c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700187"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a><span data-ttu-id="57af2-102">События WillChangeField и FieldChangeComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="57af2-102">WillChangeField and FieldChangeComplete events (ADO)</span></span>

<span data-ttu-id="57af2-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="57af2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="57af2-104">Событие **WillChangeField** вызывается перед ожидающие операции изменяется значение один или несколько объектов [поля](field-object-ado.md) в [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="57af2-104">The **WillChangeField** event is called before a pending operation changes the value of one or more [Field](field-object-ado.md) objects in the [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="57af2-105">Событие **FieldChangeComplete** вызывается после изменения значения одного или нескольких объектов **поля** .</span><span class="sxs-lookup"><span data-stu-id="57af2-105">The **FieldChangeComplete** event is called after the value of one or more **Field** objects has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="57af2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57af2-106">Syntax</span></span>

<span data-ttu-id="57af2-107">WillChangeField*cFields*, *поля* *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="57af2-107">WillChangeField*cFields*, *Fields*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="57af2-108">*CFields*, *полей*, FieldChangeComplete *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="57af2-108">FieldChangeComplete*cFields*, *Fields*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="57af2-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="57af2-109">Parameters</span></span>

|<span data-ttu-id="57af2-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="57af2-110">Parameter</span></span>|<span data-ttu-id="57af2-111">Описание</span><span class="sxs-lookup"><span data-stu-id="57af2-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="57af2-112">*cFields*</span><span class="sxs-lookup"><span data-stu-id="57af2-112">*cFields*</span></span> |<span data-ttu-id="57af2-113">**Long** , указывающее количество объектов **поля** в *полях*.</span><span class="sxs-lookup"><span data-stu-id="57af2-113">A **Long** that indicates the number of **Field** objects in *Fields*.</span></span>|
|<span data-ttu-id="57af2-114">*Fields*</span><span class="sxs-lookup"><span data-stu-id="57af2-114">*Fields*</span></span> |<span data-ttu-id="57af2-115">Для **WillChangeField**параметр *поля* представляет собой массив **типа Variant** , которая содержит **поля** объекты на основе исходных значений.</span><span class="sxs-lookup"><span data-stu-id="57af2-115">For **WillChangeField**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the original values.</span></span> <br/><br/><span data-ttu-id="57af2-116">Для **FieldChangeComplete**параметр *поля* представляет собой массив **типа Variant** , которая содержит объекты **поля** с измененными значениями.</span><span class="sxs-lookup"><span data-stu-id="57af2-116">For **FieldChangeComplete**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the changed values.</span></span>|
|<span data-ttu-id="57af2-117">*pError*</span><span class="sxs-lookup"><span data-stu-id="57af2-117">*pError*</span></span> |<span data-ttu-id="57af2-118">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="57af2-118">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="57af2-119">Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="57af2-119">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="57af2-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="57af2-120">*adStatus*</span></span> |<span data-ttu-id="57af2-121">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="57af2-121">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="57af2-122">При вызове **WillChangeField** этот параметр имеет значение **adStatusOK** , если операция, которая вызвала событие прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="57af2-122">When **WillChangeField** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="57af2-123">Если это событие не могут запрашивать отмену ожидающие операции перейдут в **adStatusCantDeny** .</span><span class="sxs-lookup"><span data-stu-id="57af2-123">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="57af2-124">При вызове **FieldChangeComplete** этот параметр имеет значение **adStatusOK** в случае успешного операцию, которая вызвала событие или **adStatusErrorsOccurred** , если операция завершилась неудачно.</span><span class="sxs-lookup"><span data-stu-id="57af2-124">When **FieldChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span> <br/><br/><span data-ttu-id="57af2-125">Прежде чем возвращает **WillChangeField** , присвойте этому параметру значение **adStatusCancel** , чтобы запросить отмену ожидающие операции.</span><span class="sxs-lookup"><span data-stu-id="57af2-125">Before **WillChangeField** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="57af2-126">Прежде чем возвращает **FieldChangeComplete** , присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="57af2-126">Before **FieldChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="57af2-127">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="57af2-127">*pRecordset*</span></span> |<span data-ttu-id="57af2-128">Объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="57af2-128">A **Recordset** object.</span></span> <span data-ttu-id="57af2-129">**Набор записей** , для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="57af2-129">The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="57af2-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="57af2-130">Remarks</span></span>

<span data-ttu-id="57af2-131">Событие **WillChangeField** или **FieldChangeComplete** может возникнуть при установке свойства [Value](value-property-ado.md) и вызова метода [обновления](update-method-ado.md) с поля и значения массива параметров.</span><span class="sxs-lookup"><span data-stu-id="57af2-131">A **WillChangeField** or **FieldChangeComplete** event may occur when setting the [Value](value-property-ado.md) property and calling the [Update](update-method-ado.md) method with field and value array parameters.</span></span>

