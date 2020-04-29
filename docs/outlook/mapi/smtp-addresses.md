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
ms.openlocfilehash: fb4402100891df8b27c8d26900a4acd05f4183e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419627"
---
# <a name="smtp-addresses"></a>SMTP-адреса

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Формат SMTP-адресов электронной почты определен в RFC 822. Компоненты MAPI должны обрабатывать любой адрес, который соответствует этому стандарту. Тем не менее, существует определенная форма адреса RFC 822, которая наилучшим образом кодирует адреса MAPI:
  
 _адрес электронной почты_ для _отображения имени_ **\<****\>**
  
Угловые скобки включены как литералы. Пустые ячейки часто используются в отображаемых именах; их не нужно заключать в кавычки. Типичный адрес может выглядеть следующим образом, который относится к одному из соавторов RFC 1521:
  
Насаниел Боренстеин \<NSB@bellcore.com\>
  
Если отображаемое имя содержит символы, которые имеют особое значение в SMTP-адресах \< , например, или @, то полное отображаемое имя должно быть заключено в двойные кавычки. В случае исходящей почты, если общая длина адреса электронной почты и отображаемого имени превышает 255 символов, отображаемое имя необходимо удалить.
  
Части карты SMTP-адресов в свойства MAPI следующим образом:
  
|**Компонент SMTP-адреса**|**Свойство MAPI**|
|:-----|:-----|
| _Отображение имен_ для всех получателей  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _отобразить — имя_ для поля "от"  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _Отображение — имя_ для поля "отправитель"  <br/> |**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _адрес электронной почты_ <br/> |**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|неявный, всегда "SMTP"  <br/> |**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
Если для адреса в входящей почте нет отображаемого имени, будет использоваться весь адрес электронной почты. Типом адреса всегда является SMTP.
  
Свойства получателей берутся из таблицы получателей сообщения MAPI; Свойства отправителя берутся из самого сообщения.
  

