---
title: Передача прав доступа
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a863494f-0071-4d97-a6c4-26707ee00e04
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: d969fd806e5038e6c918da45041402a981554a49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808280"
---
# <a name="delegate-access"></a>Передача прав доступа

  
  
**Применимо к**: Outlook 
  
Делегирование доступа означает возможность отправить сообщение от имени другого пользователя или сообщение об ошибке для другого пользователя. Делегированный доступ — новым компонентом службы зависящего от поставщика MAPI, которая может поддерживать поставщиками транспорта, при этом они. Тем не менее для этого необходимо не поставщик. Делегированный доступ имеет значение, если это необходимо для пользователя для отправки сообщения как или фильтрации входящих сообщений для другого пользователя или когда пользователь должен доступа к хранилищу сообщение другому пользователю. Перед тем как разрешить делегированного пользователя для подключения к хранилищу другому пользователю, поставщик хранения сообщений необходимо проверить делегата на наличие соответствующих прав центра сертификации. 
  
Существует две группы свойств, которые используются для поддержки доступа делегата.
  
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
  
Для исходящих сообщений свойства **PR_SENT_REPRESENTING** идентифицирует обмена сообщениями пользователя, который должен выступать в качестве отправителя. Клиенты могут задать эти свойства в качестве альтернативного варианта. Если для свойства **PR_SENT_REPRESENTING** не задано, когда сообщение достигает поставщика транспорта этот делегат поддерживает доступ, поставщик обязан присвойте их вместе со свойствами **PR_SENDER** . 
  
Для входящих сообщений свойства **PR_RCVD_REPRESENTING** идентификации пользователя, который должен выступать в качестве получателя. Ответственность за доставки сообщений делегат поставщиками транспорта необходимо задать свойства **PR_RCVD_REPRESENTING** и **PR_RECEIVED_BY** . Клиенты, сообщение делегат следует скопировать значения свойств **PR_SENT_REPRESENTING** соответствующим свойствам **PR_RCVD_REPRESENTING** . 
  
Например предположим, что John получает света 's сообщения во время света находится в отпуске. Свойства **PR_RCVD_REPRESENTING** определение Иван как получателя делегат. Когда John отправляет ответ на сообщение, в котором он получил для света, свойств сообщений **PR_SENDER** определите John как у отправителя. Так как John будет представлять света, свойства **PR_SENT_REPRESENTING** определите света. 
  
Поставщиками, обработки входящих сообщений делегата обычно обеспечивают этих сообщений, под учетной записью пользователя обмена мгновенными сообщениями, определяемую средством **PR_SENT_REPRESENTING** свойства, а не под учетной записью пользователя, определяемую средством свойства **PR_SENDER** транспорта. Исключение — это правило — при необходимости в соответствии с принципу предоставления минимальных прав и транспорта типы доступа. В этом случае поставщика транспорта можно выбрать идентификатора отправителя. 
  
Если свойства **PR_SENT_REPRESENTING** недоступны для входящего сообщения делегата, поставщика транспорта, обработка доставки их следует настроить, используя значения соответствующих свойств **PR_SENDER** . Если свойства **PR_SENT_REPRESENTING** доступны, но поставщика транспорта не поддерживает делегированный доступ, его можно использовать свойства **PR_SENDER** для доставки. 
  

