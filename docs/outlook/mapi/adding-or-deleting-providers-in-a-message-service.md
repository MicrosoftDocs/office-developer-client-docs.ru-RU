---
title: Добавление или удаление поставщиков в службе сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44bb4d34-ca96-4d5a-93fe-85e09bd7971d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ed5ea8bdfcbdaaa6b6abd81a39f0e8df50d3b314
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433425"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>Добавление или удаление поставщиков в службе сообщений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Чтобы добавить или удалить поставщиков услуг в службе сообщений, используйте [интерфейс IProviderAdmin : IUnknown.](iprovideradminiunknown.md) Вы можете получить **указатель IProviderAdmin,** вызывая [IMsgServiceAdmin::AdminProviders.](imsgserviceadmin-adminproviders.md) Таблица поставщиков, доступная через [IProviderAdmin::GetProviderTable,](iprovideradmin-getprovidertable.md)содержит сведения о поставщиках услуг, установленных в службе сообщений. Клиенты и поставщики услуг могут использовать таблицу поставщиков для доступа к имени DLL-файла поставщика, например **MAPIUID,** отображаемого имени и типа поставщика, а также сведения о службе сообщений. Дополнительные сведения см. в [таблицах поставщиков.](provider-tables.md)
  
 **Добавление или удаление поставщика услуг в службе сообщений**
  
1. Вызовите метод **AdminServices,** чтобы получить доступ к объекту администрирования службы сообщений. 
    
2. Вызовите [IMsgServiceAdmin::GetMsgServiceTable,](imsgserviceadmin-getmsgservicetable.md) чтобы получить доступ к таблице службы сообщений. 
    
3. Создайте ограничение свойств, используя структуру [SPropertyRestriction,](spropertyrestriction.md) которая соответствует **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)или **PR_SERVICE_NAME** ([PidTagServiceName)](pidtagservicename-canonical-property.md)с именем службы сообщений, которую необходимо изменить. 
    
4. Вызовите метод [IMAPITable::FindRow](imapitable-findrow.md) таблицы службы сообщений, чтобы найти строку в таблице, которая представляет целевую службу сообщений. 
    
5. Вызовите [IMsgServiceAdmin::AdminProviders,](imsgserviceadmin-adminproviders.md) чтобы получить **указатель IProviderAdmin.** **Передав PR_SERVICE_UID** [(PidTagServiceUid)](pidtagserviceuid-canonical-property.md)из строки таблицы службы сообщений в качестве _параметра lpUID._ 
    
6. Вызовите [IProviderAdmin::GetProviderTable,](iprovideradmin-getprovidertable.md) чтобы получить доступ к таблице поставщика. 
    
7. Создайте ограничение свойств с помощью структуры SPropertyRestriction, которая соответствует **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)или **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)с именем поставщика службы, который необходимо добавить или удалить. 
    
8. Вызовите метод [IMAPITable::FindRow](imapitable-findrow.md) таблицы поставщиков, чтобы найти строку в таблице, которая представляет целевого поставщика услуг. 
    
9. Вызовите [IProviderAdmin::CreateProvider,](iprovideradmin-createprovider.md) чтобы добавить поставщика или [IProviderAdmin::D eleteProvider,](iprovideradmin-deleteprovider.md) чтобы удалить его из службы сообщений. Для **CreateProvider** передайте свойство PR_DISPLAY_NAME **поставщика** в качестве параметра _lpszProvider._ В обоих методах передав свойство **PR_SERVICE_UID** поставщика в качестве параметра _lpUID._ После того как поставщик службы был добавлен или удален, изменение не будет очевидно, пока не будет создан новый сеанс. 
    
Другой способ добавления поставщика услуг, в частности поставщика store сообщений, в профиль состоит в построении идентификатора записи для поставщика. Поскольку для создания идентификатора записи требуется знание его формата, этот метод можно использовать только в том случае, если поставщик услуг сделал формат идентификатора записи общедоступным. 
  
С помощью только что созданного идентификатора записи клиент может вызвать [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). MAPI автоматически создает раздел профиля в профиле для поставщика услуг, но не добавляет его в службу сообщений. 
  
Некоторые службы сообщений не позволяют использовать этот тип динамического изменения; независимо от того, поддерживается ли она, только служба сообщений. Другая возможность, которая может поддерживаться или не поддерживаться, — это возможность прямого доступа к разделам частного профиля службы сообщений. Если используемая служба сообщений разрешает такой доступ, она публикует **GUID,** который представляет закрытый раздел в MAPISVC.INF. Этот **GUID** можно передать в вызове [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) для доступа к разделу профиля. 
  

