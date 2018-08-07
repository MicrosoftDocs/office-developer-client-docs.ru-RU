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
ms.openlocfilehash: 54843339c6843e075ec769da5751ae2fe753f302
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809021"
---
# <a name="imapiofflinenotifynotify"></a><span data-ttu-id="48f79-103">IMAPIOfflineNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="48f79-103">IMAPIOfflineNotify::Notify</span></span>

  
  
<span data-ttu-id="48f79-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="48f79-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="48f79-105">Отправляет уведомления об изменениях в состоянии подключения к клиенту.</span><span class="sxs-lookup"><span data-stu-id="48f79-105">Sends notifications to the client about changes in connection state.</span></span>
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a><span data-ttu-id="48f79-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="48f79-106">Parameters</span></span>

 <span data-ttu-id="48f79-107">_pNotifyInfo_</span><span class="sxs-lookup"><span data-stu-id="48f79-107">_pNotifyInfo_</span></span>
  
> <span data-ttu-id="48f79-108">[in] Уведомление, Outlook отправляет клиенту.</span><span class="sxs-lookup"><span data-stu-id="48f79-108">[in] The notification that Outlook sends to the client.</span></span> <span data-ttu-id="48f79-109">Это уведомление указывает часть состояние подключения, который был изменен, старый состояние подключения и новое состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="48f79-109">The notification indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="48f79-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="48f79-110">Remarks</span></span>

<span data-ttu-id="48f79-111">Outlook использует этот метод для отправки уведомлений обратных вызовов в клиент.</span><span class="sxs-lookup"><span data-stu-id="48f79-111">Outlook uses this method to send notification callbacks to a client.</span></span> <span data-ttu-id="48f79-112">Чтобы сделать этот интерфейс для Microsoft Outlook 2010 или Microsoft Outlook 2013, необходимо реализовать этот интерфейс и передать указатель на него в качестве члена в **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** при настройке обратных вызовов с помощью **[IMAPIOfflineMgr::Advise ](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="48f79-112">To make this interface available to Microsoft Outlook 2010 or Microsoft Outlook 2013, the client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
  
<span data-ttu-id="48f79-113">Клиент также передает **MAPIOFFLINE_ADVISEINFO** маркера клиента, Outlook 2010 или Outlook 2013 с помощью в **IMAPIOfflineNotify::Notify** для идентификации клиента, зарегистрированных для обратного вызова для уведомления.</span><span class="sxs-lookup"><span data-stu-id="48f79-113">The client also passes to **MAPIOFFLINE_ADVISEINFO** a client token that Outlook 2010 or Outlook 2013 uses in **IMAPIOfflineNotify::Notify** to identify the client registered for the notification callback.</span></span> 
  
<span data-ttu-id="48f79-114">В общем случае Outlook 2010 и Outlook 2013 может уведомлять клиента онлайновом/интерактивном режиме изменений и другие изменения состояния подключения, но автономного состояния API поддерживает только уведомления для онлайновом/интерактивном режиме изменения.</span><span class="sxs-lookup"><span data-stu-id="48f79-114">In general, Outlook 2010 and Outlook 2013 can notify a client of online/offline changes and other connection state changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="48f79-115">Клиент должен игнорировать все уведомления.</span><span class="sxs-lookup"><span data-stu-id="48f79-115">The client must ignore all other notifications.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="48f79-116">См. также</span><span class="sxs-lookup"><span data-stu-id="48f79-116">See also</span></span>



[<span data-ttu-id="48f79-117">Сведения об API автономного состояния</span><span class="sxs-lookup"><span data-stu-id="48f79-117">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="48f79-118">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="48f79-118">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

