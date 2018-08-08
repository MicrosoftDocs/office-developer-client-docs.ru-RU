---
title: IDistList IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IDistList
api_type:
- COM
ms.assetid: bd8e1ddb-3027-428b-8964-81614f80282d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7fee3c84d6a4d4a94397f5197f45637b0c7dd2be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808810"
---
# <a name="idistlist--imapicontainer"></a>IDistList : IMAPIContainer

  
  
**Относится к**: Outlook 
  
Предоставляет доступ к списки рассылки в поле можно изменить адрес книги контейнеров. **IDistList** создание, копирование и удаление списков рассылки, кроме разрешения имен. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Предоставляемые:  <br/> |Объекты списка рассылки  <br/> |
|Реализованный:  <br/> |Поставщиками адресных книг  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IDistList  <br/> |
|Тип указателя:  <br/> |LPDISTLIST  <br/> |
|Модель транзакций:  <br/> |В транзакции  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

Этот интерфейс не имеет каких-либо уникальных методов.
  
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Интерфейс **IDistList** наследует от [IMAPIContainer](imapicontainerimapiprop.md) и включает в себя идентичные методам как контейнеры адресной книги. Таким образом так как методы интерфейса **IDistList** , совпадают интерфейса [IABContainer](iabcontainerimapicontainer.md) , они не повторяются здесь. 
  
Список рассылки или объект, который реализует **IDistList** является коллекция обмена сообщениями объектов-пользователей или отдельных получателей. Список рассылки может состоять из всех, объектов пользователей обмена мгновенными сообщениями, или некоторые обмена сообщениями пользователя и некоторые списки рассылки. 
  
Как правило, существует два типа списков рассылки:
  
- Списки рассылки, которые развертываются с базовым системы обмена сообщениями. Этот тип списка с адресом **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) и является обрабатывается так же, как для отдельного получателя. 
    
- Списки рассылки, существующих в локальном контейнере и расширенное клиентским приложением.
    
Свойства списка рассылки необязательно относятся следующие:
  
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) 
    
- **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) 
    
Обратите внимание на то, что **PR_ADDRTYPE** является обязательным, но не является **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)). Вот так, как в список рассылки без адрес электронной почты по-прежнему могут получать сообщения, но необходимо развернуть список ее участников. Если свойство **PR_ADDRTYPE** MAPIPDL, MAPI выполняет развертывание. Если **PR_ADDRTYPE** значение, отличное от MAPIPDL, поставщика транспорта выполняет развертывание. 
  
Для получения дополнительных сведений о том, как использовать методы **IDistList** просмотра операций ссылку для параллельного методы **IABContainer**.
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

