---
title: Сведения об API автономного состояния
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: df225a0852b09e048656e817c54ea28b0de59888
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808000"
---
# <a name="about-the-offline-state-api"></a><span data-ttu-id="724cd-103">Сведения об API автономного состояния</span><span class="sxs-lookup"><span data-stu-id="724cd-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="724cd-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="724cd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="724cd-105">Автономные состояния API поддерживает обратных вызовов, указывающее, изменения в состоянии подключения пользователя в Microsoft Outlook 2013 и Microsoft Outlook 2010 — например, от которого online в Outlook 2013 или Outlook 2010 для отключения.</span><span class="sxs-lookup"><span data-stu-id="724cd-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="724cd-106">API-Интерфейс используется объект глобального автономной в Outlook 2013 или Outlook 2010 для отслеживания таких изменений для профиля учетной записи указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="724cd-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="724cd-107">Уведомления — это единственный поддерживаемого форм обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="724cd-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="724cd-108">Как клиенты этот интерфейс API почты поставщиков, кому требуется получать уведомления о такие изменения состояния подключения выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="724cd-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="724cd-109">Реализация **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="724cd-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="724cd-110">Откройте существующий объект автономной для определенного профиля, с помощью **[HrOpenOfflineObj](hropenofflineobj.md)**.</span><span class="sxs-lookup"><span data-stu-id="724cd-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="724cd-111">Определяет, есть ли объект возможностью поддержки сетевым и автономным уведомлений с помощью **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="724cd-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="724cd-112">Регистрация объекта сетевым и автономным уведомлений с помощью **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="724cd-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="724cd-113">Поставщики почты могут получать уведомления о том, что Outlook 2010 или Outlook 2013 отправить, используя **IMAPIOfflineNotify**.</span><span class="sxs-lookup"><span data-stu-id="724cd-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="724cd-114">При завершении работы удалите регистрацию автономном и интерактивном режимах уведомлений с помощью **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span><span class="sxs-lookup"><span data-stu-id="724cd-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="724cd-115">В общем случае Outlook 2013 и Outlook 2010 можно уведомление клиента онлайновом/интерактивном режиме изменения, а также другие изменения, но автономного состояния API поддерживает только уведомления для онлайновом/интерактивном режиме изменения.</span><span class="sxs-lookup"><span data-stu-id="724cd-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="724cd-116">Клиент должен игнорировать все уведомления.</span><span class="sxs-lookup"><span data-stu-id="724cd-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="724cd-117">Для получения дополнительных сведений см **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** и **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="724cd-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="724cd-118">Пример клиента, использующего автономный режим состояния API видеть [о пример автономный режим состояние надстройки](about-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="724cd-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="724cd-119">Добавить пример состояние не в сети в является надстройки COM, которая использует автономный режим состояния API-Интерфейс для мониторинга и изменить состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="724cd-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="724cd-120">Этот интерфейс API предоставляет следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="724cd-120">This API provides the following:</span></span>
  
<span data-ttu-id="724cd-121">Определения:</span><span class="sxs-lookup"><span data-stu-id="724cd-121">Definitions:</span></span>
  
- [<span data-ttu-id="724cd-122">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="724cd-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="724cd-123">Типы данных:</span><span class="sxs-lookup"><span data-stu-id="724cd-123">Data types:</span></span>
  
- <span data-ttu-id="724cd-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="724cd-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="724cd-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="724cd-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="724cd-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="724cd-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="724cd-127">Функции:</span><span class="sxs-lookup"><span data-stu-id="724cd-127">Functions:</span></span>
  
- <span data-ttu-id="724cd-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="724cd-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="724cd-129">Интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="724cd-129">Interfaces:</span></span>
  
- <span data-ttu-id="724cd-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="724cd-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="724cd-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="724cd-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="724cd-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="724cd-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

