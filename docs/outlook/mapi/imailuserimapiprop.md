---
title: IMailUser IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMailUser
api_type:
- COM
ms.assetid: 74c25870-62d9-484a-9a99-4dc35c52479e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7a6971504ec8f4f5ac8593b6b78777a12ff92b3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564565"
---
# <a name="imailuser--imapiprop"></a>IMailUser : IMAPIProp

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к много свойств, связанных с системой обмена сообщениями пользователи. Интерфейс **IMailUser** реализуется системы обмена сообщениями объектов-пользователей. **IMailUser** наследует от [IMAPIProp: IUnknown](imapipropiunknown.md) интерфейс и не имеет уникальное методов свои собственные. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Предоставляемые:  <br/> |Обмен сообщениями объектов-пользователей  <br/> |
|Реализованный:  <br/> |Поставщиками адресных книг  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMailUser  <br/> |
|Тип указателя:  <br/> |LPMAILUSER  <br/> |
|Модель транзакций:  <br/> |В транзакции  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

Этот интерфейс не имеет каких-либо уникальных методов.
  
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Пять необходимые свойства называются свойствами базовый адрес для получателей:
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_SEARCH_KEY**
    
Эти свойства рассматриваются особые, поскольку количество групп свойств, аналогичное основаны на это базовая группа. Другие группы используются для описания получателя с разными ролями, такие как исходное сообщение или делегирование отправителя. Дополнительные сведения об этих свойств и как их использовать можно [Типов адресов MAPI](mapi-address-types.md).
  
Пользователи системы обмена сообщениями можно отобразить коллекцию их свойств за счет свойство **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). **PR_DETAILS_TABLE** — это таблица отображения, который описывает макет страницы с вкладками свойство, которое отображает сведения о свойствах получателей или диалоговое окно сведений. MAPI создает сведения о диалоговых окнах, если клиент вызывает метод [IAddrBook::Details](iaddrbook-details.md) . 
  
Обмен сообщениями объектов-пользователей может иметь другие дополнительные свойства, связанные с ними. MAPI определяет множество свойств, которые обеспечивают дополнительные адресации сведений о пользователе обмена мгновенными сообщениями. Все эти свойства, строк символов. В следующем списке приведены наиболее часто используемые свойства:
  
- **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) 
    
- **PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md)) 
    
- **PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md)) 
    
- **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) 
    
- **PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md)) 
    
- **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)) 
    
- **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) 
    
Полный список свойств в разделе [Сопоставление каноническое имена свойств, чтобы имена MAPI](mapping-canonical-property-names-to-mapi-names.md).
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

