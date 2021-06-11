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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Чтобы добавить или удалить поставщиков услуг в службе сообщений, используйте [интерфейс IProviderAdmin: IUnknown.](iprovideradminiunknown.md) Вы можете получить **указатель IProviderAdmin,** позвонив [в службу IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). В таблице поставщиков, доступная через [IProviderAdmin::GetProviderTable,](iprovideradmin-getprovidertable.md)перечислены сведения о поставщиках услуг, установленных в службе сообщений. Клиенты и поставщики услуг могут использовать таблицу поставщика для доступа к имени DLL-файла поставщика, например, **или MAPIUID,** отображаемого имени и типа поставщика, а также сведений о службе сообщений. Дополнительные сведения см. в [таблицах поставщиков.](provider-tables.md)
  
 **Добавление или удаление поставщика услуг в службе сообщений**
  
1. Вызов метода **AdminServices для** доступа к объекту администрирования службы сообщений. 
    
2. Позвоните [в службу IMsgServiceAdmin::GetMsgServiceTable,](imsgserviceadmin-getmsgservicetable.md) чтобы получить доступ к таблице службы сообщений. 
    
3. Создайте ограничение свойств с помощью структуры [SPropertyRestriction,](spropertyrestriction.md) которая соответствует PR_DISPLAY_NAME [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)или **PR_SERVICE_NAME** [(PidTagServiceName)](pidtagservicename-canonical-property.md)с именем службы сообщений, которая должна быть изменена.  
    
4. Вызовите метод [IMAPITable::FindRow в таблице IMAPITable::FindRow,](imapitable-findrow.md) чтобы найти строку в таблице, которая представляет адресную службу сообщений. 
    
5. Позвоните [в службу IMsgServiceAdmin::AdminProviders,](imsgserviceadmin-adminproviders.md) чтобы получить **указатель IProviderAdmin.** **Передай столбец PR_SERVICE_UID** [(PidTagServiceUid)](pidtagserviceuid-canonical-property.md)из строки таблицы службы сообщений в качестве _параметра lpUID._ 
    
6. Вызов [IProviderAdmin::GetProviderTable для](iprovideradmin-getprovidertable.md) доступа к таблице поставщика. 
    
7. Создайте ограничение свойств с помощью структуры SPropertyRestriction, которая соответствует **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)или **PR_PROVIDER_DISPLAY** [(PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)с именем поставщика услуг, который будет добавлен или удален. 
    
8. Вызовите метод [IMAPITable::FindRow](imapitable-findrow.md) таблицы поставщиков, чтобы найти строку в таблице, которая представляет целевого поставщика услуг. 
    
9. Вызов [IProviderAdmin::CreateProvider,](iprovideradmin-createprovider.md) чтобы добавить поставщика или [IProviderAdmin::D eleteProvider,](iprovideradmin-deleteprovider.md) чтобы удалить его из службы сообщений. Для **CreateProvider** передайте свойство PR_DISPLAY_NAME **поставщика** в качестве _параметра lpszProvider._ Для любого метода передай свойство **PR_SERVICE_UID** поставщика в качестве _параметра lpUID._ После того, как поставщик услуг был добавлен или удален, изменение не будет очевидно до создания нового сеанса. 
    
Другой метод добавления поставщика услуг, в частности поставщика магазина сообщений, в профиль включает создание идентификатора записи для поставщика. Поскольку для создания идентификатора записи требуется знание его формата, этот метод можно использовать только в том случае, если поставщик услуг сделал формат идентификатора входа общедоступным. 
  
С помощью недавно созданного идентификатора входа клиент может вызвать [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). MAPI автоматически создает раздел профилей в профиле для поставщика услуг, но не добавляет его в службу сообщений. 
  
Некоторые службы сообщений не позволяют этому типу динамических изменений; поддерживается ли оно, является службой сообщений. Еще одна функция, которая может поддерживаться или не поддерживаться, — это возможность непосредственного доступа к закрытым разделам профилей службы сообщений. Если служба сообщений, которую вы используете, разрешает такой доступ, она опубликовывет **GUID,** который представляет частный раздел MAPISVC.INF. Этот **GUID** можно передать в [вызов iProviderAdmin::OpenProfileSection,](iprovideradmin-openprofilesection.md) чтобы получить доступ к разделу профилей. 
  

