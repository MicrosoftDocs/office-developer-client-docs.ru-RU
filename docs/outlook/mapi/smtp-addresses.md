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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Формат адресов электронной почты SMTP определяется в RFC 822. Компоненты MAPI должны обрабатывать любой адрес, который соответствует этому стандарту. Однако существует определенная форма адреса RFC 822, который лучше всего кодирует АДРЕСА MAPI:
  
 _display-name_ **\<** _адрес электронной почты_**\>**
  
Угловые скобки включены в качестве литералов. Пробелы являются распространенными в именах отображения; их не нужно цитировать. Типичный адрес может выглядеть как этот, который принадлежит одному из соавторов RFC 1521:
  
Натаниэль \< Боренштейн nsb@bellcore.com\>
  
Если имя отображения содержит символы, которые имеют особое значение в SMTP-адресах, например или @, все имя отображения должно быть заключено в \< двойные кавычка. При исходящую почту, если общая длина адреса электронной почты плюс имя отображения превышает 255 символов, имя отображения должно быть отброшено.
  
Части адресной карты SMTP в свойства MAPI следующим образом:
  
|**Компонент адресов SMTP**|**Свойство MAPI**|
|:-----|:-----|
| _отображение имени_ для всех получателей  <br/> |**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |
| _display-name_ for From field  <br/> |**PR_SENDER_NAME** [(PidTagSenderName)](pidtagsendername-canonical-property.md)  <br/> |
| _display-name_ для поля Отправитель  <br/> |**PR_SENT_REPRESENTING_NAME** [(PidTagSentRepresentingName)](pidtagsentrepresentingname-canonical-property.md)  <br/> |
| _адрес электронной почты_ <br/> |**PR_EMAIL_ADDRESS** [(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)  <br/> |
|неявный, всегда "SMTP"  <br/> |**PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)  <br/> |
   
Если в входящий почтовый ящик не отображается имя отображения, вместо него следует использовать весь адрес электронной почты. Тип адреса всегда SMTP.
  
Свойства получателей взяты из таблицы получателей сообщения MAPI; Свойства отправитель взяты из самого сообщения.
  

