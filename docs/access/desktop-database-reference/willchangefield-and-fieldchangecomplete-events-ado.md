---
title: События события willchangefield и FieldChangeComplete (ADO)
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
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a><span data-ttu-id="0a416-102">События события willchangefield и FieldChangeComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="0a416-102">WillChangeField and FieldChangeComplete events (ADO)</span></span>

<span data-ttu-id="0a416-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a416-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0a416-104">Событие **события willchangefield** вызывается до того, как ожидающая операция изменяет значение одного или нескольких объектов [field](field-object-ado.md) в [наборе записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0a416-104">The **WillChangeField** event is called before a pending operation changes the value of one or more [Field](field-object-ado.md) objects in the [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="0a416-105">Событие **FieldChangeComplete** вызывается после того, как значение одного или нескольких объектов **поля** изменилось.</span><span class="sxs-lookup"><span data-stu-id="0a416-105">The **FieldChangeComplete** event is called after the value of one or more **Field** objects has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a416-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a416-106">Syntax</span></span>

<span data-ttu-id="0a416-107">События willchangefield*кфиелдс*, *Fields*, *адстатус*, пред \*\*</span><span class="sxs-lookup"><span data-stu-id="0a416-107">WillChangeField*cFields*, *Fields*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="0a416-108">FieldChangeComplete*кфиелдс*, *Fields*, *Перрор*, *адстатус*, пред \*\*</span><span class="sxs-lookup"><span data-stu-id="0a416-108">FieldChangeComplete*cFields*, *Fields*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="0a416-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a416-109">Parameters</span></span>

|<span data-ttu-id="0a416-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="0a416-110">Parameter</span></span>|<span data-ttu-id="0a416-111">Описание</span><span class="sxs-lookup"><span data-stu-id="0a416-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0a416-112">*Кфиелдс*</span><span class="sxs-lookup"><span data-stu-id="0a416-112">*cFields*</span></span> |<span data-ttu-id="0a416-113">Значение **типа Long** , которое указывает количество объектов **field** в *полях*.</span><span class="sxs-lookup"><span data-stu-id="0a416-113">A **Long** that indicates the number of **Field** objects in *Fields*.</span></span>|
|<span data-ttu-id="0a416-114">*Fields*</span><span class="sxs-lookup"><span data-stu-id="0a416-114">*Fields*</span></span> |<span data-ttu-id="0a416-115">Для **события willchangefield**параметр *Fields* представляет собой массив **Variant** , содержащий объекты **field** с исходными значениями.</span><span class="sxs-lookup"><span data-stu-id="0a416-115">For **WillChangeField**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the original values.</span></span> <br/><br/><span data-ttu-id="0a416-116">Для **FieldChangeComplete**параметр *Fields* представляет собой массив **Variant** , содержащий объекты **field** с измененными значениями.</span><span class="sxs-lookup"><span data-stu-id="0a416-116">For **FieldChangeComplete**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the changed values.</span></span>|
|<span data-ttu-id="0a416-117">*Перрор*</span><span class="sxs-lookup"><span data-stu-id="0a416-117">*pError*</span></span> |<span data-ttu-id="0a416-118">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="0a416-118">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="0a416-119">В нем описывается ошибка, которая возникла, если значение *адстатус* равно **адстатусеррорсоккурред**; в противном случае он не задается.</span><span class="sxs-lookup"><span data-stu-id="0a416-119">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="0a416-120">*Адстатус*</span><span class="sxs-lookup"><span data-stu-id="0a416-120">*adStatus*</span></span> |<span data-ttu-id="0a416-121">[Евентстатусенум](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="0a416-121">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="0a416-122">При вызове **события willchangefield** этот параметр имеет значение **адстатусок** , если операция, вызвавшая событие, прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="0a416-122">When **WillChangeField** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="0a416-123">Он имеет значение **адстатускантдени** , если данное событие не может запрашивать отмену ожидающей операции.</span><span class="sxs-lookup"><span data-stu-id="0a416-123">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="0a416-124">При вызове **FieldChangeComplete** этот параметр имеет значение **адстатусок** , если операция, вызвавшая событие, прошла успешно, или значение **адстатусеррорсоккурред** , если операция завершилась неудачно.</span><span class="sxs-lookup"><span data-stu-id="0a416-124">When **FieldChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span> <br/><br/><span data-ttu-id="0a416-125">Перед возвратом **события willchangefield** присвойте этому параметру значение **адстатусканцел** , чтобы запросить отмену ожидающей операции.</span><span class="sxs-lookup"><span data-stu-id="0a416-125">Before **WillChangeField** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="0a416-126">Перед возвратом **FieldChangeComplete** присвойте этому параметру значение **адстатусунвантедевент** , чтобы предотвратить появление последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0a416-126">Before **FieldChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="0a416-127">*предшнур*</span><span class="sxs-lookup"><span data-stu-id="0a416-127">*pRecordset*</span></span> |<span data-ttu-id="0a416-128">Объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="0a416-128">A **Recordset** object.</span></span> <span data-ttu-id="0a416-129">Объект **Recordset** , для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="0a416-129">The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="0a416-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="0a416-130">Remarks</span></span>

<span data-ttu-id="0a416-131">Событие **события willchangefield** или **FieldChangeComplete** может возникнуть при задании свойства [value](value-property-ado.md) и вызове метода [Update](update-method-ado.md) с параметрами массива Field и value.</span><span class="sxs-lookup"><span data-stu-id="0a416-131">A **WillChangeField** or **FieldChangeComplete** event may occur when setting the [Value](value-property-ado.md) property and calling the [Update](update-method-ado.md) method with field and value array parameters.</span></span>

