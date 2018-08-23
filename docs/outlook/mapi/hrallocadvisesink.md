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
ms.openlocfilehash: d5cb43bfa3acd912e397644657223c177d6afb30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589324"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="96a29-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="96a29-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="96a29-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96a29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96a29-105">Создает объект приемника уведомлений, задавая контекст, указанного идентификатором вызывающего реализации и функции обратного вызова, чтобы инициировать, уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="96a29-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96a29-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="96a29-106">Header file:</span></span>  <br/> |<span data-ttu-id="96a29-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="96a29-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="96a29-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="96a29-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="96a29-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="96a29-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="96a29-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="96a29-110">Called by:</span></span>  <br/> |<span data-ttu-id="96a29-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="96a29-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="96a29-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="96a29-112">Parameters</span></span>

 <span data-ttu-id="96a29-113">_lpfnCallback_</span><span class="sxs-lookup"><span data-stu-id="96a29-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="96a29-114">[in] Указатель на функцию обратного вызова, на основании прототип [NOTIFCALLBACK](notifcallback.md) , который будет вызываться при возникновении события уведомления для только что созданный является MAPI уведомить приемника.</span><span class="sxs-lookup"><span data-stu-id="96a29-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="96a29-115">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="96a29-115">_lpvContext_</span></span>
  
> <span data-ttu-id="96a29-116">[in] Указатель на данные вызывающего передается функции обратного вызова, когда она вызывается средствами MAPI.</span><span class="sxs-lookup"><span data-stu-id="96a29-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="96a29-117">Вызывающий объект данных может представлять адрес значение для клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="96a29-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="96a29-118">Обычно для кода C++ параметр _lpvContext_ представляет указатель на адрес объекта.</span><span class="sxs-lookup"><span data-stu-id="96a29-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="96a29-119">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="96a29-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="96a29-120">[out] Указатель на указатель на объект приемник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="96a29-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="96a29-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96a29-121">Return value</span></span>

<span data-ttu-id="96a29-122">Нет.</span><span class="sxs-lookup"><span data-stu-id="96a29-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="96a29-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="96a29-123">Remarks</span></span>

<span data-ttu-id="96a29-124">Использовать функцию **HrAllocAdviseSink** , клиентское приложение или поставщик услуг создает объекта, который будет получать уведомления, создает функцию обратного вызова уведомления на основании прототипа функции [NOTIFCALLBACK](notifcallback.md) , что происходит с помощью этого объекта и передает указатель на объект функции **HrAllocAdviseSink** , что значение _lpvContext_ .</span><span class="sxs-lookup"><span data-stu-id="96a29-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="96a29-125">Таким образом выполняется уведомления; и в ходе процесса уведомления MAPI вызывает функцию обратного вызова с помощью указателя на объект контекста.</span><span class="sxs-lookup"><span data-stu-id="96a29-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="96a29-126">MAPI асинхронно реализует его обработчиком уведомлений.</span><span class="sxs-lookup"><span data-stu-id="96a29-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="96a29-127">В C++ обратного вызова для уведомления может быть метода объекта.</span><span class="sxs-lookup"><span data-stu-id="96a29-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="96a29-128">Если объект, создание уведомления не представить, клиента или поставщика, запрос уведомлений о необходимо поддерживать количество отдельных ссылку для этого объекта для объектов уведомить приемника.</span><span class="sxs-lookup"><span data-stu-id="96a29-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="96a29-129">**HrAllocAdviseSink** следует использовать с осторожностью; он является более безопасным для клиентов создать собственные приемники уведомлений.</span><span class="sxs-lookup"><span data-stu-id="96a29-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

