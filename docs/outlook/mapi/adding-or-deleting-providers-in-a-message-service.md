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
ms.openlocfilehash: 569c9d8a7ed3f56d88d83ea6fdac4477d39e50a2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569486"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>Добавление или удаление поставщиков в службе сообщений

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Чтобы добавить или удалить поставщиков услуг службы сообщений, используйте [IProviderAdmin: IUnknown](iprovideradminiunknown.md) интерфейса. Указатель **IProviderAdmin** можно извлечь путем вызова [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). В таблице поставщика, указывающее, доступны через [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)приведены сведения о поставщиках услуг, установленные в службе сообщений. Клиенты и поставщиков услуг можно использовать в таблице поставщика для доступа к имени поставщика DLL-файла, например, или **MAPIUID**, отображаемое имя и тип поставщика, а также сведения о службе сообщений. Для получения дополнительных сведений см [Поставщика](provider-tables.md).
  
 **Для добавления или удаления поставщика услуг службы сообщений**
  
1. Вызовите метод **AdminServices** для доступа к объекту администрирования службы сообщений. 
    
2. Вызов [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) для доступа к таблице службы сообщений. 
    
3. Создание с помощью [SPropertyRestriction](spropertyrestriction.md) структуры, который соответствует **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) или **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) с именем службы сообщений для ограничения свойств изменено. 
    
4. Вызовите метод [IMAPITable::FindRow](imapitable-findrow.md) в таблице службы сообщений для найдите строку в таблице, представляющий служба целевого сообщений. 
    
5. Вызов [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) для извлечения указатель **IProviderAdmin** . Передайте в столбце **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) из строки в таблице службы сообщений и параметр _lpUID_ . 
    
6. Вызов [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) для доступа к таблице поставщика. 
    
7. Построение ограничение свойства, с помощью структуры SPropertyRestriction, которая соответствует **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) или **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) с именем поставщика услуг быть добавлено или удалено. 
    
8. Вызов метода [IMAPITable::FindRow](imapitable-findrow.md) поставщика таблицы найдите строку в таблице, который представляет целевой службы поставщика. 
    
9. Вызов [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md) для добавления к поставщику или [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md) , чтобы удалить его из службы сообщений. Для **CreateProvider**передайте свойство **PR_DISPLAY_NAME** поставщика в качестве _lpszProvider_ параметра. Для любого метода передайте свойство **PR_SERVICE_UID** поставщика в качестве _lpUID_ параметра. После поставщика услуг было добавлено или удалено, изменения не будут очевидно, пока не будет создан новый сеанс. 
    
Другой метод для добавления поставщика услуг, в частности поставщика хранилища сообщений, в профиль включает создание идентификатор записи для поставщика. Так как создав запись идентификатора требует знания его формат, этот метод может использоваться только если поставщик услуг внес его формат идентификатора записи общедоступной. 
  
С идентификатором нового созданного запись клиент может вызвать [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). MAPI автоматически создает профиля в профиле для поставщика услуг, но не добавляйте к службе сообщений. 
  
Некоторые службы сообщений не разрешать этот тип динамического изменения; поддерживается ли зависит от службы сообщений. Другого компонента, который может не поддерживаться является возможность для прямого доступа к разделах личного профиля службы сообщений. Служба сообщений, которую вы используете позволяет получить, опубликовать **идентификатор GUID** , который представляет закрытый раздел в MAPISVC.INF. Вы можете передать этот **идентификатор GUID** в вызове [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) для доступа к разделу профилей. 
  

