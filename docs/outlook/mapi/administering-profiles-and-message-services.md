---
title: Администрирование профилей и служб сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 71e8cf50c1951abf1df6163cae4757ffebc979b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808024"
---
# <a name="administering-profiles-and-message-services"></a><span data-ttu-id="e1d95-103">Администрирование профилей и служб сообщений</span><span class="sxs-lookup"><span data-stu-id="e1d95-103">Administering Profiles and Message Services</span></span>

  
  
<span data-ttu-id="e1d95-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e1d95-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e1d95-105">Профиль и администрирование службы может включать в себя создание новых профилей, удаление старых профилей и изменения содержимого существующих профилей с помощью изменения службы сообщений и поставщиков услуг, содержащихся в них сообщения.</span><span class="sxs-lookup"><span data-stu-id="e1d95-105">Profile and message service administration can involve creating new profiles, deleting old profiles, and modifying the contents of existing profiles by changing the message services and service providers contained within them.</span></span> <span data-ttu-id="e1d95-106">Не все клиенты поддерживают администрирование службы профилей и сообщение как стандартные функции.</span><span class="sxs-lookup"><span data-stu-id="e1d95-106">Not all clients support profile and message service administration as standard features.</span></span> <span data-ttu-id="e1d95-107">Некоторые клиенты не более с профилями, не позволять пользователям выбрать один во время входа в систему.</span><span class="sxs-lookup"><span data-stu-id="e1d95-107">Some clients have nothing more to do with profiles than allow their users to select one at logon time.</span></span>
  
<span data-ttu-id="e1d95-108">Если вы поддерживаете администрирования службы профиля или сообщения, скорее всего, будет использоваться следующие интерфейсы, которые реализуются MAPI:</span><span class="sxs-lookup"><span data-stu-id="e1d95-108">If you support profile or message service administration, chances are you will use the following interfaces that are implemented by MAPI:</span></span>
  
