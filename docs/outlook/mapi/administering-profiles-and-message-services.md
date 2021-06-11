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
# <a name="administering-profiles-and-message-services"></a>Администрирование профилей и служб сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Администрирование профилей и служб сообщений может включать создание новых профилей, удаление старых профилей и изменение содержимого существующих профилей путем изменения служб и поставщиков сообщений, содержащихся в них. Не все клиенты поддерживают администрирование профилей и служб сообщений в качестве стандартных функций. Некоторые клиенты не имеют ничего общего с профайлами, чем разрешить пользователям выбирать их в логосное время.
  
Если вы поддерживаете администрирование профиля или службы сообщений, скорее всего, вы будете использовать следующие интерфейсы, реализованные MAPI:
  
- [IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) для администрирования службы сообщений в профиле, доступном через [IMAPISession::AdminServices](imapisession-adminservices.md) или [IProfAdmin::AdminServices](iprofadmin-adminservices.md). Клиенты обмена сообщениями обычно звонят **по вызову IMAPISession,** а клиенты конфигурации или клиенты, которые не отправляют или не получают сообщения, звонят **в IProfAdmin**. По возможности вызывай **метод IProfAdmin,** так как он не вызывает работу службы сообщений. Дополнительные сведения об использовании интерфейса **IMsgServiceAdmin** [](configuring-a-message-service.md)см. в следующих темах: Настройка службы сообщений, [](copying-a-message-service.md)копирование службы сообщений и удаление [службы сообщений.](deleting-a-message-service.md)
    
- [IProfAdmin : IUnknown](iprofadminiunknown.md) для администрирования профиля, доступного через [функцию MAPIAdminProfiles.](mapiadminprofiles.md) Дополнительные сведения об использовании интерфейса **IProfAdmin** [см.](creating-a-profile-by-using-custom-code.md)в следующих темах: Создание профиля с помощью настраиваемой кодифики, [](copying-a-profile.md)копирование [профиля,](deleting-a-profile.md)удаление [профиля,](finding-a-profile-name.md)поиск имени профиля и настройка профиля по [умолчанию.](setting-a-default-profile.md)
    
- [IProfSect : IMAPIProp](iprofsectimapiprop.md) для поддержания свойств в разделе профилей, доступных с помощью [метода IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) или [IProviderAdmin::OpenProfileSection.](iprovideradmin-openprofilesection.md) Дополнительные сведения о разделах профилей см. в [разделах MAPI Profiles.](mapi-profiles.md)
    
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md) для администрирования поставщиков услуг в службе сообщений, доступной через [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). Дополнительные сведения об использовании интерфейса **IProviderAdmin** см. в дополнительных сведениях о добавлении или удалении поставщиков в [службе сообщений.](adding-or-deleting-providers-in-a-message-service.md)
    
Будьте осторожны в поддержке администрирования профилей и служб сообщений. Нет никаких гарантий защиты от отрицательного изменения используемой профили. MAPI может запретить удаление используемой службы, но не запретить удалять все службы сообщений в нем. Если удалить каждую службу сообщений в профиле, все поставщики услуг в этих службах перестанут тем самым вызывать непредсказуемые результаты.
  
## <a name="in-this-section"></a>В этом разделе

[Создание профиля](creating-a-profile.md)
  
> Описывает, как создать профиль.
    
[Копирование профиля](copying-a-profile.md)
  
> Описывает, как скопировать профиль.
    
[Удаление профиля](deleting-a-profile.md)
  
> Описывает, как удалить профиль.
    
[Настройка профиля по умолчанию](setting-a-default-profile.md)
  
> Описывает, как установить профиль по умолчанию.
    
[Поиск имени профиля](finding-a-profile-name.md)
  
> Описывает, как найти имя профиля.
    
[Добавление службы сообщений](adding-a-message-service.md)
  
> Описывает, как добавить службу сообщений.
    
[Настройка службы сообщений](configuring-a-message-service.md)
  
> Описывает, как настроить службу сообщений.
    
[Копирование службы сообщений](copying-a-message-service.md)
  
> Описывает, как скопировать службу сообщений в профиль.
    
[Удаление службы сообщений](deleting-a-message-service.md)
  
> Описывает, как удалить службу сообщений.
    
[Добавление или удаление поставщиков в службе сообщений](adding-or-deleting-providers-in-a-message-service.md)
  
> Описывает, как добавлять или удалять поставщиков в службе сообщений.
    

