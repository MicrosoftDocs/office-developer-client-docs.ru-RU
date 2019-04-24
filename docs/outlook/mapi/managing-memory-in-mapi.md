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
# <a name="managing-memory-in-mapi"></a><span data-ttu-id="832df-103">Управление памятью в MAPI</span><span class="sxs-lookup"><span data-stu-id="832df-103">Managing Memory in MAPI</span></span>

  
  
<span data-ttu-id="832df-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="832df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="832df-105">Знание того, как и когда следует распределять и освобождать память, является важной частью программирования с использованием MAPI.</span><span class="sxs-lookup"><span data-stu-id="832df-105">Knowing how and when to allocate and free memory is an important part of programming with MAPI.</span></span> <span data-ttu-id="832df-106">MAPI предоставляет функции и макросы, которые может использовать клиент или поставщик услуг для согласованного управления памятью.</span><span class="sxs-lookup"><span data-stu-id="832df-106">MAPI provides both functions and macros that your client or service provider can use to manage memory in a consistent way.</span></span> <span data-ttu-id="832df-107">Существуют следующие три функции:</span><span class="sxs-lookup"><span data-stu-id="832df-107">The three functions are as follows:</span></span>
  
[<span data-ttu-id="832df-108">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="832df-108">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="832df-109">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="832df-109">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="832df-110">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="832df-110">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
<span data-ttu-id="832df-111">Когда клиенты и поставщики услуг используют эти функции, выдается вопрос о том, что "владеет" (то есть, как выпустить, что устраняет определенный блок памяти).</span><span class="sxs-lookup"><span data-stu-id="832df-111">When clients and service providers use these functions, the issue of who "owns" — that is, knows how to release — a particular block of memory is eliminated.</span></span> <span data-ttu-id="832df-112">Клиент, вызывающий метод поставщика услуг, не должен передавать буфер достаточно большим для хранения возвращаемого значения любого размера.</span><span class="sxs-lookup"><span data-stu-id="832df-112">A client calling a service provider method need not pass a buffer large enough to hold a return value of any size.</span></span> <span data-ttu-id="832df-113">Поставщик услуг может просто выделить соответствующий объем памяти с помощью **мапиаллокатебуффер** и, при необходимости, **мапиаллокатеморе**, а затем клиент может позже отпустить его, используя **мапифрибуффер**, не зависящее от службы. поставщики.</span><span class="sxs-lookup"><span data-stu-id="832df-113">The service provider can simply allocate the appropriate amount of memory using **MAPIAllocateBuffer** and, if necessary, **MAPIAllocateMore**, and the client can later release it at will using **MAPIFreeBuffer**, independent of the service provider.</span></span> 
  
<span data-ttu-id="832df-114">Макросы памяти используются для выделения структур или массивов структуры определенного размера.</span><span class="sxs-lookup"><span data-stu-id="832df-114">The memory macros are used to allocate structures or arrays of structures of a specific size.</span></span> <span data-ttu-id="832df-115">Клиенты и поставщики услуг должны использовать эти макросы вместо того, чтобы выделить память вручную.</span><span class="sxs-lookup"><span data-stu-id="832df-115">Clients and service providers should use these macros rather than allocate the memory manually.</span></span> <span data-ttu-id="832df-116">Например, если клиенту требуется выполнить обработку разрешения имен для списка получателей с тремя записями, макрос **сизедадрлист** можно использовать для создания структуры **ADRLIST** , которая передается в **IAddrBook:: ресолвенаме** с правильным числом Элементы **адрентри** .</span><span class="sxs-lookup"><span data-stu-id="832df-116">For example, if a client needs to perform name resolution processing on a recipient list with three entries, the **SizedADRLIST** macro can be used to create an **ADRLIST** structure to pass to **IAddrBook::ResolveName** with the correct number of **ADRENTRY** members.</span></span> <span data-ttu-id="832df-117">Все макросы памяти определены в MAPIDEFS. H файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="832df-117">All of the memory macros are defined in the MAPIDEFS.H header file.</span></span> <span data-ttu-id="832df-118">Эти макросы:</span><span class="sxs-lookup"><span data-stu-id="832df-118">These macros are:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="832df-119">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="832df-119">SizedADRLIST</span></span>](sizedadrlist.md) <br/> |[<span data-ttu-id="832df-120">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="832df-120">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
|[<span data-ttu-id="832df-121">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="832df-121">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |[<span data-ttu-id="832df-122">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="832df-122">SizedENTRYID</span></span>](sizedentryid.md) <br/> |
|[<span data-ttu-id="832df-123">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="832df-123">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |[<span data-ttu-id="832df-124">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="832df-124">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
|[<span data-ttu-id="832df-125">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="832df-125">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |[<span data-ttu-id="832df-126">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="832df-126">SizedSPropTagArray</span></span>](sizedsproptagarray.md) <br/> |
|[<span data-ttu-id="832df-127">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="832df-127">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |[<span data-ttu-id="832df-128">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="832df-128">SizedSRowSet</span></span>](sizedsrowset.md) <br/> |
|[<span data-ttu-id="832df-129">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="832df-129">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |[<span data-ttu-id="832df-130">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="832df-130">SizedSSortOrderSet</span></span>](sizedssortorderset.md) <br/> |
|[<span data-ttu-id="832df-131">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="832df-131">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> | <br/> |
   
<span data-ttu-id="832df-132">MAPI также поддерживает использование интерфейса COM для управления памятью. [](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="832df-132">MAPI also supports the use of the COM interface [IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) for memory management.</span></span> <span data-ttu-id="832df-133">Поставщику услуг во время \*\*\*\* инициализации получится указатель интерфейса исходящей информации, а также можно получить один из них с помощью функции [мапижетдефаултмаллок](mapigetdefaultmalloc.md) .</span><span class="sxs-lookup"><span data-stu-id="832df-133">Service providers are given an **IMalloc** interface pointer by MAPI at initialization time and can also retrieve one through the [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) function.</span></span> <span data-ttu-id="832df-134">Основное преимущество использования методов unalloc \*\*\*\* для управления памятью через функции MAPI заключается в том, что методы COM могут перераспределить существующий буфер.</span><span class="sxs-lookup"><span data-stu-id="832df-134">The main advantage to using the **IMalloc** methods for managing memory over the MAPI functions is that with the COM methods it is possible to reallocate an existing buffer.</span></span> <span data-ttu-id="832df-135">Функции памяти MAPI не поддерживают перераспределение.</span><span class="sxs-lookup"><span data-stu-id="832df-135">The MAPI memory functions do not support reallocation.</span></span> 
  

