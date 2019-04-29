---
title: Имаилусер IMAPIProp
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ ко многим свойствам, связанным с пользователями обмена сообщениями. Интерфейс **имаилусер** реализуется объектами пользователя обмена сообщениями. **Имаилусер** наследуется от интерфейса [IMAPIProp: IUnknown](imapipropiunknown.md) и не обладает уникальными методами. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Предоставлено:  <br/> |Объекты пользователя для обмена сообщениями  <br/> |
|Реализовано в:  <br/> |Поставщики адресных книг  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_имаилусер  <br/> |
|Тип указателя:  <br/> |ЛПМАИЛУСЕР  <br/> |
|Модель транзакции:  <br/> |Транзакции  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

У этого интерфейса нет уникальных методов.
  
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**Пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**Пр_дисплай_типе** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_емаил_аддресс** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_сеарч_кэй** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

Пять обязательных свойств называются свойствами базового адреса для получателей:
  
- **ПР_АДДРТИПЕ**
    
- **ПР_ДИСПЛАЙ_НАМЕ**
    
- **ПР_ЕМАИЛ_АДДРЕСС**
    
- **PR_ENTRYID**
    
- **PR_SEARCH_KEY**
    
Эти свойства считаются особыми, так как многие другие группы схожих свойств создаются на основе этой базовой группы. Другие группы используются для описания получателя в различных ролях, таких как исходный или представительный отправитель сообщения. Дополнительные сведения об этих свойствах и способах их использования приведены в разделе [типы адресов MAPI](mapi-address-types.md).
  
Пользователи обмена сообщениями могут отображать коллекцию их свойств, поддерживающих свойство **пр_детаилс_табле** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). **Пр_детаилс_табле** — это отображаемая таблица, в которой описывается макет диалогового окна сведения или вкладка свойств, отображающая сведения о свойствах получателей. MAPI создает диалоговые окна сведений, когда клиент вызывает метод [IAddrBook::D етаилс](iaddrbook-details.md) . 
  
Пользовательские объекты обмена сообщениями могут иметь другие связанные с ними дополнительные свойства. MAPI определяет множество свойств, которые предоставляют дополнительные сведения об адресе пользователя для обмена сообщениями. Все эти свойства являются символьными строками. В следующем списке приведены наиболее часто используемые свойства:
  
- **Пр_аккаунт** ([PidTagAccount](pidtagaccount-canonical-property.md)) 
    
- **Пр_ассистант** ([PidTagAssistant](pidtagassistant-canonical-property.md)) 
    
- **Пр_бусинесс_телефоне_нумбер** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md)) 
    
- **Пр_гивен_наме** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) 
    
- **Пр_говернмент_ид_нумбер** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md)) 
    
- **Пр_локалити** ([PidTagLocality](pidtaglocality-canonical-property.md)) 
    
- **Пр_постал_аддресс** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) 
    
Полный список свойств приведен [в разделе Сопоставление канонИческих имен свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md).
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

