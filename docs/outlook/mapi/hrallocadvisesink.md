---
title: HrAllocAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrAllocAdviseSink
api_type:
- HeaderDef
ms.assetid: 1dd460e6-ce95-4fef-bb5e-8d778c9716d5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7f9873fe8e1825c68d4540cc1d093171e9f95727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428902"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="11872-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="11872-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="11872-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11872-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11872-105">Создает объект раковины рекомендации, учитывая контекст, заданный реализацией вызовов и функцией вызова, которая будет вызвана уведомлением события.</span><span class="sxs-lookup"><span data-stu-id="11872-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11872-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="11872-106">Header file:</span></span>  <br/> |<span data-ttu-id="11872-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="11872-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="11872-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="11872-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="11872-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="11872-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="11872-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="11872-110">Called by:</span></span>  <br/> |<span data-ttu-id="11872-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="11872-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="11872-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="11872-112">Parameters</span></span>

 <span data-ttu-id="11872-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="11872-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="11872-114">[in] Указатель на функцию вызова на основе прототипа [NOTIFCALLBACK,](notifcallback.md) который MAPI должен вызывать при событии уведомления для вновь созданной раковины рекомендации.</span><span class="sxs-lookup"><span data-stu-id="11872-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="11872-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="11872-115">_lpvContext_</span></span>
  
> <span data-ttu-id="11872-116">[in] Указатель на данные вызываемого звонка, переданные функции вызова при вызове MAPI.</span><span class="sxs-lookup"><span data-stu-id="11872-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="11872-117">Данные вызываемого клиента могут представлять адрес, который имеет значение для клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="11872-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="11872-118">Как правило, для кода C++ параметр  _lpvContext_ представляет указатель на адрес объекта.</span><span class="sxs-lookup"><span data-stu-id="11872-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="11872-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="11872-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="11872-120">[вышел] Указатель на указатель на объект раковины рекомендации.</span><span class="sxs-lookup"><span data-stu-id="11872-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="11872-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11872-121">Return value</span></span>

<span data-ttu-id="11872-122">Нет.</span><span class="sxs-lookup"><span data-stu-id="11872-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="11872-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="11872-123">Remarks</span></span>

<span data-ttu-id="11872-124">Чтобы использовать функцию **HrAllocAdviseSink,** клиентский приложение или поставщик услуг создает объект для получения уведомлений, создает функцию вызова уведомлений на основе прототипа функции [NOTIFCALLBACK,](notifcallback.md) который идет с этим объектом, и передает указатель на объект в функции **HrAllocAdviseSink** в качестве _значения lpvContext._</span><span class="sxs-lookup"><span data-stu-id="11872-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="11872-125">При этом выполняется уведомление; и в рамках процесса уведомления MAPI вызывает функцию вызова с указателем объекта в качестве контекста.</span><span class="sxs-lookup"><span data-stu-id="11872-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="11872-126">MAPI асинхронно реализует свой двигатель уведомлений.</span><span class="sxs-lookup"><span data-stu-id="11872-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="11872-127">В C++вызов уведомлений может быть объектным методом.</span><span class="sxs-lookup"><span data-stu-id="11872-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="11872-128">Если объект, генерирующий уведомление, не присутствует, клиент или поставщик, запрашивающий уведомление, должен иметь отдельный справочный номер для этого объекта для раковины рекомендации объекта.</span><span class="sxs-lookup"><span data-stu-id="11872-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="11872-129">**HrAllocAdviseSink** следует использовать экономно; клиентам безопаснее создавать собственные раковины для консультирования.</span><span class="sxs-lookup"><span data-stu-id="11872-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

