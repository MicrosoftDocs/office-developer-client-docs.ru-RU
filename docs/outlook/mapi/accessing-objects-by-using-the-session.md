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
  
Указатель сеанса, полученный из вызова [мапилогонекс](mapilogonex.md) , можно использовать для доступа к широкому спектру объектов. В следующей таблице перечислены методы, которые используются для доступа к различным объектам: 
  
|**Object**|**Метод Session**|
|:-----|:-----|
|Раздел профиля  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Хранилище сообщений  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Адресная книга  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Объект администрирования службы сообщений  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Папка, сообщение, контейнер адресной книги, список рассылки или пользователь обмена сообщениями  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
С помощью метода **OpenEntry** и допустимого идентификатора записи можно открыть любую адресную книгу или объект поставщика хранилища сообщений. В дополнение к методу **IMAPISession** существуют и другие методы **OpenEntry** . **OpenEntry** реализован в следующих объектах: 
  
|**Object**|**Метод**|
|:-----|:-----|
|Объект входа поставщика адресных книг  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Адресная книга  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Контейнер адресной книги  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Сеанс  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Хранилище сообщений  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Объект входа поставщика хранилища сообщений  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Folder  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Объект support  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Некоторым методам **OpenEntry** требуется идентификатор записи объекта, который должен быть открыт, как **IMAPISession:: OpenEntry**; другие методы позволяют указать значение NULL. Идентификатор записи NULL интерпретируется по-разному в зависимости от объекта. Например, при вызове **IAddrBook:: OpenEntry** с идентификатором записи NULL MAPI открывает корневой контейнер адресной книги. Метод **OpenEntry** хранилища сообщений аналогичен; откроется корневая папка хранилища сообщений. **IMAPIContainer:: OpenEntry**, реализованный обеими папками и контейнерами адресной книги, может возвращать MAPI_E_INVALID_PARAMETER или корневой контейнер в зависимости от реализации. 
  
В дополнение к запрету значения NULL для идентификатора записи метод **OpenEntry** сеанса отличается от других методов **OpenEntry** , так как его задание не открывает объекты. Вместо этого он проверяет идентификатор записи и перенаправляет вызов другому методу **OpenEntry** , реализованному соответствующим поставщиком услуг. Например, при вызове **IMAPISession:: OpenEntry** с идентификатором записи сообщения MAPI вызывает метод **Имслогон:: OpenEntry** банка сообщений, ответственного за сообщение. 
  
В дополнение к открытию объектов с помощью сеанса клиенты используют их для сравнения. Метод [IMAPISession:: метод compareentryids](imapisession-compareentryids.md) сравнивает объекты, сравнивая их идентификаторы записей. Если структуры [мапиуид](mapiuid.md) , содержащиеся в идентификаторах записей, принадлежат одному поставщику услуг, MAPI пересылает вызов этому поставщику. **Метод compareentryids** возвращает значение ошибки, если два идентификатора записи не совпадают. Несмотря на то, что этот метод может сравнивать идентификаторы записей, принадлежащие любому типу объекта, **метод compareentryids** лучше всего подходит для объектов более высокого уровня, таких как хранилища сообщений и контейнеры адресной книги. Для сравнения объектов нижнего уровня Сравните непосредственно с ключами поиска (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) или клавиши записи (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))). 
  
Как и **OpenEntry**, **метод compareentryids** реализовано несколькими объектами. Выберите метод **OpenEntry** и **компаринтрид** , который будет использоваться в соответствии с количеством сведений, о котором вы хотите открыть или сравнить объект. При выборе метода интерфейса для вызова необходимо придерживаться следующих рекомендаций. 
  
- Если отсутствуют сведения о целевых объектах, вызовите метод [IMAPISession:: OpenEntry](imapisession-openentry.md) или [IMAPISession:: метод compareentryids](imapisession-compareentryids.md). Такой подход обеспечивает доступ к любому объекту, но является самым медленным из трех.
    
- Если вы знаете, что целевые объекты являются записями адресной книги, а не, например, папками, вызовите метод [IAddrBook:: OpenEntry](iaddrbook-openentry.md) или [IAddrBook:: метод compareentryids](iaddrbook-compareentryids.md) . **IAddrBook:: OpenEntry** открывает корневой контейнер адресной книги, если в качестве целевого объекта ЗАДАНО значение null. Такой подход обеспечивает доступ к любому объекту адресной книги и работает быстрее, чем при использовании **IMAPISession**, но медленнее, чем использование **IMAPIContainer**.
    
- Если используемый идентификатор записи является коротким идентификатором записи или если известно, что целевые объекты относятся к определенному контейнеру или папке адресной книги, вызовите метод [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) . Такой подход дает наибольшую производительность, но обеспечивает доступ только к объектам в определенном контейнере или папке. 
    

