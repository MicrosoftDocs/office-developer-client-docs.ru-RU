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
ms.openlocfilehash: a76397b74642aedf9ad5c9704735d869f61db7e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410541"
---
# <a name="accessing-objects-by-using-the-session"></a>Доступ к объектам с помощью сеанса

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указатель сеанса, получаемый при вызове [MAPILogonEx,](mapilogonex.md) можно использовать для доступа к множеству объектов. В следующей таблице перечислены методы, используемые для доступа к различным объектам: 
  
|**Object**|**Метод Session**|
|:-----|:-----|
|Раздел "Профиль"  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Хранилище сообщений  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Адресная книга  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Объект администрирования службы сообщений  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Папка, сообщение, контейнер адресной книги, список рассылки или пользователь системы обмена сообщениями  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
С помощью **метода OpenEntry** и допустимого идентификатора записи можно открыть любую адресную книгу или объект поставщика магазина сообщений. Кроме метода **IMAPISession,** в MAPI есть и другие методы **OpenEntry.** **OpenEntry** реализован в следующих объектах: 
  
|**Object**|**Способ**|
|:-----|:-----|
|Объект для логотипа поставщика адресной книги  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Адресная книга  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Контейнер адресной книги  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Сеанс  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Хранилище сообщений  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Объект для логотипа поставщика магазина сообщений  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Folder  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Объект поддержки  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Для **некоторых методов OpenEntry** требуется идентификатор записи объекта, который необходимо открыть, как и **для IMAPISession::OpenEntry;** другие методы позволяют у указанию NULL. Идентификатор записи NULL интерпретируется по-разному в зависимости от объекта. Например, при вызове **IAddrBook::OpenEntry** с идентификатором записи NULL MAPI открывает корневой контейнер адресной книги. Метод **OpenEntry** в хранилище сообщений ведет себя аналогично; Он открывает корневую папку в хранилище сообщений. **IMAPIContainer::OpenEntry,** реализованный как папками, так и контейнерами адресной книги, может возвращать MAPI_E_INVALID_PARAMETER или корневой контейнер, в зависимости от реализации. 
  
Помимо запрета значения NULL для идентификатора записи, метод **OpenEntry** сеанса отличается от других методов **OpenEntry,** так как его задача состоит в том, чтобы не открывать объекты. Вместо этого он проверяет идентификатор записи и перенаадтриет вызов на другой метод **OpenEntry,** реализованный соответствующим поставщиком услуг. Например, если вы вызываете **IMAPISession::OpenEntry** с идентификатором записи сообщения, MAPI вызывает метод **IMSLogon::OpenEntry** в хранилище сообщений, ответственном за сообщение. 
  
Помимо использования сеанса для открытия объектов, клиенты используют его для сравнения. Метод [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) сравнивает объекты, сравнивая их идентификаторы записей. Если структуры [MAPIUID,](mapiuid.md) содержащиеся в идентификаторах записей, принадлежат одному поставщику услуг, MAPI перенаададовляет вызов этому поставщику. **CompareEntryIDs** возвращает значение ошибки, если два идентификатора записи не совпадают. Хотя этот метод может сравнивать идентификаторы записей, принадлежащие любому типу объекта, **CompareEntryIDs** лучше всего работает для объектов более высокого уровня, таких как хранилища сообщений и контейнеры адресной книги. Чтобы сравнить объекты нижнего уровня, сравните непосредственно поисковые ключи объектов (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) или клавиши записи (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))). 
  
Как **и OpenEntry,** **compareEntryIDs** реализуется несколькими объектами. Выберите метод **OpenEntry** и **CompareEntryID,** который следует использовать в соответствии с объемом сведений об объекте или объектах, которые необходимо открыть или сравнить. При выборе метода интерфейса для вызова используйте следующие рекомендации: 
  
- Если у вас нет сведений о целевых объектах, вызовите [IMAPISession::OpenEntry](imapisession-openentry.md) или [IMAPISession::CompareEntryIDs.](imapisession-compareentryids.md) Этот подход обеспечивает доступ к любому объекту, но является самым медленным из трех.
    
- Если вы знаете, что целевыми объектами являются записи адресной книги, а не, например, папки, вызовите метод [IAddrBook::OpenEntry](iaddrbook-openentry.md) или [IAddrBook::CompareEntryIDs.](iaddrbook-compareentryids.md) **IAddrBook::OpenEntry** открывает корневой контейнер адресной книги, если nULL указан в качестве целевого объекта. Этот подход обеспечивает доступ к любому объекту адресной книги и быстрее, чем использование **IMAPISession,** но медленнее, чем использование **IMAPIContainer.**
    
- Если используемый идентификатор записи является краткосрочным идентификатором записи или если вы знаете, что целевые объекты принадлежат определенному контейнеру или папке адресной книги, вызовите метод [IMAPIContainer::OpenEntry.](imapicontainer-openentry.md) Этот подход обеспечивает наиболее быструю производительность, но обеспечивает доступ только к объектам в определенном контейнере или папке. 
    

