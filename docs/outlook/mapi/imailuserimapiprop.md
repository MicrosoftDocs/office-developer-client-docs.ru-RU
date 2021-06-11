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
ms.openlocfilehash: a0e109fe95120483e700bab5b82f6d7cb75e2e28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436596"
---
# <a name="imailuser--imapiprop"></a>IMailUser : IMAPIProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к многим свойствам, связанным с пользователями обмена сообщениями. Интерфейс **IMailUser** реализуется объектами пользователей обмена сообщениями. **IMailUser** наследует интерфейс [IMAPIProp : IUnknown](imapipropiunknown.md) и не имеет собственных уникальных методов. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Подвергается:  <br/> |Объекты пользователей обмена сообщениями  <br/> |
|Реализовано в:  <br/> |Поставщики адресных книг  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMailUser  <br/> |
|Тип указателя:  <br/> |LPMAILUSER  <br/> |
|Модель транзакции:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

Этот интерфейс не имеет уникальных методов.
  
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)  <br/> |Чтение и запись  <br/> |
|**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |Чтение и запись  <br/> |
|**PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_EMAIL_ADDRESS** [(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)  <br/> |Чтение и запись  <br/> |
|**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_RECORD_KEY** [(PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

Пять из необходимых свойств известны как базовые свойства адресов для получателей:
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_SEARCH_KEY**
    
Эти свойства считаются особыми, так как многие другие группы аналогичных свойств построены на этой базовой группе. Другие группы используются для описания получателя в различных ролях, таких как исходный или делегированная отправитель сообщения. Дополнительные сведения об этих свойствах и о том, как их использовать, см. в дополнительных [сведениях о типах адресов MAPI.](mapi-address-types.md)
  
Пользователи обмена сообщениями могут отображать коллекцию своих свойств, **поддерживая** свойство [PR_DETAILS_TABLE (PidTagDetailsTable).](pidtagdetailstable-canonical-property.md) **PR_DETAILS_TABLE** — это таблица отображения, описываемая макет диалогового окна с деталями или страница свойства на вкладке, на которую отображаются сведения о свойстве получателей. MAPI создает диалоговые окна с подробными сведениями, когда клиент вызывает [метод IAddrBook::D etails.](iaddrbook-details.md) 
  
Объекты пользователей сообщений могут иметь другие необязательные свойства, связанные с ними. MAPI определяет множество свойств, которые предоставляют дополнительные сведения о пользователе обмена сообщениями. Все эти свойства являются строками символов. В следующем списке показаны наиболее часто используемые свойства:
  
- **PR_ACCOUNT** [(PidTagAccount)](pidtagaccount-canonical-property.md) 
    
- **PR_ASSISTANT** [(PidTagAssistant)](pidtagassistant-canonical-property.md) 
    
- **PR_BUSINESS_TELEPHONE_NUMBER** [(PidTagBusinessTelephoneNumber)](pidtagbusinesstelephonenumber-canonical-property.md) 
    
- **PR_GIVEN_NAME** [(PidTagGivenName)](pidtaggivenname-canonical-property.md) 
    
- **PR_GOVERNMENT_ID_NUMBER** [(PidTagGovernmentIdNumber)](pidtaggovernmentidnumber-canonical-property.md) 
    
- **PR_LOCALITY** [(PidTagLocality)](pidtaglocality-canonical-property.md) 
    
- **PR_POSTAL_ADDRESS** [(PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) 
    
Полный список свойств см. в списке Сопоставление имен канонических свойств [с именами MAPI.](mapping-canonical-property-names-to-mapi-names.md)
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

