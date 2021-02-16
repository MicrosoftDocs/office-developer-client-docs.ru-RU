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
ms.openlocfilehash: 1e64241008a4adde4431b2c9683199294f21e396
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410562"
---
# <a name="administering-profiles-and-message-services"></a><span data-ttu-id="115d4-103">Администрирование профилей и служб сообщений</span><span class="sxs-lookup"><span data-stu-id="115d4-103">Administering Profiles and Message Services</span></span>

  
  
<span data-ttu-id="115d4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="115d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="115d4-105">Администрирование профилей и служб сообщений может включать создание новых профилей, удаление старых профилей и изменение содержимого существующих профилей путем изменения служб сообщений и содержащихся в них поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="115d4-105">Profile and message service administration can involve creating new profiles, deleting old profiles, and modifying the contents of existing profiles by changing the message services and service providers contained within them.</span></span> <span data-ttu-id="115d4-106">Не все клиенты поддерживают администрирование профилей и служб сообщений в качестве стандартных функций.</span><span class="sxs-lookup"><span data-stu-id="115d4-106">Not all clients support profile and message service administration as standard features.</span></span> <span data-ttu-id="115d4-107">Некоторые клиенты не имеют ничего больше общего с профилями, чем позволяют пользователям выбирать их во время логотипа.</span><span class="sxs-lookup"><span data-stu-id="115d4-107">Some clients have nothing more to do with profiles than allow their users to select one at logon time.</span></span>
  
<span data-ttu-id="115d4-108">Если вы поддерживаете администрирование профиля или службы сообщений, скорее всего, вы будете использовать следующие интерфейсы, реализованные с помощью MAPI:</span><span class="sxs-lookup"><span data-stu-id="115d4-108">If you support profile or message service administration, chances are you will use the following interfaces that are implemented by MAPI:</span></span>
  
- <span data-ttu-id="115d4-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) для администрирования службы сообщений в профиле, доступном через [IMAPISession::AdminServices](imapisession-adminservices.md) или [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span><span class="sxs-lookup"><span data-stu-id="115d4-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) to administer a message service in a profile, accessible through either [IMAPISession::AdminServices](imapisession-adminservices.md) or [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span></span> <span data-ttu-id="115d4-110">Клиенты обмена сообщениями обычно звонят **по IMAPISession,** когда клиенты конфигурации или клиенты, которые не отправляют и не получают сообщения, звонят **в IProfAdmin.**</span><span class="sxs-lookup"><span data-stu-id="115d4-110">Messaging clients typically call **IMAPISession** while configuration clients, or clients that do not send or receive messages, call **IProfAdmin**.</span></span> <span data-ttu-id="115d4-111">По возможности вызовите метод **IProfAdmin,** так как он не вызывает службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="115d4-111">Whenever possible, call the **IProfAdmin** method because it does not cause the message service to be started.</span></span> <span data-ttu-id="115d4-112">Дополнительные сведения об использовании интерфейса **IMsgServiceAdmin** [](configuring-a-message-service.md)см. в следующих темах: "Настройка службы сообщений", [](copying-a-message-service.md)"Копирование службы сообщений" и "Удаление [службы сообщений".](deleting-a-message-service.md)</span><span class="sxs-lookup"><span data-stu-id="115d4-112">For more information about using the **IMsgServiceAdmin** interface, see the following topics: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).</span></span>
    
- <span data-ttu-id="115d4-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) для администрирования профиля, доступного через [функцию MAPIAdminProfiles.](mapiadminprofiles.md)</span><span class="sxs-lookup"><span data-stu-id="115d4-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) to administer a profile, accessible through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> <span data-ttu-id="115d4-114">Дополнительные сведения об использовании интерфейса **IProfAdmin** см. в следующих [](copying-a-profile.md) [темах:](creating-a-profile-by-using-custom-code.md)"Создание профиля с помощью пользовательского кода", "Копирование профиля", [](deleting-a-profile.md)"Удаление профиля", [](finding-a-profile-name.md)"Поиск имени профиля" и "Настройка профиля по умолчанию". [](setting-a-default-profile.md)</span><span class="sxs-lookup"><span data-stu-id="115d4-114">For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), [Finding a Profile Name](finding-a-profile-name.md), and [Setting a Default Profile](setting-a-default-profile.md).</span></span>
    
