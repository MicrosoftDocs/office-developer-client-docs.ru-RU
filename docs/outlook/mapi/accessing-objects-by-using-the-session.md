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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указатель сеанса, получаемый при вызове в [MAPILogonEx,](mapilogonex.md) может использоваться для доступа к различным объектам. В следующей таблице перечислены методы, используемые для доступа к различным объектам: 
  
|**Object**|**Метод сеанса**|
|:-----|:-----|
|Раздел Профиль  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Хранилище сообщений  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Адресная книга  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Объект администрирования службы сообщений  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Папка, сообщение, контейнер адресной книги, список рассылки или пользователь обмена сообщениями  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
С помощью **метода OpenEntry** и допустимого идентификатора записи можно открыть любой объект поставщика адресной книги или магазина сообщений. Существуют другие **методы OpenEntry** в MAPI, в дополнение к **методу IMAPISession.** **OpenEntry** реализуется в следующих объектах: 
  
|**Object**|**Способ**|
|:-----|:-----|
|Объект logon поставщика адресных книг  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Адресная книга  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Контейнер адресной книги  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Session  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Хранилище сообщений  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Объект logon поставщика магазина сообщений  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Folder  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Объект поддержки  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Некоторые **методы OpenEntry** требуют ввода идентификатора объекта, который должен быть открыт, как **и IMAPISession::OpenEntry;** другие методы позволяют укаварить NULL. Идентификатор записи NULL интерпретируется по-разному в зависимости от объекта. Например, при вызове **IAddrBook::OpenEntry** с идентификатором входа NULL MAPI открывает корневой контейнер адресной книги. Метод **OpenEntry** магазина сообщений ведет себя аналогично; он открывает корневую папку магазина сообщений. **IMAPIContainer::OpenEntry,** реализованный как папками, так и контейнерами адресной книги, может возвращаться MAPI_E_INVALID_PARAMETER или корневой контейнер в зависимости от реализуемого. 
  
Помимо отмены значения NULL для идентификатора записи метод **OpenEntry** сеанса отличается от других методов **OpenEntry,** так как его задача состоит не в том, чтобы открывать объекты. Вместо этого он проверяет идентификатор записи и передает вызов другому методу **OpenEntry,** реализованным соответствующим поставщиком услуг. Например, если вы вызываете **IMAPISession::OpenEntry** с идентификатором входа сообщения, MAPI вызывает **метод IMSLogon::OpenEntry** магазина сообщений, ответственный за сообщение. 
  
Помимо использования сеанса для открытия объектов клиенты используют его для сравнения. Метод [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) сравнивает объекты, сравнивая их идентификаторы записей. Если структуры [MAPIUID,](mapiuid.md) содержащиеся в идентификаторах записи, принадлежат одному поставщику услуг, MAPI передает вызов этому поставщику. **CompareEntryID возвращает** значение ошибки, если два идентификатора записи не совпадают. Хотя этот метод может сравнить идентификаторы записей, которые относятся к любому типу объекта, **CompareEntryIDs** лучше всего работает для объектов более высокого уровня, таких как хранилища сообщений и контейнеры адресной книги. Чтобы сравнить объекты нижнего уровня, сравните непосредственно клавиши поиска объектов **(PR_SEARCH_KEY** [(PidTagSearchKey))](pidtagsearchkey-canonical-property.md)или клавиши записи **(PR_RECORD_KEY** [(PidTagRecordKey)).](pidtagrecordkey-canonical-property.md) 
  
Как **и OpenEntry,** **CompareEntryID реализуется** несколькими объектами. Выберите метод **OpenEntry** и **CompareEntryID,** который следует использовать в соответствии с объемом сведений об объекте или объектах, которые необходимо открыть или сравнить. При выборе метода интерфейса используйте следующие рекомендации: 
  
- Если у вас нет сведений о целевых объектах, вызывайте [IMAPISession::OpenEntry](imapisession-openentry.md) или [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md). Этот подход позволяет получить доступ к любому объекту, но является самым медленным из трех.
    
- Если вы знаете, что целевые объекты — это записи адресной книги, а не, например, папки, позвоните в [метод IAddrBook::OpenEntry](iaddrbook-openentry.md) или [IAddrBook::CompareEntryIDs.](iaddrbook-compareentryids.md) **IAddrBook::OpenEntry** открывает корневой контейнер адресной книги, когда NULL указывается в качестве целевого объекта. Этот подход позволяет получить доступ к любому объекту адресной книги и быстрее, чем с **помощью IMAPISession,** но медленнее, чем с **помощью IMAPIContainer**.
    
- Если используемый идентификатор записи является краткосрочным идентификатором записи или если вы знаете, что целевые объекты относятся к определенному контейнеру или папке адресной книги, позвоните по методу [IMAPIContainer::OpenEntry.](imapicontainer-openentry.md) Этот подход обеспечивает максимально быструю производительность, но позволяет получать доступ только к объектам в определенном контейнере или папке. 
    

