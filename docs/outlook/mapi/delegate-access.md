---
title: Делегированный доступ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a863494f-0071-4d97-a6c4-26707ee00e04
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3d6a0eaf8ad125a0ae1ea3abb57e2aa57e0bdfe3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427264"
---
# <a name="delegate-access"></a>Делегированный доступ

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Доступ к делегированию относится к возможности пользователя отправлять сообщение в качестве другого пользователя или получать сообщение для другого пользователя. Делегатский доступ — это независимая от поставщика услуг функция MAPI, которую поставщики транспорта могут поддерживать при выборе. Однако для этого не требуется ни один поставщик. Делегатский доступ имеет важное значение, если пользователю необходимо отправлять сообщения в качестве или фильтровать входящие сообщения для другого пользователя или когда пользователь должен получить доступ к хранилище сообщений другого пользователя. Прежде чем разрешить пользователю-делегату подключаться к другому магазину, поставщик магазина сообщений должен убедиться, что пользователь делегирования имеет соответствующие полномочия. 
  
Существует две группы свойств, которые используются для поддержки доступа к делегатам:
  
 **PR_SENT_REPRESENTING_ADDRTYPE** [(PidTagSentRepresentingAddressType)](pidtagsentrepresentingaddresstype-canonical-property.md) 
  
 **PR_SENT_REPRESENTING_EMAIL_ADDRESS** [(PidTagSentRepresentingEmailAddress)](pidtagsentrepresentingemailaddress-canonical-property.md) 
  
 **PR_SENT_REPRESENTING_ENTRYID** [(PidTagSentRepresentingEntryId)](pidtagsentrepresentingentryid-canonical-property.md) 
  
 **PR_SENT_REPRESENTING_NAME** [(PidTagSentRepresentingName)](pidtagsentrepresentingname-canonical-property.md) 
  
 **PR_SENT_REPRESENTING_SEARCH_KEY** [(PidTagSentRepresentingSearchKey)](pidtagsentrepresentingsearchkey-canonical-property.md) 
  
 **PR_RCVD_REPRESENTING_ADDRTYPE** [(PidTagReceivedRepresentingAddressType)](pidtagreceivedrepresentingaddresstype-canonical-property.md) 
  
 **PR_RCVD_REPRESENTING_EMAIL_ADDRESS** [(PidTagReceivedRepresentingEmailAddress)](pidtagreceivedrepresentingemailaddress-canonical-property.md) 
  
 **PR_RCVD_REPRESENTING_ENTRYID** [(PidTagReceivedRepresentingEntryId)](pidtagreceivedrepresentingentryid-canonical-property.md) 
  
 **PR_RCVD_REPRESENTING_NAME** [(PidTagReceivedRepresentingName)](pidtagreceivedrepresentingname-canonical-property.md) 
  
 **PR_RCVD_REPRESENTING_SEARCH_KEY** [(PidTagReceivedRepresentingSearchKey)](pidtagreceivedrepresentingsearchkey-canonical-property.md) 
  
В исходяющих сообщениях  свойства PR_SENT_REPRESENTING определяют пользователя обмена сообщениями, который должен выступать в качестве отправитель. Клиенты могут установить эти свойства в качестве параметра. Если **PR_SENT_REPRESENTING** к моменту, когда сообщение достигнет транспортного поставщика, который поддерживает доступ к делегированию, поставщик  должен установить их вместе с свойствами PR_SENDER. 
  
В входящих сообщениях  свойства PR_RCVD_REPRESENTING определяют пользователя, который должен выступать в качестве получателя. Поставщики транспорта, ответственные за доставку сообщений делегатов, должны PR_RCVD_REPRESENTING **и** **PR_RECEIVED_BY** свойства. Клиенты, получающие сообщение делегата, должны **скопировать** значения свойств PR_SENT_REPRESENTING в соответствующие PR_RCVD_REPRESENTING **свойства.** 
  
Например, предположим, что Джон получает сообщения Салли, пока Салли находится в отпуске. Свойства **PR_RCVD_REPRESENTING** определяют Джона как получателя делегата. Когда Джон отправляет ответ на сообщение, полученное для Салли,  свойства PR_SENDER определяют Джона как отправитель. Так как Джон представляет Салли, **PR_SENT_REPRESENTING** свойства определяют Sally. 
  
Поставщики транспорта, которые могут обрабатывать входящие сообщения делегатов, обычно должны  доставлять **эти** сообщения в качестве пользователя обмена сообщениями, идентифицированного свойствами PR_SENT_REPRESENTING, а не как пользователь, идентифицированный PR_SENDER свойствами. Исключение из этого правила состоит в том случае, если необходимо соответствовать привилегиям доступа и типам транспорта. В этом случае поставщик транспорта может выбрать идентификатор отправки. 
  
Если свойства **PR_SENT_REPRESENTING** недоступны для входящих сообщений делегата, поставщик транспорта для обработки доставки должен установить их, используя значения соответствующих свойств **PR_SENDER.** Если **PR_SENT_REPRESENTING** доступны, но поставщик транспорта не поддерживает доступ к делегатам, он может использовать свойства PR_SENDER для доставки.  
  