- <span data-ttu-id="e1d95-109">[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) для администрирования службы сообщений в профиле через [IMAPISession::AdminServices](imapisession-adminservices.md) или [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span><span class="sxs-lookup"><span data-stu-id="e1d95-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) to administer a message service in a profile, accessible through either [IMAPISession::AdminServices](imapisession-adminservices.md) or [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span></span> <span data-ttu-id="e1d95-110">Клиенты обмена сообщениями вызов **IMAPISession** во время настройки клиентов или клиентов, которые не отправлять и получать сообщения, вызова **IProfAdmin**.</span><span class="sxs-lookup"><span data-stu-id="e1d95-110">Messaging clients typically call **IMAPISession** while configuration clients, or clients that do not send or receive messages, call **IProfAdmin**.</span></span> <span data-ttu-id="e1d95-111">По возможности, вызовите метод **IProfAdmin** , так как он не вызывает сообщения службу для запуска.</span><span class="sxs-lookup"><span data-stu-id="e1d95-111">Whenever possible, call the **IProfAdmin** method because it does not cause the message service to be started.</span></span> <span data-ttu-id="e1d95-112">Дополнительные сведения об использовании интерфейса **IMsgServiceAdmin** в следующих разделах: [Настройка службы сообщений](configuring-a-message-service.md), [скопировав службы сообщений](copying-a-message-service.md)и [Удаление службы сообщений](deleting-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="e1d95-112">For more information about using the **IMsgServiceAdmin** interface, see the following topics: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).</span></span>
    
- <span data-ttu-id="e1d95-113">[IProfAdmin: IUnknown](iprofadminiunknown.md) для администрирования профиля, можно использовать функцию [MAPIAdminProfiles](mapiadminprofiles.md) .</span><span class="sxs-lookup"><span data-stu-id="e1d95-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) to administer a profile, accessible through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> <span data-ttu-id="e1d95-114">Дополнительные сведения об использовании интерфейса **IProfAdmin** в следующих разделах: [Создание профилей с помощью пользовательский код](creating-a-profile-by-using-custom-code.md), [Копирование профиля](copying-a-profile.md), [Удаление профиля](deleting-a-profile.md), [Поиск имени профиля](finding-a-profile-name.md)и [параметр По умолчанию профиль](setting-a-default-profile.md).</span><span class="sxs-lookup"><span data-stu-id="e1d95-114">For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), [Finding a Profile Name](finding-a-profile-name.md), and [Setting a Default Profile](setting-a-default-profile.md).</span></span>
    
- <span data-ttu-id="e1d95-115">[IProfSect: IMAPIProp](iprofsectimapiprop.md) на обслуживание свойства в разделе профилей, можно использовать метод [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) или [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="e1d95-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) to maintain the properties in a profile section, accessible through the [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> <span data-ttu-id="e1d95-116">Дополнительные сведения о разделах профиля можно [Профили MAPI](mapi-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="e1d95-116">For more information about profile sections, see [MAPI Profiles](mapi-profiles.md).</span></span>
    
- <span data-ttu-id="e1d95-117">[IProviderAdmin: IUnknown](iprovideradminiunknown.md) для администрирования поставщиков услуг службы сообщений, можно использовать [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span><span class="sxs-lookup"><span data-stu-id="e1d95-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) to administer the service providers in a message service, accessible through [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span></span> <span data-ttu-id="e1d95-118">Дополнительные сведения об использовании интерфейса **IProviderAdmin** можно [Добавление или удаление поставщиков службы сообщений](adding-or-deleting-providers-in-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="e1d95-118">For more information about using the **IProviderAdmin** interface, see [Adding or Deleting Providers in a Message Service](adding-or-deleting-providers-in-a-message-service.md).</span></span>
    
<span data-ttu-id="e1d95-119">Будьте внимательны, чтобы в вашей поддержки администрирования службы профилей и сообщения.</span><span class="sxs-lookup"><span data-stu-id="e1d95-119">Be careful in your support of profile and message service administration.</span></span> <span data-ttu-id="e1d95-120">Существует не меры безопасности для защиты от отрицательно изменения профиля, который используется.</span><span class="sxs-lookup"><span data-stu-id="e1d95-120">There are no safeguards to protect against adversely modifying a profile that is in use.</span></span> <span data-ttu-id="e1d95-121">MAPI можно запретить удаление профиля используется, но не можете запретить пользователям удаление каждая служба сообщения в нем.</span><span class="sxs-lookup"><span data-stu-id="e1d95-121">MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it.</span></span> <span data-ttu-id="e1d95-122">При удалении каждая служба сообщения в профиль всех поставщиков услуг в эти службы остановит, приводящую к непредсказуемым последствиям будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="e1d95-122">If you delete every message service in a profile, all of the service providers in these services will stop thereby causing unpredictable results to occur.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="e1d95-123">В этой статье</span><span class="sxs-lookup"><span data-stu-id="e1d95-123">In this section</span></span>

[<span data-ttu-id="e1d95-124">Создание профиля</span><span class="sxs-lookup"><span data-stu-id="e1d95-124">Creating a Profile</span></span>](creating-a-profile.md)
  
> <span data-ttu-id="e1d95-125">Описывается, как создать профиль.</span><span class="sxs-lookup"><span data-stu-id="e1d95-125">Describes how to create a profile.</span></span>
    
[<span data-ttu-id="e1d95-126">Копирование профиля</span><span class="sxs-lookup"><span data-stu-id="e1d95-126">Copying a Profile</span></span>](copying-a-profile.md)
  
> <span data-ttu-id="e1d95-127">Описывается, как скопировать профиль.</span><span class="sxs-lookup"><span data-stu-id="e1d95-127">Describes how to copy a profile.</span></span>
    
[<span data-ttu-id="e1d95-128">Удаление профиля</span><span class="sxs-lookup"><span data-stu-id="e1d95-128">Deleting a Profile</span></span>](deleting-a-profile.md)
  
> <span data-ttu-id="e1d95-129">Описывается, как удалить профиль.</span><span class="sxs-lookup"><span data-stu-id="e1d95-129">Describes how to delete a profile.</span></span>
    
[<span data-ttu-id="e1d95-130">Установка профиля по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e1d95-130">Setting a Default Profile</span></span>](setting-a-default-profile.md)
  
> <span data-ttu-id="e1d95-131">В данной статье описывается настройка профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e1d95-131">Describes how to set a default profile.</span></span>
    
[<span data-ttu-id="e1d95-132">Поиск имени профиля</span><span class="sxs-lookup"><span data-stu-id="e1d95-132">Finding a Profile Name</span></span>](finding-a-profile-name.md)
  
> <span data-ttu-id="e1d95-133">Описывается, как найти имя профиля.</span><span class="sxs-lookup"><span data-stu-id="e1d95-133">Describes how to find a name of a profile.</span></span>
    
[<span data-ttu-id="e1d95-134">Добавление службы сообщений</span><span class="sxs-lookup"><span data-stu-id="e1d95-134">Adding a Message Service</span></span>](adding-a-message-service.md)
  
> <span data-ttu-id="e1d95-135">В данной статье описывается добавление службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e1d95-135">Describes how to add a message service.</span></span>
    
[<span data-ttu-id="e1d95-136">Настройка службы сообщений</span><span class="sxs-lookup"><span data-stu-id="e1d95-136">Configuring a Message Service</span></span>](configuring-a-message-service.md)
  
> <span data-ttu-id="e1d95-137">В данной статье описывается настройка службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e1d95-137">Describes how to configure a message service.</span></span>
    
[<span data-ttu-id="e1d95-138">Копирование службы сообщений</span><span class="sxs-lookup"><span data-stu-id="e1d95-138">Copying a Message Service</span></span>](copying-a-message-service.md)
  
> <span data-ttu-id="e1d95-139">Описание копирования службы сообщений в профиль.</span><span class="sxs-lookup"><span data-stu-id="e1d95-139">Describes how to copy a message service to a profile.</span></span>
    
[<span data-ttu-id="e1d95-140">Удаление службы сообщений</span><span class="sxs-lookup"><span data-stu-id="e1d95-140">Deleting a Message Service</span></span>](deleting-a-message-service.md)
  
> <span data-ttu-id="e1d95-141">В данной статье описывается удаление службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e1d95-141">Describes how to delete a message service.</span></span>
    
[<span data-ttu-id="e1d95-142">Добавление или удаление поставщиков в службе сообщений</span><span class="sxs-lookup"><span data-stu-id="e1d95-142">Adding or Deleting Providers in a Message Service</span></span>](adding-or-deleting-providers-in-a-message-service.md)
  
> <span data-ttu-id="e1d95-143">Описывается, как добавлять или удалять поставщиков службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e1d95-143">Describes how to add or delete providers in a message service.</span></span>
    

