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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302487"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a><span data-ttu-id="7d70a-102">События WillChangeField и FieldChangeComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="7d70a-102">WillChangeField and FieldChangeComplete events (ADO)</span></span>

<span data-ttu-id="7d70a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d70a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7d70a-104">Событие **WillChangeField** вызвано перед изменением ожидающих операций значения одного или более объектов [Field](field-object-ado.md) в [наборе записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="7d70a-104">The **WillChangeField** event is called before a pending operation changes the value of one or more [Field](field-object-ado.md) objects in the [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="7d70a-105">Событие **FieldChangeComplete** вызвано после изменения значения одного или более объектов **Field.**</span><span class="sxs-lookup"><span data-stu-id="7d70a-105">The **FieldChangeComplete** event is called after the value of one or more **Field** objects has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d70a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d70a-106">Syntax</span></span>

<span data-ttu-id="7d70a-107">WillChangeField *cFields,* *Fields,* *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="7d70a-107">WillChangeField *cFields*, *Fields*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="7d70a-108">FieldChangeComplete *cFields,* *Fields,* *pError,* *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="7d70a-108">FieldChangeComplete *cFields*, *Fields*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="7d70a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d70a-109">Parameters</span></span>

|<span data-ttu-id="7d70a-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="7d70a-110">Parameter</span></span>|<span data-ttu-id="7d70a-111">Описание</span><span class="sxs-lookup"><span data-stu-id="7d70a-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7d70a-112">*cFields*</span><span class="sxs-lookup"><span data-stu-id="7d70a-112">*cFields*</span></span> |<span data-ttu-id="7d70a-113">**Длинное,** которое указывает количество объектов **Field** в *полях.*</span><span class="sxs-lookup"><span data-stu-id="7d70a-113">A **Long** that indicates the number of **Field** objects in *Fields*.</span></span>|
|<span data-ttu-id="7d70a-114">*Fields*</span><span class="sxs-lookup"><span data-stu-id="7d70a-114">*Fields*</span></span> |<span data-ttu-id="7d70a-115">Для **WillChangeField** параметр *Fields* — это массив **variant,** содержащий **объекты Field** с исходными значениями.</span><span class="sxs-lookup"><span data-stu-id="7d70a-115">For **WillChangeField**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the original values.</span></span> <br/><br/><span data-ttu-id="7d70a-116">Для **FieldChangeComplete** параметр *Fields* — это массив **вариантов,** содержащий **объекты Field** с измененными значениями.</span><span class="sxs-lookup"><span data-stu-id="7d70a-116">For **FieldChangeComplete**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the changed values.</span></span>|
|<span data-ttu-id="7d70a-117">*pError*</span><span class="sxs-lookup"><span data-stu-id="7d70a-117">*pError*</span></span> |<span data-ttu-id="7d70a-118">Объект [Error.](error-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="7d70a-118">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="7d70a-119">В ней описывается ошибка, которая произошла, если *значением adStatus* является **adStatusErrorsOccurred;** в противном случае он не установлен.</span><span class="sxs-lookup"><span data-stu-id="7d70a-119">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="7d70a-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="7d70a-120">*adStatus*</span></span> |<span data-ttu-id="7d70a-121">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="7d70a-121">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="7d70a-122">При **вызывается WillChangeField,** этот параметр задан как **adStatusOK,** если операция, которая вызвала событие, была успешной.</span><span class="sxs-lookup"><span data-stu-id="7d70a-122">When **WillChangeField** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="7d70a-123">Если это событие не может запросить отмену ожидающей операции, ему задается **adStatusCantDeny.**</span><span class="sxs-lookup"><span data-stu-id="7d70a-123">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="7d70a-124">При вызывается **FieldChangeComplete,** этот параметр задан как **adStatusOK,** если операция, которая привела к событию, была успешной, или **adStatusErrorsOccurred,** если операция не удалась.</span><span class="sxs-lookup"><span data-stu-id="7d70a-124">When **FieldChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span> <br/><br/><span data-ttu-id="7d70a-125">Перед **возвратом WillChangeField** установите для этого параметра **параметр adStatusCancel** запрос на отмену ожидающих операций.</span><span class="sxs-lookup"><span data-stu-id="7d70a-125">Before **WillChangeField** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="7d70a-126">Перед **возвратом FieldChangeComplete** установите для этого параметра **параметр adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="7d70a-126">Before **FieldChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="7d70a-127">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="7d70a-127">*pRecordset*</span></span> |<span data-ttu-id="7d70a-128">Объект **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="7d70a-128">A **Recordset** object.</span></span> <span data-ttu-id="7d70a-129">Набор **записей,** для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="7d70a-129">The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7d70a-130">Заметки</span><span class="sxs-lookup"><span data-stu-id="7d70a-130">Remarks</span></span>

<span data-ttu-id="7d70a-131">Событие **WillChangeField** или **FieldChangeComplete** может возникать при установке свойства [Value](value-property-ado.md) и вызове метода [Update](update-method-ado.md) с параметрами массива полей и значений.</span><span class="sxs-lookup"><span data-stu-id="7d70a-131">A **WillChangeField** or **FieldChangeComplete** event may occur when setting the [Value](value-property-ado.md) property and calling the [Update](update-method-ado.md) method with field and value array parameters.</span></span>

