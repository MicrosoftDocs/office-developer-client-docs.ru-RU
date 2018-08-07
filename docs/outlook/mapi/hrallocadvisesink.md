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
ms.openlocfilehash: 5a5e736e8be1120f5fb90048f01fdc8a44479060
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808649"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="51088-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="51088-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="51088-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="51088-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="51088-105">Создает объект приемника уведомлений, задавая контекст, указанного идентификатором вызывающего реализации и функции обратного вызова, чтобы инициировать, уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="51088-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51088-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="51088-106">Header file:</span></span>  <br/> |<span data-ttu-id="51088-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="51088-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="51088-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="51088-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="51088-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="51088-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="51088-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="51088-110">Called by:</span></span>  <br/> |<span data-ttu-id="51088-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="51088-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="51088-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="51088-112">Parameters</span></span>

 <span data-ttu-id="51088-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="51088-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="51088-114">[in] Указатель на функцию обратного вызова, на основании прототип [NOTIFCALLBACK](notifcallback.md) , который будет вызываться при возникновении события уведомления для только что созданный является MAPI уведомить приемника.</span><span class="sxs-lookup"><span data-stu-id="51088-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="51088-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="51088-115">_lpvContext_</span></span>
  
> <span data-ttu-id="51088-116">[in] Указатель на данные вызывающего передается функции обратного вызова, когда она вызывается средствами MAPI.</span><span class="sxs-lookup"><span data-stu-id="51088-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="51088-117">Вызывающий объект данных может представлять адрес значение для клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="51088-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="51088-118">Обычно для кода C++ параметр _lpvContext_ представляет указатель на адрес объекта.</span><span class="sxs-lookup"><span data-stu-id="51088-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="51088-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="51088-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="51088-120">[out] Указатель на указатель на объект приемник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="51088-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="51088-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51088-121">Return value</span></span>

<span data-ttu-id="51088-122">Нет.</span><span class="sxs-lookup"><span data-stu-id="51088-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="51088-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="51088-123">Remarks</span></span>

<span data-ttu-id="51088-124">Использовать функцию **HrAllocAdviseSink** , клиентское приложение или поставщик услуг создает объекта, который будет получать уведомления, создает функцию обратного вызова уведомления на основании прототипа функции [NOTIFCALLBACK](notifcallback.md) , что происходит с помощью этого объекта и передает указатель на объект функции **HrAllocAdviseSink** , что значение _lpvContext_ .</span><span class="sxs-lookup"><span data-stu-id="51088-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="51088-125">Таким образом выполняется уведомления; и в ходе процесса уведомления MAPI вызывает функцию обратного вызова с помощью указателя на объект контекста.</span><span class="sxs-lookup"><span data-stu-id="51088-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="51088-126">MAPI асинхронно реализует его обработчиком уведомлений.</span><span class="sxs-lookup"><span data-stu-id="51088-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="51088-127">В C++ обратного вызова для уведомления может быть метода объекта.</span><span class="sxs-lookup"><span data-stu-id="51088-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="51088-128">Если объект, создание уведомления не представить, клиента или поставщика, запрос уведомлений о необходимо поддерживать количество отдельных ссылку для этого объекта для объектов уведомить приемника.</span><span class="sxs-lookup"><span data-stu-id="51088-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="51088-129">**HrAllocAdviseSink** следует использовать с осторожностью; он является более безопасным для клиентов создать собственные приемники уведомлений.</span><span class="sxs-lookup"><span data-stu-id="51088-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

