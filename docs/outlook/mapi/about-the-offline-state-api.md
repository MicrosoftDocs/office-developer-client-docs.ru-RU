---
title: Сведения об API автономного состояния
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410485"
---
# <a name="about-the-offline-state-api"></a><span data-ttu-id="c6d72-103">Сведения об API автономного состояния</span><span class="sxs-lookup"><span data-stu-id="c6d72-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="c6d72-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6d72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6d72-105">API автономного состояния поддерживает обратные вызовы, указывающие изменения состояния подключения пользователя в Microsoft Outlook 2013 и Microsoft Outlook 2010 (например, из сети в Outlook 2013 или Outlook 2010 в автономный режим).</span><span class="sxs-lookup"><span data-stu-id="c6d72-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="c6d72-106">API использует глобальный автономный объект в Outlook 2013 или Outlook 2010 для отслеживания этих изменений для определенного профиля учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="c6d72-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="c6d72-107">Уведомление — единственная поддерживаемая форма обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="c6d72-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="c6d72-108">В качестве клиентов этого API поставщики почты, которые хотят получать уведомления о таких изменениях состояния подключения, выполняют следующие действия:</span><span class="sxs-lookup"><span data-stu-id="c6d72-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="c6d72-109">Реализация **[имапиоффлиненотифи](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="c6d72-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="c6d72-110">Откройте существующий автономный объект для определенного профиля с помощью **[хропеноффлинеобж](hropenofflineobj.md)**.</span><span class="sxs-lookup"><span data-stu-id="c6d72-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="c6d72-111">Определите, имеет ли объект возможность предоставления уведомлений в Интернете или в автономном режиме с помощью **[имапиоффлине::-Capabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="c6d72-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="c6d72-112">ЗаРегистрируйте объект для интерактивных или автономных уведомлений с помощью **[имапиоффлинемгр:: Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="c6d72-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="c6d72-113">Теперь поставщики почты могут получать уведомления, которые Outlook 2013 или Outlook 2010 отправляет с помощью **имапиоффлиненотифи**.</span><span class="sxs-lookup"><span data-stu-id="c6d72-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="c6d72-114">При завершении работы удалите регистрацию для уведомлений в Интернете и в автономном режиме с помощью **[имапиоффлинемгр:: unadvise](imapiofflinemgr-unadvise.md)**.</span><span class="sxs-lookup"><span data-stu-id="c6d72-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="c6d72-115">Как правило, Outlook 2013 и Outlook 2010 могут уведомлять Клиента об изменениях в Интернете или в автономном режиме, а также других изменениях, но API автономного состояния поддерживает только уведомления об изменениях в Интернете и в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="c6d72-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="c6d72-116">Клиент должен игнорировать все остальные уведомления.</span><span class="sxs-lookup"><span data-stu-id="c6d72-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="c6d72-117">Дополнительные сведения см. в статье **[имапиоффлиненотифи:: notify](imapiofflinenotify-notify.md)** and **[мапиоффлине_нотифи](mapioffline_notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="c6d72-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="c6d72-118">Пример клиента, использующего API автономного состояния, представлен в статье [Пример надстройки](about-the-sample-offline-state-add-in.md)с автономным состоянием.</span><span class="sxs-lookup"><span data-stu-id="c6d72-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="c6d72-119">Надстройка "автономное состояние" — это надстройка COM, использующая API автономного состояния для отслеживания и изменения состояния подключения.</span><span class="sxs-lookup"><span data-stu-id="c6d72-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="c6d72-120">Этот API предоставляет следующие функции:</span><span class="sxs-lookup"><span data-stu-id="c6d72-120">This API provides the following:</span></span>
  
<span data-ttu-id="c6d72-121">Определения</span><span class="sxs-lookup"><span data-stu-id="c6d72-121">Definitions:</span></span>
  
- [<span data-ttu-id="c6d72-122">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="c6d72-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="c6d72-123">Типы данных:</span><span class="sxs-lookup"><span data-stu-id="c6d72-123">Data types:</span></span>
  
- <span data-ttu-id="c6d72-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="c6d72-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="c6d72-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="c6d72-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="c6d72-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="c6d72-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="c6d72-127">Обязанностей</span><span class="sxs-lookup"><span data-stu-id="c6d72-127">Functions:</span></span>
  
- <span data-ttu-id="c6d72-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="c6d72-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="c6d72-129">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="c6d72-129">Interfaces:</span></span>
  
- <span data-ttu-id="c6d72-130">**[Имапиоффлине](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="c6d72-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="c6d72-131">**[Имапиоффлинемгр](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="c6d72-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="c6d72-132">**[Имапиоффлиненотифи](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="c6d72-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

