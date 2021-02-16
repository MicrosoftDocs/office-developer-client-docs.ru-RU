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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Администрирование профилей и служб сообщений может включать создание новых профилей, удаление старых профилей и изменение содержимого существующих профилей путем изменения служб сообщений и содержащихся в них поставщиков услуг. Не все клиенты поддерживают администрирование профилей и служб сообщений в качестве стандартных функций. Некоторые клиенты не имеют ничего больше общего с профилями, чем позволяют пользователям выбирать их во время логотипа.
  
Если вы поддерживаете администрирование профиля или службы сообщений, скорее всего, вы будете использовать следующие интерфейсы, реализованные с помощью MAPI:
  
- [IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) для администрирования службы сообщений в профиле, доступном через [IMAPISession::AdminServices](imapisession-adminservices.md) или [IProfAdmin::AdminServices](iprofadmin-adminservices.md). Клиенты обмена сообщениями обычно звонят **по IMAPISession,** когда клиенты конфигурации или клиенты, которые не отправляют и не получают сообщения, звонят **в IProfAdmin.** По возможности вызовите метод **IProfAdmin,** так как он не вызывает службу сообщений. Дополнительные сведения об использовании интерфейса **IMsgServiceAdmin** [](configuring-a-message-service.md)см. в следующих темах: "Настройка службы сообщений", [](copying-a-message-service.md)"Копирование службы сообщений" и "Удаление [службы сообщений".](deleting-a-message-service.md)
    
- [IProfAdmin : IUnknown](iprofadminiunknown.md) для администрирования профиля, доступного через [функцию MAPIAdminProfiles.](mapiadminprofiles.md) Дополнительные сведения об использовании интерфейса **IProfAdmin** см. в следующих [](copying-a-profile.md) [темах:](creating-a-profile-by-using-custom-code.md)"Создание профиля с помощью пользовательского кода", "Копирование профиля", [](deleting-a-profile.md)"Удаление профиля", [](finding-a-profile-name.md)"Поиск имени профиля" и "Настройка профиля по умолчанию". [](setting-a-default-profile.md)
    
- [IProfSect : IMAPIProp](iprofsectimapiprop.md) для обслуживания свойств в разделе профиля, доступном с помощью [метода IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) или [IProviderAdmin::OpenProfileSection.](iprovideradmin-openprofilesection.md) Дополнительные сведения о разделах профилей см. в [разделах "Профили MAPI".](mapi-profiles.md)
    
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md) для администрирования поставщиков услуг в службе сообщений, доступной через [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). Дополнительные сведения об использовании интерфейса **IProviderAdmin** см. в подпрограмме "Добавление или удаление поставщиков [в службе сообщений".](adding-or-deleting-providers-in-a-message-service.md)
    
Будьте осторожны при поддержке администрирования профилей и служб сообщений. Не существует мер защиты от отрицательного изменения используемой профили. MAPI может предотвратить удаление используемой службы сообщений, но не может предотвратить удаление всех служб сообщений в нем. Если удалить все службы сообщений в профиле, все поставщики служб в этих службах перестанут таким образом вызывать непредсказуемые результаты.
  
## <a name="in-this-section"></a>В этом разделе:

[Создание профиля](creating-a-profile.md)
  
> Описывает создание профиля.
    
[Копирование профиля](copying-a-profile.md)
  
> Описывает копирование профиля.
    
[Удаление профиля](deleting-a-profile.md)
  
> Описывает удаление профиля.
    
[Настройка профиля по умолчанию](setting-a-default-profile.md)
  
> Описывается, как установить профиль по умолчанию.
    
[Поиск имени профиля](finding-a-profile-name.md)
  
> Описывает, как найти имя профиля.
    
[Добавление службы сообщений](adding-a-message-service.md)
  
> Описывается добавление службы сообщений.
    
[Настройка службы сообщений](configuring-a-message-service.md)
  
> Описывает настройку службы сообщений.
    
[Копирование службы сообщений](copying-a-message-service.md)
  
> Описывается копирование службы сообщений в профиль.
    
[Удаление службы сообщений](deleting-a-message-service.md)
  
> Описывается, как удалить службу сообщений.
    
[Добавление или удаление поставщиков в службе сообщений](adding-or-deleting-providers-in-a-message-service.md)
  
> Описывается добавление или удаление поставщиков в службе сообщений.
    

