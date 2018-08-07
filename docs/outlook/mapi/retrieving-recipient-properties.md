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
ms.openlocfilehash: a7bdcf133b8b2b5d8eb906cc0f5b5803838e27a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812139"
---
# <a name="retrieving-recipient-properties"></a>Извлечение свойств получателя
  
**Относится к**: Outlook 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>Для доступа к одного или нескольких свойств записи адресной книги
  
1. Для каждой записи адресной книги интересов вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md), передав идентификатор записи конечного пользователя или список рассылки системы обмена сообщениями.
    
2. Затем выполните одно из следующих действий.
    
   - Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) списка рассылки или обмена мгновенными сообщениями пользователя для каждой записи адресной книги интересов, со списком одно или несколько свойств для извлечения. 
    
   - Вызовите [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), передав структуру [ADRLIST](adrlist.md) , в котором содержатся все свойства для всех записей желаемую адресной книги. Так как один вызов **PrepareRecips** можно получить сведения о нескольких адрес записей книги, это предпочтительными стратегии, когда вы заинтересованы в нескольких получателей. 
    

