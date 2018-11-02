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
description: 'Дата последнего изменения: 25 июня 2012 года'
ms.openlocfilehash: a84114a3363f9cbcd9455bce12d3171843bd18a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571117"
---
# <a name="imapiofflinenotifynotify"></a><span data-ttu-id="1433b-103">IMAPIOfflineNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="1433b-103">IMAPIOfflineNotify::Notify</span></span>

  
  
<span data-ttu-id="1433b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1433b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1433b-105">Отправляет уведомления об изменениях в состоянии подключения к клиенту.</span><span class="sxs-lookup"><span data-stu-id="1433b-105">Sends notifications to the client about changes in connection state.</span></span>
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a><span data-ttu-id="1433b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1433b-106">Parameters</span></span>

 <span data-ttu-id="1433b-107">_pNotifyInfo_</span><span class="sxs-lookup"><span data-stu-id="1433b-107">_pNotifyInfo_</span></span>
  
> <span data-ttu-id="1433b-108">[in] Уведомление, Outlook отправляет клиенту.</span><span class="sxs-lookup"><span data-stu-id="1433b-108">[in] The notification that Outlook sends to the client.</span></span> <span data-ttu-id="1433b-109">Это уведомление указывает часть состояние подключения, который был изменен, старый состояние подключения и новое состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="1433b-109">The notification indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1433b-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="1433b-110">Remarks</span></span>

<span data-ttu-id="1433b-111">Outlook использует этот метод для отправки уведомлений обратных вызовов в клиент.</span><span class="sxs-lookup"><span data-stu-id="1433b-111">Outlook uses this method to send notification callbacks to a client.</span></span> <span data-ttu-id="1433b-112">Чтобы сделать этот интерфейс для Microsoft Outlook 2010 или Microsoft Outlook 2013, необходимо реализовать этот интерфейс и передать указатель на него в качестве члена в **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** при настройке обратных вызовов с помощью **[IMAPIOfflineMgr::Advise ](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="1433b-112">To make this interface available to Microsoft Outlook 2010 or Microsoft Outlook 2013, the client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
  
<span data-ttu-id="1433b-113">Клиент также передает **MAPIOFFLINE_ADVISEINFO** маркера клиента, Outlook 2010 или Outlook 2013 с помощью в **IMAPIOfflineNotify::Notify** для идентификации клиента, зарегистрированных для обратного вызова для уведомления.</span><span class="sxs-lookup"><span data-stu-id="1433b-113">The client also passes to **MAPIOFFLINE_ADVISEINFO** a client token that Outlook 2010 or Outlook 2013 uses in **IMAPIOfflineNotify::Notify** to identify the client registered for the notification callback.</span></span> 
  
<span data-ttu-id="1433b-114">В общем случае Outlook 2010 и Outlook 2013 может уведомлять клиента онлайновом/интерактивном режиме изменений и другие изменения состояния подключения, но автономного состояния API поддерживает только уведомления для онлайновом/интерактивном режиме изменения.</span><span class="sxs-lookup"><span data-stu-id="1433b-114">In general, Outlook 2010 and Outlook 2013 can notify a client of online/offline changes and other connection state changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="1433b-115">Клиент должен игнорировать все уведомления.</span><span class="sxs-lookup"><span data-stu-id="1433b-115">The client must ignore all other notifications.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1433b-116">См. также</span><span class="sxs-lookup"><span data-stu-id="1433b-116">See also</span></span>



[<span data-ttu-id="1433b-117">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="1433b-117">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="1433b-118">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="1433b-118">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

