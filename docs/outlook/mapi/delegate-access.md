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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Делегирование доступа означает возможность пользователя отправлять сообщение как другого пользователя или получать сообщение для другого пользователя. Делегирование доступа — это независимая от поставщика функция MAPI, которую поставщики транспорта могут поддерживать при выборе. Однако для этого не требуется ни один поставщик. Делегирование доступа полезно, если пользователю необходимо отправлять сообщения как входящие или фильтровать входящие сообщения для другого пользователя или когда пользователь должен получить доступ к хранилище сообщений другого пользователя. Прежде чем разрешить пользователю-делегату подключаться к окне другого пользователя, поставщик хранилище сообщений должен убедиться, что пользователь-делегат обладает надлежащими полномочиями. 
  
Существует две группы свойств, которые используются для поддержки делегирования доступа:
  
 **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType)](pidtagsentrepresentingaddresstype-canonical-property.md) 
  
 **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress)](pidtagsentrepresentingemailaddress-canonical-property.md) 
  
 **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId)](pidtagsentrepresentingentryid-canonical-property.md) 
  
 **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey)](pidtagsentrepresentingsearchkey-canonical-property.md) 
  
 **PR_RCVD_REPRESENTING_ADDRTYPE** ([PidTagReceivedRepresentingAddressType)](pidtagreceivedrepresentingaddresstype-canonical-property.md) 
  
 **PR_RCVD_REPRESENTING_EMAIL_ADDRESS** ([PidTagReceivedRepresentingEmailAddress)](pidtagreceivedrepresentingemailaddress-canonical-property.md) 
  
 **PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId)](pidtagreceivedrepresentingentryid-canonical-property.md) 
  
 **PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey)](pidtagreceivedrepresentingsearchkey-canonical-property.md) 
  
В исходяющих сообщениях  свойства PR_SENT_REPRESENTING определяют пользователя обмена сообщениями, который должен выступать в качестве отправитель. Клиенты могут настроить эти свойства в качестве варианта. Если **PR_SENT_REPRESENTING** к моменту достижения сообщения поставщиком транспорта, который поддерживает делегирование доступа, за их PR_SENDER отвечает поставщик.  
  
В входящих сообщениях PR_RCVD_REPRESENTING **определяет** пользователя, который должен выступать в качестве получателя. Поставщики транспорта, отвечающие за доставку сообщений-делегатов, должны PR_RCVD_REPRESENTING **и** **PR_RECEIVED_BY** сообщения. Клиенты, получающие сообщение делегата,  должны скопировать значения свойств PR_SENT_REPRESENTING в соответствующие PR_RCVD_REPRESENTING **свойства.** 
  
Например, предположим, что Иван получает сообщения от Ели в отпуске. Свойства **PR_RCVD_REPRESENTING** определяют Ивана в качестве получателя-делегата. Когда Иван отправляет ответ на сообщение, полученное для Sally,  его PR_SENDER идентифицирует Его как отправитель. Так как Иван представляет Sally, **PR_SENT_REPRESENTING** свойства определяют Sally. 
  
Поставщики транспорта, которые обработки входящих сообщений делегата обычно должны  доставить эти сообщения в качестве пользователя обмена  сообщениями, идентифицированные свойствами PR_SENT_REPRESENTING, а не как пользователь, идентифицированный свойствами PR_SENDER. Исключением из этого правила является необходимость в совпадении привилегий доступа и типов транспорта. В этом случае поставщик транспорта может выбрать отправляющий идентификатор. 
  
Если **PR_SENT_REPRESENTING** недоступны для входящих сообщений делегата, поставщик транспорта, который занимается доставкой, должен установить их, **используя** значения соответствующих PR_SENDER сообщений. Если **PR_SENT_REPRESENTING** доступны, но поставщик транспорта не поддерживает делегирование доступа,  он может использовать PR_SENDER для доставки. 
  

