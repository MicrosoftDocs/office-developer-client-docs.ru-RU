---
title: SMTP-адреса
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 655d48d1ea937659f85e0ef7379425759ea7e256
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591361"
---
# <a name="smtp-addresses"></a>SMTP-адреса

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Формат адреса электронной почты SMTP определен в RFC 822. Компоненты MAPI должен обрабатывать любого адреса, соответствующие этому стандарту. Однако существует определенной формы RFC 822 адрес, который лучше всего кодирует MAPI адреса:
  
 _отображаемое имя_ **\<** _адрес электронной почты_**\>**
  
Угловые скобки включены в качестве литералов. Пустые ячейки являются стандартными в отображаемые имена; они должны не заключаться в кавычки. Типичная адрес может выглядеть эта команда, которая относится к одному из соавторов RFC 1521:
  
Nathaniel Borenstein \<nsb@bellcore.com\>
  
Если отображаемое имя содержит символы, которые имеют особое значение в SMTP-адреса, такие как \< или @, всей отображаемое имя должно заключаться в двойные кавычки. На исходящей почты Если общая длина адрес электронной почты и отображения имя содержит более 255 символов, отображаемое имя должны быть удалены.
  
Части SMTP-адрес сопоставления свойств MAPI следующим образом:
  
|**Компонент адрес SMTP**|**Свойство MAPI**|
|:-----|:-----|
| _отображаемое имя_ для всех получателей  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _отображаемое имя_ из поля  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _отображаемое имя_ поля отправителя  <br/> |**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _адрес электронной почты_ <br/> |**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|неявные, всегда «SMTP»  <br/> |**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
Если не отображаемое имя для адреса в входящей почты, должен использоваться адрес электронной почты всей. Тип адреса всегда является SMTP.
  
Свойствами получателя, взяты из таблицы получателей сообщения MAPI. свойства отправителя, взяты из сообщения.
  

