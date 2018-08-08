---
title: Доступ к объектам с помощью сеанса
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ee20e73e5bc7bb6854b956da541d3a318a267d0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808017"
---
# <a name="accessing-objects-by-using-the-session"></a>Доступ к объектам с помощью сеанса

  
  
**Относится к**: Outlook 
  
Указатель сеанса, полученные из при вызове [MAPILogonEx](mapilogonex.md) можно использовать для доступа к множеству объектов. В следующей таблице перечислены методы, используемые для доступа к различных объектов: 
  
|**Объект**|**Метод сеанса**|
|:-----|:-----|
|Раздел профиля  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Хранение сообщений  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Адресная книга  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Объект администрирования службы сообщений  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Папка, сообщения, контейнер адресной книги, список рассылки или обмена мгновенными сообщениями пользователя  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
С помощью метода **OpenEntry** и идентификатор допустимый записи можно открыть любой адресной книги или сообщение объекта-поставщика хранилища. Существуют другие методы **OpenEntry** в MAPI, кроме метода **IMAPISession** . **OpenEntry** реализуется в следующих объектов: 
  
|**Объект**|**Способ**|
|:-----|:-----|
|Объект входа поставщик адресной книги  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Адресная книга  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Контейнер адресной книги  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Сеанс  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Хранение сообщений  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Объект входа поставщика хранилища сообщений  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Folder  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Поддержка объектов  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Некоторые методы **OpenEntry** требуется идентификатор записи объекта, чтобы открыть, как **IMAPISession::OpenEntry**; другие методы разрешить NULL должен быть указан. Идентификатор записи NULL обрабатывается по-разному в зависимости от объекта. Например при вызове **IAddrBook::OpenEntry** с идентификатором записи NULL, MAPI открывает корневой контейнер адресной книги. Метод **OpenEntry** хранилище сообщений ведет себя аналогично; она открывается в корневую папку хранилища сообщений. **IMAPIContainer::OpenEntry**, реализованный папки и контейнеров адресной книги, может вернуть MAPI_E_INVALID_PARAMETER или корневой контейнер, в зависимости от реализации. 
  
В дополнение к запрещение идентификатор записи значение NULL, метод **OpenEntry** сеанса отличается от другие методы **OpenEntry** из-за его задание не следует открыть объекты. Вместо этого проверяет идентификатор записи и перенаправляет звонок с другим методом **OpenEntry** , реализованный поставщика услуг, соответствующего. К примеру при вызове **IMAPISession::OpenEntry** с идентификатором записи сообщения, MAPI вызывает **IMSLogon::OpenEntry** метод хранилища сообщений ответственность за сообщение. 
  
В дополнение к сеансу для открытия объектов, клиенты используют его для их сравнения. Метод [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) сравнивает, сравнение их идентификаторы записей. Если [MAPIUID](mapiuid.md) структуры, содержащихся в идентификаторы записей принадлежат к поставщику услуг, MAPI перенаправляет звонок этому поставщику. **CompareEntryIDs** возвращает ошибку, если не соответствующие идентификаторы двух записей. Несмотря на то, что этот метод позволяет сравнивать идентификаторы записей, относящихся к любой тип объекта, **CompareEntryIDs** из них лучше подходит для более высокого уровня объекты, такие как хранилищ сообщений и контейнеров адресной книги. Для сравнения нижнем уровне объектов, непосредственно сравнивайте ключей поиска объектов (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) или ключи записей (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))). 
  
Как **OpenEntry** **CompareEntryIDs** реализуется несколько объектов. Выберите необходимый **OpenEntry** и **CompareEntryID** метод согласно объем сведений, у вас есть о объект или объекты открыть или по сравнению. При выборе вызываемый метод интерфейса, придерживайтесь следующих рекомендаций: 
  
- Если у вас нет сведений о целевых объектов, вызовите [IMAPISession::OpenEntry](imapisession-openentry.md) или [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md). Такой подход обеспечивает доступ к любой объект, но не самые медленные из трех.
    
- Если вы уверены, что целевых объектов адресной книги, а не, например, папки, вызовите метод [IAddrBook::OpenEntry](iaddrbook-openentry.md) или [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) . **IAddrBook::OpenEntry** открывает корневой контейнер адресной книги, если в качестве целевого объекта указано значение NULL. Такой подход обеспечивает доступ к любой объект адресной книги и быстрее, чем **IMAPISession**, но более медленными, чем использование **IMAPIContainer**.
    
- Если идентификатор записи является идентификатором краткосрочных запись или вы знаете, что целевых объектов принадлежащих контейнер определенный адресной книги или папки, вызовите метод [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) . Такой подход обеспечивает максимальное быстродействие, но обеспечивает доступ только к объектам в конкретных контейнер или папки. 
    

