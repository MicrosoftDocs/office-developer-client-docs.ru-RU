---
title: Таблицы получателей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cc7635c474b99898d59589f33fcf06cf24697378
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812099"
---
# <a name="recipient-tables"></a>Таблицы получателей

  
  
**Относится к**: Outlook 
  
Получателей таблица содержит сведения о всех получателей сообщения. Поставщики хранилища сообщений реализации получателей таблиц и их использования для клиентских приложений. Клиенты получить доступ к таблице получателей, вызвав метод [IMessage::GetRecipientTable](imessage-getrecipienttable.md) или если поставщик хранилища сообщения его поддерживает метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) . Для доступа клиентов к получателей таблицы с **OpenProperty** путем указания для свойства tag и IID_IMAPITable **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) для идентификатора интерфейса. Путем вызова метода [IMessage::ModifyRecipients](imessage-modifyrecipients.md) можно внесены изменения в таблицу получателей. 
  
Получателей таблицы имеют набор в зависимости от того, является ли сообщение отправлено различных столбцов. Следующие свойства составляют обязательный столбец, задайте в таблицах получателей:
  
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
Необязательный условий.
  
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
Отправленных сообщений должен включать дополнительные свойства в их набор необходимых столбцов:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
В зависимости от реализации поставщика для дополнительных столбцов, такие как **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) и [ENTRYID](entryid.md), возможно, в таблице.
  
Любой поставщика хранилища сообщений, поддерживающего передачи сообщений — как указано в STORE_SUBMIT_OK бит в свойстве поставщика **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) — следует обеспечивают поддержку для определенного набора ограничения в реализации получателей в таблице. **И**, **или**, существует и ограничений свойств являются между типами ограничения, которые должны быть доступны пользователям получателей в таблице. Только операторы равно и не равно должны поддерживаться в ограничении свойства. Эти ограничения должны работать со следующими свойствами:
  
- **PR_ADDRTYPE**
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_RECIPIENT_TYPE**
    
- **PR_RESPONSIBILITY**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

