---
title: Объектная модель компонентов и MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cf687a7bfadb0981ca3440c2f81bc5de8f910924
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808197"
---
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="e627e-103">Объектная модель компонентов и MAPI</span><span class="sxs-lookup"><span data-stu-id="e627e-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="e627e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e627e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e627e-105">Документация по Windows SDK документы с этим правилам при внедрении объекты, которые соответствуют для модели компонентных объектов (COM).</span><span class="sxs-lookup"><span data-stu-id="e627e-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="e627e-106">Эти правила рассматриваются как сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="e627e-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="e627e-107">Разработка интерфейсов и объекты.</span><span class="sxs-lookup"><span data-stu-id="e627e-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="e627e-108">Реализуйте интерфейс [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e627e-108">Implement the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="e627e-109">Управление памятью.</span><span class="sxs-lookup"><span data-stu-id="e627e-109">Manage memory.</span></span>
    
- <span data-ttu-id="e627e-110">Обработка подсчет ссылок.</span><span class="sxs-lookup"><span data-stu-id="e627e-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="e627e-111">Реализация объектов COM объектов.</span><span class="sxs-lookup"><span data-stu-id="e627e-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="e627e-112">Несмотря на то, что все объекты MAPI считаются на основе COM, так как их реализовать интерфейсы, производные от [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx), в некоторых случаях из стандартных правил COM отличается MAPI.</span><span class="sxs-lookup"><span data-stu-id="e627e-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="e627e-113">В этом отклонение разработчики большая гибкость в их реализации.</span><span class="sxs-lookup"><span data-stu-id="e627e-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="e627e-114">К примеру интерфейса MAPI, как и любой COM-интерфейс описывает контракт между разработчик и вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="e627e-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="e627e-115">После создания и публикации интерфейс его определение не может и не изменяется.</span><span class="sxs-lookup"><span data-stu-id="e627e-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="e627e-116">MAPI не отличаются от это описание, но он немного ослабляет используемые описание.</span><span class="sxs-lookup"><span data-stu-id="e627e-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="e627e-117">Специалистов по внедрению можно выбрать реализует конкретного способа возвращает одно из следующих значений ошибка вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="e627e-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="e627e-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e627e-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="e627e-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="e627e-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="e627e-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="e627e-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="e627e-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e627e-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="e627e-122">Другие отклонений от стандартных правил COM, описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e627e-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="e627e-123">**Правила программирования COM**</span><span class="sxs-lookup"><span data-stu-id="e627e-123">**COM programming rule**</span></span>|<span data-ttu-id="e627e-124">**MAPI вариантов**</span><span class="sxs-lookup"><span data-stu-id="e627e-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e627e-125">Все параметры строки в методы интерфейса должны быть Юникод.</span><span class="sxs-lookup"><span data-stu-id="e627e-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="e627e-126">Интерфейсы MAPI определены для разрешения параметров строки Юникод или ANSI.</span><span class="sxs-lookup"><span data-stu-id="e627e-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="e627e-127">Множество методов, которые имеют строковый параметр, также имеют параметр **ulFlags** ; значение флага MAPI_UNICODE в **ulFlags**указывает ширину строковый параметр.</span><span class="sxs-lookup"><span data-stu-id="e627e-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="e627e-128">Некоторые интерфейсы MAPI не поддерживает Юникод и возврата MAPI_E_BAD_CHARWIDTH при установке флага MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="e627e-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="e627e-129">Все методы интерфейса должен иметь тип возвращаемого значения HRESULT.</span><span class="sxs-lookup"><span data-stu-id="e627e-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="e627e-130">MAPI есть по крайней мере один метод, который возвращает значение, не являющиеся HRESULT: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="e627e-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="e627e-131">Вызывающих объектов и специалистов по внедрению следует выделить и освободить память для параметров интерфейса с помощью стандартных механизмов выделения задач COM.</span><span class="sxs-lookup"><span data-stu-id="e627e-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="e627e-132">Все методы интерфейса MAPI для управления памяти для параметров интерфейса использовать связанные выделения пространства [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e627e-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="e627e-133">Все реализации MAPI интерфейсы, определенные OLE, такие как [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)использовать стандартный выделения пространства задач COM.</span><span class="sxs-lookup"><span data-stu-id="e627e-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="e627e-134">Все параметры указатель должен явно иметь значение NULL при сбое метода.</span><span class="sxs-lookup"><span data-stu-id="e627e-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="e627e-135">Интерфейсы MAPI требуется, что выходные параметры указателя быть задано значение NULL или не изменяются, когда метод не удается выполнить.</span><span class="sxs-lookup"><span data-stu-id="e627e-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="e627e-136">Все реализации интерфейса MAPI интерфейсы, определенные OLE явно задать выходные параметры значение NULL в случае ошибки.</span><span class="sxs-lookup"><span data-stu-id="e627e-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="e627e-137">Реализация комбинируемого объектов, когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="e627e-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="e627e-138">Интерфейсы MAPI не комбинируемого.</span><span class="sxs-lookup"><span data-stu-id="e627e-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e627e-139">См. также</span><span class="sxs-lookup"><span data-stu-id="e627e-139">See also</span></span>



[<span data-ttu-id="e627e-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e627e-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="e627e-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="e627e-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="e627e-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e627e-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="e627e-143">Обзор интерфейса и объект MAPI</span><span class="sxs-lookup"><span data-stu-id="e627e-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