- <span data-ttu-id="115d4-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) для обслуживания свойств в разделе профиля, доступном с помощью [метода IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) или [IProviderAdmin::OpenProfileSection.](iprovideradmin-openprofilesection.md)</span><span class="sxs-lookup"><span data-stu-id="115d4-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) to maintain the properties in a profile section, accessible through the [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> <span data-ttu-id="115d4-116">Дополнительные сведения о разделах профилей см. в [разделах "Профили MAPI".](mapi-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="115d4-116">For more information about profile sections, see [MAPI Profiles](mapi-profiles.md).</span></span>
    
- <span data-ttu-id="115d4-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) для администрирования поставщиков услуг в службе сообщений, доступной через [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span><span class="sxs-lookup"><span data-stu-id="115d4-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) to administer the service providers in a message service, accessible through [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span></span> <span data-ttu-id="115d4-118">Дополнительные сведения об использовании интерфейса **IProviderAdmin** см. в подпрограмме "Добавление или удаление поставщиков [в службе сообщений".](adding-or-deleting-providers-in-a-message-service.md)</span><span class="sxs-lookup"><span data-stu-id="115d4-118">For more information about using the **IProviderAdmin** interface, see [Adding or Deleting Providers in a Message Service](adding-or-deleting-providers-in-a-message-service.md).</span></span>
    
<span data-ttu-id="115d4-119">Будьте осторожны при поддержке администрирования профилей и служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="115d4-119">Be careful in your support of profile and message service administration.</span></span> <span data-ttu-id="115d4-120">Не существует мер защиты от отрицательного изменения используемой профили.</span><span class="sxs-lookup"><span data-stu-id="115d4-120">There are no safeguards to protect against adversely modifying a profile that is in use.</span></span> <span data-ttu-id="115d4-121">MAPI может предотвратить удаление используемой службы сообщений, но не может предотвратить удаление всех служб сообщений в нем.</span><span class="sxs-lookup"><span data-stu-id="115d4-121">MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it.</span></span> <span data-ttu-id="115d4-122">Если удалить все службы сообщений в профиле, все поставщики служб в этих службах перестанут таким образом вызывать непредсказуемые результаты.</span><span class="sxs-lookup"><span data-stu-id="115d4-122">If you delete every message service in a profile, all of the service providers in these services will stop thereby causing unpredictable results to occur.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="115d4-123">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="115d4-123">In this section</span></span>

[<span data-ttu-id="115d4-124">Создание профиля</span><span class="sxs-lookup"><span data-stu-id="115d4-124">Creating a Profile</span></span>](creating-a-profile.md)
  
> <span data-ttu-id="115d4-125">Описывает создание профиля.</span><span class="sxs-lookup"><span data-stu-id="115d4-125">Describes how to create a profile.</span></span>
    
[<span data-ttu-id="115d4-126">Копирование профиля</span><span class="sxs-lookup"><span data-stu-id="115d4-126">Copying a Profile</span></span>](copying-a-profile.md)
  
> <span data-ttu-id="115d4-127">Описывает копирование профиля.</span><span class="sxs-lookup"><span data-stu-id="115d4-127">Describes how to copy a profile.</span></span>
    
[<span data-ttu-id="115d4-128">Удаление профиля</span><span class="sxs-lookup"><span data-stu-id="115d4-128">Deleting a Profile</span></span>](deleting-a-profile.md)
  
> <span data-ttu-id="115d4-129">Описывает удаление профиля.</span><span class="sxs-lookup"><span data-stu-id="115d4-129">Describes how to delete a profile.</span></span>
    
[<span data-ttu-id="115d4-130">Настройка профиля по умолчанию</span><span class="sxs-lookup"><span data-stu-id="115d4-130">Setting a Default Profile</span></span>](setting-a-default-profile.md)
  
> <span data-ttu-id="115d4-131">Описывается, как установить профиль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="115d4-131">Describes how to set a default profile.</span></span>
    
[<span data-ttu-id="115d4-132">Поиск имени профиля</span><span class="sxs-lookup"><span data-stu-id="115d4-132">Finding a Profile Name</span></span>](finding-a-profile-name.md)
  
> <span data-ttu-id="115d4-133">Описывает, как найти имя профиля.</span><span class="sxs-lookup"><span data-stu-id="115d4-133">Describes how to find a name of a profile.</span></span>
    
[<span data-ttu-id="115d4-134">Добавление службы сообщений</span><span class="sxs-lookup"><span data-stu-id="115d4-134">Adding a Message Service</span></span>](adding-a-message-service.md)
  
> <span data-ttu-id="115d4-135">Описывается добавление службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="115d4-135">Describes how to add a message service.</span></span>
    
[<span data-ttu-id="115d4-136">Настройка службы сообщений</span><span class="sxs-lookup"><span data-stu-id="115d4-136">Configuring a Message Service</span></span>](configuring-a-message-service.md)
  
> <span data-ttu-id="115d4-137">Описывает настройку службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="115d4-137">Describes how to configure a message service.</span></span>
    
[<span data-ttu-id="115d4-138">Копирование службы сообщений</span><span class="sxs-lookup"><span data-stu-id="115d4-138">Copying a Message Service</span></span>](copying-a-message-service.md)
  
> <span data-ttu-id="115d4-139">Описывается копирование службы сообщений в профиль.</span><span class="sxs-lookup"><span data-stu-id="115d4-139">Describes how to copy a message service to a profile.</span></span>
    
[<span data-ttu-id="115d4-140">Удаление службы сообщений</span><span class="sxs-lookup"><span data-stu-id="115d4-140">Deleting a Message Service</span></span>](deleting-a-message-service.md)
  
> <span data-ttu-id="115d4-141">Описывается, как удалить службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="115d4-141">Describes how to delete a message service.</span></span>
    
[<span data-ttu-id="115d4-142">Добавление или удаление поставщиков в службе сообщений</span><span class="sxs-lookup"><span data-stu-id="115d4-142">Adding or Deleting Providers in a Message Service</span></span>](adding-or-deleting-providers-in-a-message-service.md)
  
> <span data-ttu-id="115d4-143">Описывается добавление или удаление поставщиков в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="115d4-143">Describes how to add or delete providers in a message service.</span></span>
    

