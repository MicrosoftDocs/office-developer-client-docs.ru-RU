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
# <a name="administering-profiles-and-message-services"></a><span data-ttu-id="53fa2-103">Администрирование профилей и служб сообщений</span><span class="sxs-lookup"><span data-stu-id="53fa2-103">Administering Profiles and Message Services</span></span>

  
  
<span data-ttu-id="53fa2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53fa2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53fa2-105">Администратор службы профилей и сообщений может создавать новые профили, удалять старые профили и изменять содержимое существующих профилей, изменяя службы сообщений и поставщики услуг, содержащиеся в них.</span><span class="sxs-lookup"><span data-stu-id="53fa2-105">Profile and message service administration can involve creating new profiles, deleting old profiles, and modifying the contents of existing profiles by changing the message services and service providers contained within them.</span></span> <span data-ttu-id="53fa2-106">Не все клиенты поддерживают управление профилями и службами сообщений в качестве стандартных функций.</span><span class="sxs-lookup"><span data-stu-id="53fa2-106">Not all clients support profile and message service administration as standard features.</span></span> <span data-ttu-id="53fa2-107">У некоторых клиентов нет ничего больше действий с профилями, чем разрешить пользователям выбирать один из них во время входа.</span><span class="sxs-lookup"><span data-stu-id="53fa2-107">Some clients have nothing more to do with profiles than allow their users to select one at logon time.</span></span>
  
<span data-ttu-id="53fa2-108">Если вы поддерживаете Управление профилями или службами сообщений, вероятно, вы будете использовать следующие интерфейсы, реализованные MAPI:</span><span class="sxs-lookup"><span data-stu-id="53fa2-108">If you support profile or message service administration, chances are you will use the following interfaces that are implemented by MAPI:</span></span>
  
- <span data-ttu-id="53fa2-109">[Имсгсервицеадмин: IUnknown](imsgserviceadminiunknown.md) для администрирования службы сообщений в профиле, доступ к которым можно получить с помощью [IMAPISession:: админсервицес](imapisession-adminservices.md) или [ипрофадмин:: админсервицес](iprofadmin-adminservices.md).</span><span class="sxs-lookup"><span data-stu-id="53fa2-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) to administer a message service in a profile, accessible through either [IMAPISession::AdminServices](imapisession-adminservices.md) or [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span></span> <span data-ttu-id="53fa2-110">Клиенты обмена сообщениями обычно вызывают **IMAPISession** , когда клиенты конфигурации или клиенты, которые не могут отправлять и получать сообщения, вызывают **ипрофадмин**.</span><span class="sxs-lookup"><span data-stu-id="53fa2-110">Messaging clients typically call **IMAPISession** while configuration clients, or clients that do not send or receive messages, call **IProfAdmin**.</span></span> <span data-ttu-id="53fa2-111">По мере возможности вызовите метод **ипрофадмин** , так как он не приводит к запуску службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="53fa2-111">Whenever possible, call the **IProfAdmin** method because it does not cause the message service to be started.</span></span> <span data-ttu-id="53fa2-112">Дополнительные сведения об использовании интерфейса **имсгсервицеадмин** представлены в следующих разделах: [Настройка службы сообщений](configuring-a-message-service.md), [копирование службы](copying-a-message-service.md)сообщений и [Удаление службы сообщений](deleting-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="53fa2-112">For more information about using the **IMsgServiceAdmin** interface, see the following topics: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).</span></span>
    
- <span data-ttu-id="53fa2-113">[Ипрофадмин: IUnknown](iprofadminiunknown.md) для администрирования профиля, доступный с помощью функции [мапиадминпрофилес](mapiadminprofiles.md) .</span><span class="sxs-lookup"><span data-stu-id="53fa2-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) to administer a profile, accessible through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> <span data-ttu-id="53fa2-114">Дополнительные сведения об использовании интерфейса **ипрофадмин** представлены в следующих разделах: [Создание профиля с помощью пользовательского кода](creating-a-profile-by-using-custom-code.md), [копирование профиля](copying-a-profile.md), [Удаление профиля](deleting-a-profile.md), [Поиск имени профиля](finding-a-profile-name.md)и [Настройка Профиль по умолчанию](setting-a-default-profile.md).</span><span class="sxs-lookup"><span data-stu-id="53fa2-114">For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), [Finding a Profile Name](finding-a-profile-name.md), and [Setting a Default Profile](setting-a-default-profile.md).</span></span>
    
