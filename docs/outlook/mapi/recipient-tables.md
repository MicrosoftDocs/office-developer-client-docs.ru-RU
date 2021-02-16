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
ms.openlocfilehash: 8950623308e85de1d239deb322f65ee867a33ca0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437289"
---
# <a name="recipient-tables"></a>Таблицы получателей

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Таблица получателей содержит сведения обо всех получателях сообщения. Поставщики store сообщений реализуют таблицы получателей, а клиентские приложения используют их. Клиенты получают доступ к таблице получателей, звоня [методу IMessage::GetRecipientTable](imessage-getrecipienttable.md) или, если поставщик хранимых сообщений поддерживает ее, [методУ IMAPIProp::OpenProperty.](imapiprop-openproperty.md) Клиенты имеют доступ к таблицам  получателей с помощью **OpenProperty,** указав PR_MESSAGE_RECIPIENTS ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)для тега свойства и IID_IMAPITable для идентификатора интерфейса. Изменения таблицы получателей можно внести с помощью вызова метода [IMessage::ModifyRecipients.](imessage-modifyrecipients.md) 
  
Таблицы получателей имеют другой набор столбцов в зависимости от того, было ли сообщение отправлено. Следующие свойства составляют необходимый набор столбцов в таблицах получателей:
  
- **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)
    
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType)](pidtagrecipienttype-canonical-property.md)
    
- **PR_ROWID** ([PidTagRowid)](pidtagrowid-canonical-property.md)
    
Дополнительные свойства:
  
- **PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)
    
- **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)
    
- **PR_SPOOLER_STATUS** ([PidTagSpoolerStatus)](pidtagspoolerstatus-canonical-property.md)
    
- **PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)
    
Отправленные сообщения должны включать следующие дополнительные свойства в требуемом наборе столбцов:
  
- **PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)
    
- **PR_RESPONSIBILITY** ([PidTagResponsibility)](pidtagresponsibility-canonical-property.md)
    
В зависимости от реализации поставщика в таблице могут быть дополнительные столбцы, например **PR_SENDER_NAME** [(PidTagSenderName)](pidtagsendername-canonical-property.md)и [ENTRYID.](entryid.md)
  
Любой поставщик хранилищ сообщений, который поддерживает передачу сообщений ( как указано в бите STORE_SUBMIT_OK, задаваемом в свойстве **PR_STORE_SUPPORT_MASK** поставщика [(PidTagStoreSupportMask),](pidtagstoresupportmask-canonical-property.md)должен поддерживать определенный набор ограничений в реализации таблицы получателей. Ограничения **AND**, **OR**, существуют и ограничения свойств являются одними из типов ограничений, которые должны быть доступны для пользователей таблиц получателей. Ограничение свойств должно поддерживать только операторы "равное" и "не равное". Эти ограничения должны работать со следующими свойствами:
  
- **PR_ADDRTYPE**
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress)](pidtagemailaddress-canonical-property.md) 
    
- **PR_RECIPIENT_TYPE**
    
- **PR_RESPONSIBILITY**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

