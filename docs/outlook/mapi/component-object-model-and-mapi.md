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
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="07995-103">Модель COM и MAPI</span><span class="sxs-lookup"><span data-stu-id="07995-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="07995-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07995-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07995-105">В документации по ПАКЕТу SDK для Windows входит подробное описание правил реализации объектов, которые соответствуют модели компонентных объектов (COM).</span><span class="sxs-lookup"><span data-stu-id="07995-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="07995-106">Эти правила позволяют выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="07995-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="07995-107">РазРаботайте интерфейсы и объекты.</span><span class="sxs-lookup"><span data-stu-id="07995-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="07995-108">Реализуйте интерфейс [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="07995-108">Implement the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="07995-109">Управление памятью.</span><span class="sxs-lookup"><span data-stu-id="07995-109">Manage memory.</span></span>
    
- <span data-ttu-id="07995-110">Обработка подсчета ссылок.</span><span class="sxs-lookup"><span data-stu-id="07995-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="07995-111">Реализуйте объекты с апартаментными потоками.</span><span class="sxs-lookup"><span data-stu-id="07995-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="07995-112">Несмотря на то, что все объекты MAPI считаются основанными на COM, так как они реализуют интерфейсы, наследующие от [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI-отклонения в некоторых ситуациях от стандартных правил com.</span><span class="sxs-lookup"><span data-stu-id="07995-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="07995-113">Это отклонение позволяет разработчикам больше гибкости в реализациях.</span><span class="sxs-lookup"><span data-stu-id="07995-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="07995-114">Например, интерфейс MAPI, как и любой COM-интерфейс, описывает контракт между разработчиком и вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="07995-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="07995-115">После создания и публикации интерфейса его определение не может и не изменится.</span><span class="sxs-lookup"><span data-stu-id="07995-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="07995-116">В этом описании MAPI не имеет отклонения, но он может быть недоступен.</span><span class="sxs-lookup"><span data-stu-id="07995-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="07995-117">Разработчики могут отказаться от реализации определенных методов, возвращая одно из следующих значений ошибки вызывающему абоненту:</span><span class="sxs-lookup"><span data-stu-id="07995-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="07995-118">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="07995-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="07995-119">МАПИ_Е_ТУ_КОМПЛЕКС</span><span class="sxs-lookup"><span data-stu-id="07995-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="07995-120">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="07995-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="07995-121">МАПИ_Е_ТИПЕ_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="07995-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="07995-122">Другие отклонения от стандартных правил COM описаны в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="07995-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="07995-123">**Правило программирования COM**</span><span class="sxs-lookup"><span data-stu-id="07995-123">**COM programming rule**</span></span>|<span data-ttu-id="07995-124">**Вариант MAPI**</span><span class="sxs-lookup"><span data-stu-id="07995-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07995-125">Все строковые параметры в методах интерфейса должны иметь формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="07995-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="07995-126">Интерфейсы MAPI определяют, чтобы разрешить строковые параметры Юникода или ANSI.</span><span class="sxs-lookup"><span data-stu-id="07995-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="07995-127">Многие методы, у которых есть строковый параметр, также имеют параметр **ulFlags** ; Ширина строкового параметра указывается значением флага МАПИ_УНИКОДЕ в **ulFlags**.</span><span class="sxs-lookup"><span data-stu-id="07995-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="07995-128">Некоторые интерфейсы MAPI не поддерживают Юникод и не возвращают МАПИ_Е_БАД_ЧАРВИДС, если установлен флаг МАПИ_УНИКОДЕ.</span><span class="sxs-lookup"><span data-stu-id="07995-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="07995-129">Все методы интерфейса должны иметь тип возвращаемого значения HRESULT.</span><span class="sxs-lookup"><span data-stu-id="07995-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="07995-130">В MAPI есть по крайней мере один метод, который возвращает значение, отличное от HRESULT: [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="07995-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="07995-131">Вызывающим объектам и разработчикам следует выделить и освободить память для параметров интерфейса с помощью стандартных механизмами выделения задач COM.</span><span class="sxs-lookup"><span data-stu-id="07995-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="07995-132">Все методы MAPI используют связанные распределителя памяти [мапиаллокатебуффер](mapiallocatebuffer.md), [мапиаллокатеморе](mapiallocatemore.md)и [мапифрибуффер](mapifreebuffer.md) для управления памятью для параметров интерфейса.</span><span class="sxs-lookup"><span data-stu-id="07995-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="07995-133">Все реализации MAPI интерфейсов, определенных в OLE, например [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), используют стандартные распределителя памяти для задач COM.</span><span class="sxs-lookup"><span data-stu-id="07995-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="07995-134">Все параметры указателя должны явно иметь значение NULL, если метод завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="07995-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="07995-135">Для интерфейсов MAPI необходимо, чтобы для параметров указателя out было задано значение NULL или не было изменено при сбое метода.</span><span class="sxs-lookup"><span data-stu-id="07995-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="07995-136">Все реализации MAPI интерфейсов, определенные в OLE, явно задают для параметров out значение NULL в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="07995-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="07995-137">Реализуйте статистические объекты везде, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="07995-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="07995-138">Интерфейсы MAPI не поддерживают статистическую обработку.</span><span class="sxs-lookup"><span data-stu-id="07995-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07995-139">См. также</span><span class="sxs-lookup"><span data-stu-id="07995-139">See also</span></span>



[<span data-ttu-id="07995-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="07995-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="07995-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="07995-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="07995-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="07995-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="07995-143">Общие сведения об объекте и интерфейсе MAPI</span><span class="sxs-lookup"><span data-stu-id="07995-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

