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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348218"
---
# <a name="hrallocadvisesink"></a><span data-ttu-id="cfe5e-103">HrAllocAdviseSink</span><span class="sxs-lookup"><span data-stu-id="cfe5e-103">HrAllocAdviseSink</span></span>

  
  
<span data-ttu-id="cfe5e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cfe5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cfe5e-105">Создает объект приемника уведомлений, задавая контекст, заданный вызывающей реализацией, и функцию обратного вызова, которая вызывается уведомлением о событии.</span><span class="sxs-lookup"><span data-stu-id="cfe5e-105">Creates an advise sink object, given a context specified by the calling implementation and a callback function to be triggered by an event notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cfe5e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="cfe5e-106">Header file:</span></span>  <br/> |<span data-ttu-id="cfe5e-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="cfe5e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="cfe5e-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="cfe5e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cfe5e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cfe5e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cfe5e-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="cfe5e-110">Called by:</span></span>  <br/> |<span data-ttu-id="cfe5e-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="cfe5e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDAPI HrAllocAdviseSink(
  LPNOTIFCALLBACK lpfnCallback,
  LPVOID lpvContext,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="cfe5e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfe5e-112">Parameters</span></span>

 <span data-ttu-id="cfe5e-113">_Лпфнкаллбакк_</span><span class="sxs-lookup"><span data-stu-id="cfe5e-113">_lpfnCallback_</span></span>
  
> <span data-ttu-id="cfe5e-114">возврата Указатель на функцию обратного вызова, основанную на прототипе [нотифкаллбакк](notifcallback.md) , который вызывается MAPI при возникновении события уведомления для вновь созданного приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="cfe5e-114">[in] Pointer to a callback function based on the [NOTIFCALLBACK](notifcallback.md) prototype that MAPI is to call when a notification event occurs for the newly created advise sink.</span></span> 
    
 <span data-ttu-id="cfe5e-115">_Лпвконтекст_</span><span class="sxs-lookup"><span data-stu-id="cfe5e-115">_lpvContext_</span></span>
  
> <span data-ttu-id="cfe5e-116">возврата Указатель на абонентские данные, передаваемые в функцию обратного вызова, когда она вызывается MAPI.</span><span class="sxs-lookup"><span data-stu-id="cfe5e-116">[in] Pointer to caller data passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="cfe5e-117">Данные звонящего могут представлять адрес важности для клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="cfe5e-117">The caller data can represent an address of significance to the client or provider.</span></span> <span data-ttu-id="cfe5e-118">Как правило, для кода C++ параметр _лпвконтекст_ представляет указатель на адрес объекта.</span><span class="sxs-lookup"><span data-stu-id="cfe5e-118">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to the address of an object.</span></span> 
    
 <span data-ttu-id="cfe5e-119">_Лппадвисесинк_</span><span class="sxs-lookup"><span data-stu-id="cfe5e-119">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="cfe5e-120">вышли Указатель на указатель на объект приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="cfe5e-120">[out] Pointer to a pointer to an advise sink object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cfe5e-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cfe5e-121">Return value</span></span>

<span data-ttu-id="cfe5e-122">Нет.</span><span class="sxs-lookup"><span data-stu-id="cfe5e-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cfe5e-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="cfe5e-123">Remarks</span></span>

<span data-ttu-id="cfe5e-124">Чтобы использовать функцию **храллокадвисесинк** , клиентское приложение или поставщик услуг создает объект для получения уведомлений, создает функцию обратного вызова уведомления на основе прототипа функции [нотифкаллбакк](notifcallback.md) , который передается с этим объектом. и передает указатель на объект в функции **храллокадвисесинк** в качестве значения _лпвконтекст_ .</span><span class="sxs-lookup"><span data-stu-id="cfe5e-124">To use the **HrAllocAdviseSink** function, a client application or service provider creates an object to receive notifications, creates a notification callback function based on the [NOTIFCALLBACK](notifcallback.md) function prototype that goes with that object, and passes a pointer to the object in the **HrAllocAdviseSink** function as the  _lpvContext_ value.</span></span> <span data-ttu-id="cfe5e-125">При этом выполняется уведомление; в рамках процесса уведомления MAPI вызывает функцию обратного вызова с указателем объекта в качестве контекста.</span><span class="sxs-lookup"><span data-stu-id="cfe5e-125">Doing so performs a notification; and as part of the notification process, MAPI calls the callback function with the object pointer as the context.</span></span> 
  
<span data-ttu-id="cfe5e-126">MAPI асинхронно реализует обработчик уведомлений.</span><span class="sxs-lookup"><span data-stu-id="cfe5e-126">MAPI implements its notification engine asynchronously.</span></span> <span data-ttu-id="cfe5e-127">В C++ обратный вызов уведомления может быть методом объекта.</span><span class="sxs-lookup"><span data-stu-id="cfe5e-127">In C++, the notification callback can be an object method.</span></span> <span data-ttu-id="cfe5e-128">Если объект, создающий уведомление, отсутствует, то клиент или поставщик, запрашивающий уведомление, должен хранить отдельный счетчик ссылок для этого объекта в приемнике уведомлений объекта.</span><span class="sxs-lookup"><span data-stu-id="cfe5e-128">If the object generating the notification is not present, the client or provider requesting notification must keep a separate reference count for that object for the object's advise sink.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="cfe5e-129">**Храллокадвисесинк** следует использовать экономно; Клиенты более безопасны для создания собственных приемников уведомлений.</span><span class="sxs-lookup"><span data-stu-id="cfe5e-129">**HrAllocAdviseSink** should be used sparingly; it is safer for clients to create their own advise sinks.</span></span> 
  

