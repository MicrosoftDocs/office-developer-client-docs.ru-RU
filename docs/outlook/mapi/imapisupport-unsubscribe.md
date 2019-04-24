---
title: Имаписуппортунсубскрибе
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Unsubscribe
api_type:
- COM
ms.assetid: 3f2870f7-1c08-4d0f-b9d8-7644f5e55b78
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f27da216b9c474aa31503917a6d3c7a74eab9c4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341267"
---
# <a name="imapisupportunsubscribe"></a><span data-ttu-id="ed798-103">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="ed798-103">IMAPISupport::Unsubscribe</span></span>

  
  
<span data-ttu-id="ed798-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed798-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed798-105">ОтМеняет ответственность за отправку уведомлений, которые были установлены ранее при вызове метода [имаписуппорт:: Subscribe](imapisupport-subscribe.md) .</span><span class="sxs-lookup"><span data-stu-id="ed798-105">Cancels the responsibility for sending notifications that was previously established with a call to the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="ed798-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed798-106">Parameters</span></span>

 <span data-ttu-id="ed798-107">_Улконнектион_</span><span class="sxs-lookup"><span data-stu-id="ed798-107">_ulConnection_</span></span>
  
> <span data-ttu-id="ed798-108">возврата Ненулевой номер подключения, представляющий регистрацию уведомления, предварительно установленную через **имаписуппорт:: Subscribe**.</span><span class="sxs-lookup"><span data-stu-id="ed798-108">[in] The nonzero connection number that represents the notification registration previously established through **IMAPISupport::Subscribe**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ed798-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed798-109">Return value</span></span>

<span data-ttu-id="ed798-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ed798-110">S_OK</span></span> 
  
> <span data-ttu-id="ed798-111">Регистрация уведомления отменена.</span><span class="sxs-lookup"><span data-stu-id="ed798-111">The notification registration was canceled.</span></span>
    
<span data-ttu-id="ed798-112">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="ed798-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ed798-113">Номер подключения, переданный в параметре _улконнектион_ , не существует.</span><span class="sxs-lookup"><span data-stu-id="ed798-113">The connection number passed in the  _ulConnection_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ed798-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed798-114">Remarks</span></span>

<span data-ttu-id="ed798-115">Метод **имаписуппорт:: unsubscribe** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="ed798-115">The **IMAPISupport::Unsubscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="ed798-116">Поставщики услуг отменяют подписываться на отмену регистрации уведомлений, предварительно настроенных подПискум. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ed798-116">Service providers call **Unsubscribe** to cancel a notification registration previously set up by **Subscribe**.</span></span> <span data-ttu-id="ed798-117">**Unsubscribe** отменяет регистрацию, освобождая указатель приемника уведомлений, переданный в вызове **Subscribe** .</span><span class="sxs-lookup"><span data-stu-id="ed798-117">**Unsubscribe** cancels the registration by releasing the advise sink pointer passed in the **Subscribe** call.</span></span> 
  
<span data-ttu-id="ed798-118">Как правило, метод **IUnknown:: Release** приемника уведомлений вызывается во время \*\*\*\* вызова unsubscribe.</span><span class="sxs-lookup"><span data-stu-id="ed798-118">Generally, the advise sink's **IUnknown::Release** method is called during the **Unsubscribe** call.</span></span> <span data-ttu-id="ed798-119">Тем не менее, если другой поток находится в процессе вызова метода [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) для объекта приемника уведомлений, вызов **освобождения** задерживается до возвращения метода **OnNotify** .</span><span class="sxs-lookup"><span data-stu-id="ed798-119">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ed798-120">См. также</span><span class="sxs-lookup"><span data-stu-id="ed798-120">See also</span></span>



[<span data-ttu-id="ed798-121">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="ed798-121">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="ed798-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="ed798-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="ed798-123">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ed798-123">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

