---
title: События WillChangeField и FieldChangeComplete (ADO)
TOCTitle: WillChangeField and FieldChangeComplete events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2967b6670ad96752e7ce47d82227fad70335e1f6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927405"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a><span data-ttu-id="8ed9d-102">События WillChangeField и FieldChangeComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="8ed9d-102">WillChangeField and FieldChangeComplete events (ADO)</span></span>


<span data-ttu-id="8ed9d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ed9d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ed9d-104">Событие **WillChangeField** вызывается перед ожидающие операции изменяется значение один или несколько объектов [поля](field-object-ado.md) в [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8ed9d-104">The **WillChangeField** event is called before a pending operation changes the value of one or more [Field](field-object-ado.md) objects in the [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="8ed9d-105">Событие **FieldChangeComplete** вызывается после изменения значения одного или нескольких объектов **поля** .</span><span class="sxs-lookup"><span data-stu-id="8ed9d-105">The **FieldChangeComplete** event is called after the value of one or more **Field** objects has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ed9d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ed9d-106">Syntax</span></span>

<span data-ttu-id="8ed9d-107">WillChangeField*cFields*, *поля* *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="8ed9d-107">WillChangeField*cFields*, *Fields*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="8ed9d-108">*CFields*, *полей*, FieldChangeComplete *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="8ed9d-108">FieldChangeComplete*cFields*, *Fields*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="8ed9d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ed9d-109">Parameters</span></span>

  - <span data-ttu-id="8ed9d-110">*cFields*</span><span class="sxs-lookup"><span data-stu-id="8ed9d-110">*cFields*</span></span>

  - <span data-ttu-id="8ed9d-111">**Long** , указывающее количество объектов **поля** в *полях*.</span><span class="sxs-lookup"><span data-stu-id="8ed9d-111">A **Long** that indicates the number of **Field** objects in *Fields*.</span></span>

  - <span data-ttu-id="8ed9d-112">*Поля*</span><span class="sxs-lookup"><span data-stu-id="8ed9d-112">*Fields*</span></span>

  - <span data-ttu-id="8ed9d-113">Для **WillChangeField**параметр *поля* представляет собой массив **типа Variant** , которая содержит **поля** объекты на основе исходных значений.</span><span class="sxs-lookup"><span data-stu-id="8ed9d-113">For **WillChangeField**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the original values.</span></span>  
      
    <span data-ttu-id="8ed9d-114">Для **FieldChangeComplete**параметр *поля* представляет собой массив **типа Variant** , которая содержит объекты **поля** с измененными значениями.</span><span class="sxs-lookup"><span data-stu-id="8ed9d-114">For **FieldChangeComplete**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the changed values.</span></span>

  - <span data-ttu-id="8ed9d-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="8ed9d-115">*pError*</span></span>

  - <span data-ttu-id="8ed9d-116">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="8ed9d-116">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="8ed9d-117">Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="8ed9d-117">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="8ed9d-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="8ed9d-118">*adStatus*</span></span>

  - [<span data-ttu-id="8ed9d-119">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="8ed9d-119">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="8ed9d-120">При вызове **WillChangeField** этот параметр имеет значение **adStatusOK** , если операция, которая вызвала событие прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="8ed9d-120">When **WillChangeField** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="8ed9d-121">Если это событие не могут запрашивать отмену ожидающие операции перейдут в **adStatusCantDeny** .</span><span class="sxs-lookup"><span data-stu-id="8ed9d-121">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="8ed9d-122">При вызове **FieldChangeComplete** этот параметр имеет значение **adStatusOK** в случае успешного операцию, которая вызвала событие или **adStatusErrorsOccurred** , если операция завершилась неудачно.</span><span class="sxs-lookup"><span data-stu-id="8ed9d-122">When **FieldChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span>
    
    <span data-ttu-id="8ed9d-123">Прежде чем возвращает **WillChangeField** , присвойте этому параметру значение **adStatusCancel** , чтобы запросить отмену ожидающие операции.</span><span class="sxs-lookup"><span data-stu-id="8ed9d-123">Before **WillChangeField** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="8ed9d-124">Прежде чем возвращает **FieldChangeComplete** , присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="8ed9d-124">Before **FieldChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="8ed9d-125">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="8ed9d-125">*pRecordset*</span></span>

  - <span data-ttu-id="8ed9d-126">Объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="8ed9d-126">A **Recordset** object.</span></span> <span data-ttu-id="8ed9d-127">**Набор записей** , для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="8ed9d-127">The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ed9d-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ed9d-128">Remarks</span></span>

<span data-ttu-id="8ed9d-129">Событие **WillChangeField** или **FieldChangeComplete** может возникнуть при установке свойства [Value](value-property-ado.md) и вызова метода [обновления](update-method-ado.md) с поля и значения массива параметров.</span><span class="sxs-lookup"><span data-stu-id="8ed9d-129">A **WillChangeField** or **FieldChangeComplete** event may occur when setting the [Value](value-property-ado.md) property and calling the [Update](update-method-ado.md) method with field and value array parameters.</span></span>

