---
title: Получение свойств получателя
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 38063cebe70b153decce6713ac5fc31d6916dbf6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426676"
---
# <a name="retrieving-recipient-properties"></a>Получение свойств получателя
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>Доступ к одному или нескольким свойствам записи адресной книги
  
1. Для каждой интересующей записи адресной книги вызовите [IAddrBook:: OpenEntry](iaddrbook-openentry.md), передав идентификатор записи целевого пользователя обмена сообщениями или списка рассылки.
    
2. Затем выполните одно из следующих действий.
    
   - ВыЗовите метод [IMAPIProp::](imapiprop-getprops.md) -PROPS для каждой интересующей записи адресной книги со списком одного или нескольких извлекаемых свойств. 
    
   - Call [IAddrBook::P репаререЦипс](iaddrbook-preparerecips.md), передающий структуру [ADRLIST](adrlist.md) , в которой хранятся все свойства всех нужных записей адресной книги. Так как один вызов **препаререЦипс** может возвращать сведения о нескольких записях адресных книг, это предпочтительная стратегия, когда вы заинтересованы в нескольких получателях. 
    

