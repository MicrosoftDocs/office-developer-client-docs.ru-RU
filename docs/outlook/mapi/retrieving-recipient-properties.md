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
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a>Доступ к одному или более свойствам записи адресной книги
  
1. Для каждой интересующих вас записей адресной книги вызовите [IAddrBook::OpenEntry,](iaddrbook-openentry.md)передав идентификатор записи целевого пользователя обмена сообщениями или списка рассылки.
    
2. Затем сделайте одно из следующих:
    
   - Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) пользователя или списка рассылки для каждой интересующих вас адресных книг со списком свойств, которые необходимо получить. 
    
   - Вызовите [IAddrBook::P repareRecips, передав](iaddrbook-preparerecips.md)структуру [ADRLIST,](adrlist.md) которая содержит все свойства для всех нужных записей адресной книги. Так как один вызов **PrepareRecips** может возвращать сведения о нескольких записях адресной книги, это предпочтительный вариант, если вас интересует несколько получателей. 
    