- <span data-ttu-id="53fa2-115">[Ипрофсект: IMAPIProp](iprofsectimapiprop.md) для хранения свойств в разделе профиля, доступ к которому можно получить с помощью метода [IMAPISession:: опенпрофилесектион](imapisession-openprofilesection.md) или [ипровидерадмин:: опенпрофилесектион](iprovideradmin-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="53fa2-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) to maintain the properties in a profile section, accessible through the [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> <span data-ttu-id="53fa2-116">Дополнительные сведения о разделах профилей см. [](mapi-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="53fa2-116">For more information about profile sections, see [MAPI Profiles](mapi-profiles.md).</span></span>
    
- <span data-ttu-id="53fa2-117">[Ипровидерадмин: IUnknown](iprovideradminiunknown.md) для администрирования поставщиков служб в службе сообщений, доступных через [Имсгсервицеадмин:: админпровидерс](imsgserviceadmin-adminproviders.md).</span><span class="sxs-lookup"><span data-stu-id="53fa2-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) to administer the service providers in a message service, accessible through [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span></span> <span data-ttu-id="53fa2-118">Дополнительные сведения об использовании интерфейса **ипровидерадмин** приведены [в статье Добавление или удаление поставщиков в службе сообщений](adding-or-deleting-providers-in-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="53fa2-118">For more information about using the **IProviderAdmin** interface, see [Adding or Deleting Providers in a Message Service](adding-or-deleting-providers-in-a-message-service.md).</span></span>
    
<span data-ttu-id="53fa2-119">Следите за поддержкой управления профилями и службами сообщений.</span><span class="sxs-lookup"><span data-stu-id="53fa2-119">Be careful in your support of profile and message service administration.</span></span> <span data-ttu-id="53fa2-120">Нет мер защиты от неблагоприятного изменения используемого профиля.</span><span class="sxs-lookup"><span data-stu-id="53fa2-120">There are no safeguards to protect against adversely modifying a profile that is in use.</span></span> <span data-ttu-id="53fa2-121">Служба MAPI может препятствовать удалению профиля, но не может запретить удаление всех сообщений в ней.</span><span class="sxs-lookup"><span data-stu-id="53fa2-121">MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it.</span></span> <span data-ttu-id="53fa2-122">Если вы удалите каждую службу сообщений в профиле, все поставщики услуг, указанные в этих службах, приостанавливаются, тем самым вызывая непредсказуемые результаты.</span><span class="sxs-lookup"><span data-stu-id="53fa2-122">If you delete every message service in a profile, all of the service providers in these services will stop thereby causing unpredictable results to occur.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="53fa2-123">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="53fa2-123">In this section</span></span>

[<span data-ttu-id="53fa2-124">Создание профиля</span><span class="sxs-lookup"><span data-stu-id="53fa2-124">Creating a Profile</span></span>](creating-a-profile.md)
  
> <span data-ttu-id="53fa2-125">Описывается создание профиля.</span><span class="sxs-lookup"><span data-stu-id="53fa2-125">Describes how to create a profile.</span></span>
    
[<span data-ttu-id="53fa2-126">Копирование профиля</span><span class="sxs-lookup"><span data-stu-id="53fa2-126">Copying a Profile</span></span>](copying-a-profile.md)
  
> <span data-ttu-id="53fa2-127">Описывается копирование профиля.</span><span class="sxs-lookup"><span data-stu-id="53fa2-127">Describes how to copy a profile.</span></span>
    
[<span data-ttu-id="53fa2-128">Удаление профиля</span><span class="sxs-lookup"><span data-stu-id="53fa2-128">Deleting a Profile</span></span>](deleting-a-profile.md)
  
> <span data-ttu-id="53fa2-129">Описывает, как удалить профиль.</span><span class="sxs-lookup"><span data-stu-id="53fa2-129">Describes how to delete a profile.</span></span>
    
[<span data-ttu-id="53fa2-130">Настройка профиля по умолчанию</span><span class="sxs-lookup"><span data-stu-id="53fa2-130">Setting a Default Profile</span></span>](setting-a-default-profile.md)
  
> <span data-ttu-id="53fa2-131">Сведения о том, как задать профиль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="53fa2-131">Describes how to set a default profile.</span></span>
    
[<span data-ttu-id="53fa2-132">Поиск имени профиля</span><span class="sxs-lookup"><span data-stu-id="53fa2-132">Finding a Profile Name</span></span>](finding-a-profile-name.md)
  
> <span data-ttu-id="53fa2-133">Описывается, как найти имя профиля.</span><span class="sxs-lookup"><span data-stu-id="53fa2-133">Describes how to find a name of a profile.</span></span>
    
[<span data-ttu-id="53fa2-134">Добавление службы сообщений</span><span class="sxs-lookup"><span data-stu-id="53fa2-134">Adding a Message Service</span></span>](adding-a-message-service.md)
  
> <span data-ttu-id="53fa2-135">Описывает, как добавить службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="53fa2-135">Describes how to add a message service.</span></span>
    
[<span data-ttu-id="53fa2-136">Настройка службы сообщений</span><span class="sxs-lookup"><span data-stu-id="53fa2-136">Configuring a Message Service</span></span>](configuring-a-message-service.md)
  
> <span data-ttu-id="53fa2-137">Сведения о настройке службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="53fa2-137">Describes how to configure a message service.</span></span>
    
[<span data-ttu-id="53fa2-138">Копирование службы сообщений</span><span class="sxs-lookup"><span data-stu-id="53fa2-138">Copying a Message Service</span></span>](copying-a-message-service.md)
  
> <span data-ttu-id="53fa2-139">Сведения о том, как скопировать службу сообщений в профиль.</span><span class="sxs-lookup"><span data-stu-id="53fa2-139">Describes how to copy a message service to a profile.</span></span>
    
[<span data-ttu-id="53fa2-140">Удаление службы сообщений</span><span class="sxs-lookup"><span data-stu-id="53fa2-140">Deleting a Message Service</span></span>](deleting-a-message-service.md)
  
> <span data-ttu-id="53fa2-141">Описывает, как удалить службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="53fa2-141">Describes how to delete a message service.</span></span>
    
[<span data-ttu-id="53fa2-142">Добавление или удаление поставщиков в службе сообщений</span><span class="sxs-lookup"><span data-stu-id="53fa2-142">Adding or Deleting Providers in a Message Service</span></span>](adding-or-deleting-providers-in-a-message-service.md)
  
> <span data-ttu-id="53fa2-143">Описывает, как добавлять и удалять поставщиков в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="53fa2-143">Describes how to add or delete providers in a message service.</span></span>
    

