---
title: Управление памятью в MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 66489c09be641d8fe9ae5f3ffff46a6d5004f473
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298098"
---
# <a name="managing-memory-in-mapi"></a><span data-ttu-id="2bb5d-103">Управление памятью в MAPI</span><span class="sxs-lookup"><span data-stu-id="2bb5d-103">Managing Memory in MAPI</span></span>

  
  
<span data-ttu-id="2bb5d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2bb5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2bb5d-105">Знание того, как и когда распределять и выделять свободную память, является важной частью программирования с помощью MAPI.</span><span class="sxs-lookup"><span data-stu-id="2bb5d-105">Knowing how and when to allocate and free memory is an important part of programming with MAPI.</span></span> <span data-ttu-id="2bb5d-106">MAPI предоставляет функции и макрос, которые клиент или поставщик услуг может использовать для последовательного управления памятью.</span><span class="sxs-lookup"><span data-stu-id="2bb5d-106">MAPI provides both functions and macros that your client or service provider can use to manage memory in a consistent way.</span></span> <span data-ttu-id="2bb5d-107">Эти три функции следуют следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2bb5d-107">The three functions are as follows:</span></span>
  
[<span data-ttu-id="2bb5d-108">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="2bb5d-108">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="2bb5d-109">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="2bb5d-109">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="2bb5d-110">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2bb5d-110">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
<span data-ttu-id="2bb5d-111">Когда клиенты и поставщики услуг используют эти функции, устраняется вопрос о том, кто "владеет", то есть знает, как освободиться, — определенный блок памяти.</span><span class="sxs-lookup"><span data-stu-id="2bb5d-111">When clients and service providers use these functions, the issue of who "owns" — that is, knows how to release — a particular block of memory is eliminated.</span></span> <span data-ttu-id="2bb5d-112">Клиенту, вызываемому методу поставщика услуг, не нужно проходить достаточно большой буфер для удержания значения возврата любого размера.</span><span class="sxs-lookup"><span data-stu-id="2bb5d-112">A client calling a service provider method need not pass a buffer large enough to hold a return value of any size.</span></span> <span data-ttu-id="2bb5d-113">Поставщик служб может просто выделить соответствующее количество памяти с помощью **MAPIAllocateBuffer** и, при необходимости, **MAPIAllocateMore,** и клиент может позже выпустить ее по завеству с помощью **MAPIFreeBuffer,** независимо от поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="2bb5d-113">The service provider can simply allocate the appropriate amount of memory using **MAPIAllocateBuffer** and, if necessary, **MAPIAllocateMore**, and the client can later release it at will using **MAPIFreeBuffer**, independent of the service provider.</span></span> 
  
<span data-ttu-id="2bb5d-114">Макрос памяти используется для выделения структур или массивов структур определенного размера.</span><span class="sxs-lookup"><span data-stu-id="2bb5d-114">The memory macros are used to allocate structures or arrays of structures of a specific size.</span></span> <span data-ttu-id="2bb5d-115">Клиенты и поставщики услуг должны использовать эти макрос, а не распределять память вручную.</span><span class="sxs-lookup"><span data-stu-id="2bb5d-115">Clients and service providers should use these macros rather than allocate the memory manually.</span></span> <span data-ttu-id="2bb5d-116">Например, если клиенту необходимо выполнить обработку разрешения имен в списке получателей с тремя записями, макрос **SizedADRLIST** можно использовать для создания структуры **ADRLIST,** чтобы передать **В IAddrBook::ResolveName** с правильным числом **участников ADRENTRY.**</span><span class="sxs-lookup"><span data-stu-id="2bb5d-116">For example, if a client needs to perform name resolution processing on a recipient list with three entries, the **SizedADRLIST** macro can be used to create an **ADRLIST** structure to pass to **IAddrBook::ResolveName** with the correct number of **ADRENTRY** members.</span></span> <span data-ttu-id="2bb5d-117">Все макрос памяти определяются в MAPIDEFS. Файл заглавной папки H.</span><span class="sxs-lookup"><span data-stu-id="2bb5d-117">All of the memory macros are defined in the MAPIDEFS.H header file.</span></span> <span data-ttu-id="2bb5d-118">Эти макрос:</span><span class="sxs-lookup"><span data-stu-id="2bb5d-118">These macros are:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="2bb5d-119">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="2bb5d-119">SizedADRLIST</span></span>](sizedadrlist.md) <br/> |[<span data-ttu-id="2bb5d-120">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="2bb5d-120">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
|[<span data-ttu-id="2bb5d-121">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="2bb5d-121">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |[<span data-ttu-id="2bb5d-122">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="2bb5d-122">SizedENTRYID</span></span>](sizedentryid.md) <br/> |
|[<span data-ttu-id="2bb5d-123">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="2bb5d-123">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |[<span data-ttu-id="2bb5d-124">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="2bb5d-124">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
|[<span data-ttu-id="2bb5d-125">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="2bb5d-125">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |[<span data-ttu-id="2bb5d-126">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="2bb5d-126">SizedSPropTagArray</span></span>](sizedsproptagarray.md) <br/> |
|[<span data-ttu-id="2bb5d-127">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="2bb5d-127">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |[<span data-ttu-id="2bb5d-128">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="2bb5d-128">SizedSRowSet</span></span>](sizedsrowset.md) <br/> |
|[<span data-ttu-id="2bb5d-129">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="2bb5d-129">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |[<span data-ttu-id="2bb5d-130">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="2bb5d-130">SizedSSortOrderSet</span></span>](sizedssortorderset.md) <br/> |
|[<span data-ttu-id="2bb5d-131">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="2bb5d-131">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> | <br/> |
   
<span data-ttu-id="2bb5d-132">MAPI также поддерживает использование интерфейса [COM IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) для управления памятью.</span><span class="sxs-lookup"><span data-stu-id="2bb5d-132">MAPI also supports the use of the COM interface [IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) for memory management.</span></span> <span data-ttu-id="2bb5d-133">Поставщики услуг получили указатель **интерфейса IMalloc** по MAPI во время инициализации и могут также получить его с помощью [функции MAPIGetDefaultMalloc.](mapigetdefaultmalloc.md)</span><span class="sxs-lookup"><span data-stu-id="2bb5d-133">Service providers are given an **IMalloc** interface pointer by MAPI at initialization time and can also retrieve one through the [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) function.</span></span> <span data-ttu-id="2bb5d-134">Основное преимущество использования методов **IMalloc** для управления памятью над функциями MAPI заключается в том, что с помощью методов COM можно перенаправить существующий буфер.</span><span class="sxs-lookup"><span data-stu-id="2bb5d-134">The main advantage to using the **IMalloc** methods for managing memory over the MAPI functions is that with the COM methods it is possible to reallocate an existing buffer.</span></span> <span data-ttu-id="2bb5d-135">Функции памяти MAPI не поддерживают перераспределение.</span><span class="sxs-lookup"><span data-stu-id="2bb5d-135">The MAPI memory functions do not support reallocation.</span></span> 
  

