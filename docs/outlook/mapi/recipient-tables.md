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
  
Таблица Recipient содержит сведения обо всех получателях сообщения. Поставщики хранилищ сообщений реализуют таблицы получателей, а клиентские приложения используют их. Клиенты обращаются к таблице получателей, выполнив вызов метода [iMessage:: жетреЦипиенттабле](imessage-getrecipienttable.md) , или если поставщик хранилища сообщений поддерживает его, в метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) . Клиенты обращаются к таблицам получателей с помощью **опенпроперти** , указывая **пр_мессаже_реЦипиентс** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) для тега свойства и иид_имапитабле для идентификатора интерфейса. Изменения в таблице получателей можно выполнить, вызвав метод [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) . 
  
Таблицы получателей имеют разный набор столбцов в зависимости от того, было ли отправлено сообщение. Следующие свойства составляют обязательный набор столбцов в таблицах получателей:
  
- **Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **Пр_реЦипиент_типе** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **Пр_ровид** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
Необязательные свойства:
  
- **Пр_дисплай_типе** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **Пр_спулер_статус** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))
    
- **Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
Отправленные сообщения должны включать следующие дополнительные свойства в требуемый набор столбцов:
  
- **Пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **Пр_респонсибилити** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
В зависимости от реализации поставщика дополнительные столбцы, такие как **пр_сендер_наме** ([PidTagSenderName](pidtagsendername-canonical-property.md)) и [EntryID](entryid.md), могут находиться в таблице.
  
Любой поставщик хранилища сообщений, поддерживающий передачу сообщений, как указано в битовом СТОРЕ_СУБМИТ_ОК, заданном в свойстве **пр_сторе_суппорт_маск** поставщика ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), должен поддерживать определенный набор ограничения в реализации таблицы получателей. Ограничения " **и**", "существует" и "Свойства" относятся к типам ограничений, которые должны быть доступны для пользователей таблицы получателей. **** Только операторы EQUAL и Not Equals должны поддерживаться в ограничении свойства. Эти ограничения должны работать со следующими свойствами:
  
- **ПР_АДДРТИПЕ**
    
- **Пр_емаил_аддресс** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **ПР_РЕЦИПИЕНТ_ТИПЕ**
    
- **ПР_РЕСПОНСИБИЛИТИ**
    
- **ПР_СПУЛЕР_СТАТУС**
    
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

