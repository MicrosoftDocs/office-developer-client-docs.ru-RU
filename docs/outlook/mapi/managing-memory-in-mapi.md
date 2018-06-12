---
title: Управление памятью в MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 5859d94f85ca3fe7a0c738ed596d3c1a11fb2e8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809670"
---
# <a name="managing-memory-in-mapi"></a><span data-ttu-id="e603d-103">Управление памятью в MAPI</span><span class="sxs-lookup"><span data-stu-id="e603d-103">Managing Memory in MAPI</span></span>

  
  
<span data-ttu-id="e603d-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e603d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e603d-105">Знать, как и когда для размещения и освободить память является важной частью программирования с использованием MAPI.</span><span class="sxs-lookup"><span data-stu-id="e603d-105">Knowing how and when to allocate and free memory is an important part of programming with MAPI.</span></span> <span data-ttu-id="e603d-106">MAPI предоставляет функции и макросы, которые ваш поставщик клиента или службы можно использовать для управления памяти в едином виде.</span><span class="sxs-lookup"><span data-stu-id="e603d-106">MAPI provides both functions and macros that your client or service provider can use to manage memory in a consistent way.</span></span> <span data-ttu-id="e603d-107">Три функции, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="e603d-107">The three functions are as follows:</span></span>
  
[<span data-ttu-id="e603d-108">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e603d-108">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="e603d-109">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="e603d-109">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="e603d-110">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e603d-110">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
<span data-ttu-id="e603d-111">Когда использовать эти функции проблемы клиентов и поставщиков услуг из «владельца» — то есть, знает, как освободить — устранены определенный блок памяти.</span><span class="sxs-lookup"><span data-stu-id="e603d-111">When clients and service providers use these functions, the issue of who "owns" — that is, knows how to release — a particular block of memory is eliminated.</span></span> <span data-ttu-id="e603d-112">Клиента, вызывающего метод поставщика службы не нужно передавать буфера, достаточное для хранения возвращаемого значения любого размера.</span><span class="sxs-lookup"><span data-stu-id="e603d-112">A client calling a service provider method need not pass a buffer large enough to hold a return value of any size.</span></span> <span data-ttu-id="e603d-113">Поставщик услуг просто можно выделить соответствующий объем памяти, с помощью **MAPIAllocateBuffer** и, при необходимости, **MAPIAllocateMore**и клиента можно более поздней версии выпуска его на использование **MAPIFreeBuffer**, вне зависимости от службы будут Поставщик.</span><span class="sxs-lookup"><span data-stu-id="e603d-113">The service provider can simply allocate the appropriate amount of memory using **MAPIAllocateBuffer** and, if necessary, **MAPIAllocateMore**, and the client can later release it at will using **MAPIFreeBuffer**, independent of the service provider.</span></span> 
  
<span data-ttu-id="e603d-114">Макросы памяти используются для распределения структур или массивов структур определенного размера.</span><span class="sxs-lookup"><span data-stu-id="e603d-114">The memory macros are used to allocate structures or arrays of structures of a specific size.</span></span> <span data-ttu-id="e603d-115">Клиенты и поставщиков услуг должен использовать эти макросы, а не вручную выделить память.</span><span class="sxs-lookup"><span data-stu-id="e603d-115">Clients and service providers should use these macros rather than allocate the memory manually.</span></span> <span data-ttu-id="e603d-116">Например если клиент должен выполнять разрешение имен обработки в список получателей с тремя записями, макрос **SizedADRLIST** можно использовать для создание структуры **ADRLIST** для передачи **IAddrBook::ResolveName** с правильным числом Члены **ADRENTRY** .</span><span class="sxs-lookup"><span data-stu-id="e603d-116">For example, if a client needs to perform name resolution processing on a recipient list with three entries, the **SizedADRLIST** macro can be used to create an **ADRLIST** structure to pass to **IAddrBook::ResolveName** with the correct number of **ADRENTRY** members.</span></span> <span data-ttu-id="e603d-117">Все макросы памяти определены в MAPIDEFS. Файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="e603d-117">All of the memory macros are defined in the MAPIDEFS.H header file.</span></span> <span data-ttu-id="e603d-118">Эти макросы являются:</span><span class="sxs-lookup"><span data-stu-id="e603d-118">These macros are:</span></span> 
  
|||
|:-----|:-----|
|[<span data-ttu-id="e603d-119">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="e603d-119">SizedADRLIST</span></span>](sizedadrlist.md) <br/> |[<span data-ttu-id="e603d-120">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="e603d-120">SizedDtblPage</span></span>](sizeddtblpage.md) <br/> |
|[<span data-ttu-id="e603d-121">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="e603d-121">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |[<span data-ttu-id="e603d-122">SizedENTRYID</span><span class="sxs-lookup"><span data-stu-id="e603d-122">SizedENTRYID</span></span>](sizedentryid.md) <br/> |
|[<span data-ttu-id="e603d-123">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="e603d-123">SizedDtblCheckBox</span></span>](sizeddtblcheckbox.md) <br/> |[<span data-ttu-id="e603d-124">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="e603d-124">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
|[<span data-ttu-id="e603d-125">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="e603d-125">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |[<span data-ttu-id="e603d-126">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="e603d-126">SizedSPropTagArray</span></span>](sizedsproptagarray.md) <br/> |
|[<span data-ttu-id="e603d-127">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="e603d-127">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |[<span data-ttu-id="e603d-128">SizedSRowSet</span><span class="sxs-lookup"><span data-stu-id="e603d-128">SizedSRowSet</span></span>](sizedsrowset.md) <br/> |
|[<span data-ttu-id="e603d-129">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="e603d-129">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |[<span data-ttu-id="e603d-130">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="e603d-130">SizedSSortOrderSet</span></span>](sizedssortorderset.md) <br/> |
|[<span data-ttu-id="e603d-131">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="e603d-131">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> | <br/> |
   
<span data-ttu-id="e603d-132">Использование интерфейса COM [IMalloc](http://msdn.microsoft.com/en-us/library/ms678425%28VS.85%29.aspx) также поддерживает MAPI для управления памятью.</span><span class="sxs-lookup"><span data-stu-id="e603d-132">MAPI also supports the use of the COM interface [IMalloc](http://msdn.microsoft.com/en-us/library/ms678425%28VS.85%29.aspx) for memory management.</span></span> <span data-ttu-id="e603d-133">Поставщики услуг назначается указатель интерфейса **IMalloc** с MAPI во время инициализации, а также можно получить от 1 до [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) функции.</span><span class="sxs-lookup"><span data-stu-id="e603d-133">Service providers are given an **IMalloc** interface pointer by MAPI at initialization time and can also retrieve one through the [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) function.</span></span> <span data-ttu-id="e603d-134">Основное преимущество с помощью методов **IMalloc** для управления памяти функции MAPI — это, что с методами COM можно перемещать существующий буфер.</span><span class="sxs-lookup"><span data-stu-id="e603d-134">The main advantage to using the **IMalloc** methods for managing memory over the MAPI functions is that with the COM methods it is possible to reallocate an existing buffer.</span></span> <span data-ttu-id="e603d-135">Функции памяти MAPI не поддерживают перераспределения.</span><span class="sxs-lookup"><span data-stu-id="e603d-135">The MAPI memory functions do not support reallocation.</span></span> 
  

