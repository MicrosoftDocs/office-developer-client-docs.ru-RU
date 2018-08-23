---
title: Извлечение свойств получателя
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a48c6a8e043062bc6b48e09934fded1dccb507b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585439"
---
# <a name="retrieving-recipient-properties"></a>Извлечение свойств получателя
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>Для доступа к одного или нескольких свойств записи адресной книги
  
1. Для каждой записи адресной книги интересов вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md), передав идентификатор записи конечного пользователя или список рассылки системы обмена сообщениями.
    
2. Затем выполните одно из следующих действий.
    
   - Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) списка рассылки или обмена мгновенными сообщениями пользователя для каждой записи адресной книги интересов, со списком одно или несколько свойств для извлечения. 
    
   - Вызовите [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), передав структуру [ADRLIST](adrlist.md) , в котором содержатся все свойства для всех записей желаемую адресной книги. Так как один вызов **PrepareRecips** можно получить сведения о нескольких адрес записей книги, это предпочтительными стратегии, когда вы заинтересованы в нескольких получателей. 
    

