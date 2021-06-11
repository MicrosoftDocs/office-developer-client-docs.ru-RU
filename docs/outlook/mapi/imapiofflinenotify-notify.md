---
title: IMAPIOfflineNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify.Notify
api_type:
- COM
ms.assetid: 10c7cb9d-2e9d-72eb-6b07-31eed892e646
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 4440df4b8e4a46e13748cf47d599e16599aaf858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410695"
---
# <a name="imapiofflinenotifynotify"></a><span data-ttu-id="e25a1-103">IMAPIOfflineNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="e25a1-103">IMAPIOfflineNotify::Notify</span></span>

  
  
<span data-ttu-id="e25a1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e25a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e25a1-105">Отправляет клиенту уведомления об изменениях состояния подключения.</span><span class="sxs-lookup"><span data-stu-id="e25a1-105">Sends notifications to the client about changes in connection state.</span></span>
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a><span data-ttu-id="e25a1-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e25a1-106">Parameters</span></span>

 <span data-ttu-id="e25a1-107">_pNotifyInfo_</span><span class="sxs-lookup"><span data-stu-id="e25a1-107">_pNotifyInfo_</span></span>
  
> <span data-ttu-id="e25a1-108">[in] Уведомление, которое Outlook клиенту.</span><span class="sxs-lookup"><span data-stu-id="e25a1-108">[in] The notification that Outlook sends to the client.</span></span> <span data-ttu-id="e25a1-109">В уведомлении указывается часть измененного состояния подключения, старое состояние подключения и новое состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="e25a1-109">The notification indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e25a1-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="e25a1-110">Remarks</span></span>

<span data-ttu-id="e25a1-111">Outlook этот метод используется для отправки клиенту отзова уведомлений.</span><span class="sxs-lookup"><span data-stu-id="e25a1-111">Outlook uses this method to send notification callbacks to a client.</span></span> <span data-ttu-id="e25a1-112">Чтобы сделать этот интерфейс доступным для Microsoft Outlook 2010, русская версия или Microsoft Outlook 2013, клиент должен реализовать этот интерфейс и передать **[](mapioffline_adviseinfo.md)** ему указатель в качестве участника MAPIOFFLINE_ADVISEINFO при настройке вызовов с помощью **[IMAPIOfflineMgr:::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="e25a1-112">To make this interface available to Microsoft Outlook 2010 or Microsoft Outlook 2013, the client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
  
<span data-ttu-id="e25a1-113">Клиент также передает  MAPIOFFLINE_ADVISEINFO клиентский маркер, который Outlook 2010 или Outlook 2013 г. используется в **IMAPIOfflineNotify:::Notify** для идентификации клиента, зарегистрированного для вызова уведомления.</span><span class="sxs-lookup"><span data-stu-id="e25a1-113">The client also passes to **MAPIOFFLINE_ADVISEINFO** a client token that Outlook 2010 or Outlook 2013 uses in **IMAPIOfflineNotify::Notify** to identify the client registered for the notification callback.</span></span> 
  
<span data-ttu-id="e25a1-114">Как правило, Outlook 2010 и Outlook 2013 г. может уведомлять клиента об изменениях в режиме online/offline и других изменениях состояния подключения, но API состояния автономного подключения поддерживает только уведомления для изменений в режиме online/offline.</span><span class="sxs-lookup"><span data-stu-id="e25a1-114">In general, Outlook 2010 and Outlook 2013 can notify a client of online/offline changes and other connection state changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="e25a1-115">Клиент должен игнорировать все другие уведомления.</span><span class="sxs-lookup"><span data-stu-id="e25a1-115">The client must ignore all other notifications.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e25a1-116">См. также</span><span class="sxs-lookup"><span data-stu-id="e25a1-116">See also</span></span>



[<span data-ttu-id="e25a1-117">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="e25a1-117">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="e25a1-118">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="e25a1-118">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

