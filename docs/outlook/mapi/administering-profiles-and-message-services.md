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
ms.openlocfilehash: 124f4875834e035e29d4c63e52789bf07f18258d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587546"
---
# <a name="administering-profiles-and-message-services"></a>Администрирование профилей и служб сообщений

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Профиль и администрирование службы может включать в себя создание новых профилей, удаление старых профилей и изменения содержимого существующих профилей с помощью изменения службы сообщений и поставщиков услуг, содержащихся в них сообщения. Не все клиенты поддерживают администрирование службы профилей и сообщение как стандартные функции. Некоторые клиенты не более с профилями, не позволять пользователям выбрать один во время входа в систему.
  
Если вы поддерживаете администрирования службы профиля или сообщения, скорее всего, будет использоваться следующие интерфейсы, которые реализуются MAPI:
  
- [IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) для администрирования службы сообщений в профиле через [IMAPISession::AdminServices](imapisession-adminservices.md) или [IProfAdmin::AdminServices](iprofadmin-adminservices.md). Клиенты обмена сообщениями вызов **IMAPISession** во время настройки клиентов или клиентов, которые не отправлять и получать сообщения, вызова **IProfAdmin**. По возможности, вызовите метод **IProfAdmin** , так как он не вызывает сообщения службу для запуска. Дополнительные сведения об использовании интерфейса **IMsgServiceAdmin** в следующих разделах: [Настройка службы сообщений](configuring-a-message-service.md), [скопировав службы сообщений](copying-a-message-service.md)и [Удаление службы сообщений](deleting-a-message-service.md).
    
- [IProfAdmin: IUnknown](iprofadminiunknown.md) для администрирования профиля, можно использовать функцию [MAPIAdminProfiles](mapiadminprofiles.md) . Дополнительные сведения об использовании интерфейса **IProfAdmin** в следующих разделах: [Создание профилей с помощью пользовательский код](creating-a-profile-by-using-custom-code.md), [Копирование профиля](copying-a-profile.md), [Удаление профиля](deleting-a-profile.md), [Поиск имени профиля](finding-a-profile-name.md)и [параметр По умолчанию профиль](setting-a-default-profile.md).
    
- [IProfSect: IMAPIProp](iprofsectimapiprop.md) на обслуживание свойства в разделе профилей, можно использовать метод [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) или [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) . Дополнительные сведения о разделах профиля можно [Профили MAPI](mapi-profiles.md).
    
- [IProviderAdmin: IUnknown](iprovideradminiunknown.md) для администрирования поставщиков услуг службы сообщений, можно использовать [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). Дополнительные сведения об использовании интерфейса **IProviderAdmin** можно [Добавление или удаление поставщиков службы сообщений](adding-or-deleting-providers-in-a-message-service.md).
    
Будьте внимательны, чтобы в вашей поддержки администрирования службы профилей и сообщения. Существует не меры безопасности для защиты от отрицательно изменения профиля, который используется. MAPI можно запретить удаление профиля используется, но не можете запретить пользователям удаление каждая служба сообщения в нем. При удалении каждая служба сообщения в профиль всех поставщиков услуг в эти службы остановит, приводящую к непредсказуемым последствиям будет выполнена.
  
## <a name="in-this-section"></a>В этой статье

[Создание профиля](creating-a-profile.md)
  
> Описывается, как создать профиль.
    
[Копирование профиля](copying-a-profile.md)
  
> Описывается, как скопировать профиль.
    
[Удаление профиля](deleting-a-profile.md)
  
> Описывается, как удалить профиль.
    
[Установка профиля по умолчанию](setting-a-default-profile.md)
  
> В данной статье описывается настройка профиля по умолчанию.
    
[Поиск имени профиля](finding-a-profile-name.md)
  
> Описывается, как найти имя профиля.
    
[Добавление службы сообщений](adding-a-message-service.md)
  
> В данной статье описывается добавление службы сообщений.
    
[Настройка службы сообщений](configuring-a-message-service.md)
  
> В данной статье описывается настройка службы сообщений.
    
[Копирование службы сообщений](copying-a-message-service.md)
  
> Описание копирования службы сообщений в профиль.
    
[Удаление службы сообщений](deleting-a-message-service.md)
  
> В данной статье описывается удаление службы сообщений.
    
[Добавление или удаление поставщиков в службе сообщений](adding-or-deleting-providers-in-a-message-service.md)
  
> Описывается, как добавлять или удалять поставщиков службы сообщений.
    

