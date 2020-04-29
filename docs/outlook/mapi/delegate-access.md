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
  
Делегированный доступ — это способность пользователя отправлять сообщение от имени другого пользователя или получать сообщение для другого пользователя. Делегированный доступ — это не зависящая от поставщика функция MAPI, которую поставщики транспорта могут поддерживать, если они выбраны. Однако для этого не требуется поставщика. Делегированный доступ полезен, если необходимо, чтобы пользователь отправлял сообщения или отфильтровать входящие сообщения для другого пользователя, или когда пользователь должен получить доступ к хранилищу сообщений другого пользователя. Прежде чем разрешить представителю подключаться к магазину другого пользователя, поставщик хранилища сообщений должен проверить, что представитель пользователя имеет соответствующие полномочия. 
  
Существует две группы свойств, которые используются для поддержки делегированного доступа:
  
 **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_ADDRTYPE** ([PidTagReceivedRepresentingAddressType](pidtagreceivedrepresentingaddresstype-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_EMAIL_ADDRESS** ([PidTagReceivedRepresentingEmailAddress](pidtagreceivedrepresentingemailaddress-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md)) 
  
В исходящих сообщениях свойства **PR_SENT_REPRESENTING** идентифицируют пользователя обмена сообщениями, который должен использоваться в качестве отправителя. Клиенты могут задавать эти свойства в качестве варианта. Если свойства **PR_SENT_REPRESENTING** не заданы в момент времени, когда сообщение достигнет поставщика транспорта, поддерживающего делегированный доступ, то это обязанность поставщика, позволяющая задать их вместе со свойствами **PR_SENDER** . 
  
В входящих сообщениях свойства **PR_RCVD_REPRESENTING** идентифицируют пользователя, который должен стать получателем. Для поставщиков транспорта, которые отвечают за доставку сообщений представителей, необходимо задать свойства **PR_RCVD_REPRESENTING** и **PR_RECEIVED_BY** . Клиенты, получившие сообщение делегата, должны скопировать значения свойств **PR_SENT_REPRESENTING** в соответствующие свойства **PR_RCVD_REPRESENTING** . 
  
Например, пусть Иван получает сообщения Салли, когда Салли находится на отпуске. В свойствах **PR_RCVD_REPRESENTING** указать Иван в качестве получателя делегата. Когда Иван отправляет ответ на сообщение, полученное для Салли, свойства **PR_SENDER** сообщения определяют Иван как отправитель. Так как Джон представляет Салли, свойства **PR_SENT_REPRESENTING** определяют Салли. 
  
Поставщики транспорта, которые обрабатывают входящие сообщения делегатов, обычно должны доставлять эти сообщения в качестве пользователя обмена сообщениями, идентифицируемого **PR_SENT_REPRESENTING** свойствами, а не как пользователь, указанный в свойствах **PR_SENDER** . Исключением из этого правила является то, что оно необходимо для того, чтобы сопоставлять типы прав доступа и транспорта. В этом случае поставщик транспорта может выбрать удостоверение отправки. 
  
Если свойства **PR_SENT_REPRESENTING** недоступны для входящего сообщения делегата, то для доставки в качестве поставщика транспорта необходимо задать их, используя значения соответствующих свойств **PR_SENDER** . Если свойства **PR_SENT_REPRESENTING** доступны, но поставщик транспорта не поддерживает делегированный доступ, он может использовать свойства **PR_SENDER** для доставки. 
  

