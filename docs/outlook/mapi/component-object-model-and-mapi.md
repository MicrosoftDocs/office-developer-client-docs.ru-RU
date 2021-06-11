---
title: Модель COM и MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a91ab8497a690fd4b99f76274d0213284253fd06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334470"
---
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="5c23f-103">Модель COM и MAPI</span><span class="sxs-lookup"><span data-stu-id="5c23f-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="5c23f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c23f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c23f-105">Документация Windows SDK включает всестороннее обсуждение правил реализации объектов, которые соответствуют объектной модели компонентов (COM).</span><span class="sxs-lookup"><span data-stu-id="5c23f-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="5c23f-106">В этих правилах решается вопрос о том, как сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="5c23f-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="5c23f-107">Проектирование интерфейсов и объектов.</span><span class="sxs-lookup"><span data-stu-id="5c23f-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="5c23f-108">Реализация [интерфейса IUnknown.](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c23f-108">Implement the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="5c23f-109">Управление памятью.</span><span class="sxs-lookup"><span data-stu-id="5c23f-109">Manage memory.</span></span>
    
- <span data-ttu-id="5c23f-110">Обработка подсчета ссылок.</span><span class="sxs-lookup"><span data-stu-id="5c23f-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="5c23f-111">Реализация объектов с резьбой по квартирам.</span><span class="sxs-lookup"><span data-stu-id="5c23f-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="5c23f-112">Хотя все объекты MAPI считаются com-базами, так как они реализуют интерфейсы, унаследованные от [IUnknown,](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)MAPI в некоторых ситуациях отклоняется от стандартных правил COM.</span><span class="sxs-lookup"><span data-stu-id="5c23f-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="5c23f-113">Это отклонение позволяет разработчикам более гибко использовать их реализацию.</span><span class="sxs-lookup"><span data-stu-id="5c23f-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="5c23f-114">Например, интерфейс MAPI, как и любой интерфейс COM, описывает контракт между реализации и вызываемой.</span><span class="sxs-lookup"><span data-stu-id="5c23f-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="5c23f-115">После создания и публикации интерфейса его определение не может и не меняется.</span><span class="sxs-lookup"><span data-stu-id="5c23f-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="5c23f-116">MAPI не отклоняться от этого описания, но это несколько расслабляет описание.</span><span class="sxs-lookup"><span data-stu-id="5c23f-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="5c23f-117">Реализация может не реализовывать определенные методы, возвращая одному из следующих значений ошибки вызываемого:</span><span class="sxs-lookup"><span data-stu-id="5c23f-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="5c23f-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="5c23f-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="5c23f-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="5c23f-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="5c23f-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5c23f-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="5c23f-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="5c23f-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="5c23f-122">Другие отклонения от стандартных правил COM описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5c23f-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="5c23f-123">**Правило программирования COM**</span><span class="sxs-lookup"><span data-stu-id="5c23f-123">**COM programming rule**</span></span>|<span data-ttu-id="5c23f-124">**Вариант MAPI**</span><span class="sxs-lookup"><span data-stu-id="5c23f-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c23f-125">Все параметры строки в методах интерфейса должны быть Юникодом.</span><span class="sxs-lookup"><span data-stu-id="5c23f-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="5c23f-126">Интерфейсы MAPI определяются для разрешения параметров строки Unicode или ANSI.</span><span class="sxs-lookup"><span data-stu-id="5c23f-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="5c23f-127">Многие методы, которые имеют параметр строки, также имеют **параметр ulFlags;** ширина параметра строки указывается значением флага MAPI_UNICODE **в ulFlags**.</span><span class="sxs-lookup"><span data-stu-id="5c23f-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="5c23f-128">Некоторые интерфейсы MAPI не поддерживают Юникод и возвращают MAPI_E_BAD_CHARWIDTH при MAPI_UNICODE флага.</span><span class="sxs-lookup"><span data-stu-id="5c23f-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="5c23f-129">Все методы интерфейса должны иметь возвращаемого типа HRESULT.</span><span class="sxs-lookup"><span data-stu-id="5c23f-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="5c23f-130">MAPI имеет по крайней мере один метод, который возвращает значение, не относящеся к HRESULT: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="5c23f-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="5c23f-131">Звонители и реализутели должны выделять и бесплатно выделять память для параметров интерфейса с помощью стандартных распределителей задач COM.</span><span class="sxs-lookup"><span data-stu-id="5c23f-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="5c23f-132">Все методы MAPI используют связанные алокаторы [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer](mapifreebuffer.md) для управления памятью для параметров интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5c23f-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="5c23f-133">Все реализации интерфейсов MAPI, определенных OLE, например [IStream,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)используют стандартные ком-решения задач.</span><span class="sxs-lookup"><span data-stu-id="5c23f-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="5c23f-134">Все параметры указателя на выходе должны быть явно заданы NULL при сбой метода.</span><span class="sxs-lookup"><span data-stu-id="5c23f-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="5c23f-135">Интерфейсы MAPI требуют, чтобы параметры указателей либо были заданы nULL, либо оставались неизменными при сбой метода.</span><span class="sxs-lookup"><span data-stu-id="5c23f-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="5c23f-136">Все реализации интерфейсов MAPI, определенные OLE, явно определяют параметры NULL при сбое.</span><span class="sxs-lookup"><span data-stu-id="5c23f-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="5c23f-137">Реализация агрегируемых объектов по мере возможности.</span><span class="sxs-lookup"><span data-stu-id="5c23f-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="5c23f-138">Интерфейсы MAPI не являются агрегируемыми.</span><span class="sxs-lookup"><span data-stu-id="5c23f-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c23f-139">См. также</span><span class="sxs-lookup"><span data-stu-id="5c23f-139">See also</span></span>



[<span data-ttu-id="5c23f-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="5c23f-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="5c23f-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="5c23f-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="5c23f-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5c23f-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="5c23f-143">Обзор объектов и интерфейсов MAPI</span><span class="sxs-lookup"><span data-stu-id="5c23f-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

