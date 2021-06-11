---
title: Подготовка получателя
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bb6bc8b8d0199ab07d5dad353dbc25da240593e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419879"
---
# <a name="preparing-a-recipient"></a>Подготовка получателя

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиентская заявка подготавливает получателей путем преобразования их краткосрочных идентификаторов записей в идентификаторы долгосрочных записей и, возможно, добавления, изменения или изменения свойств. Можно подготовить получателей, которые являются частью списка получателей, для сообщения или получателей, не связанных с сообщением. Как правило, клиенты звонят [в IAddrBook::P repareRecips](iaddrbook-preparerecips.md) напрямую, чтобы перевести краткосрочные идентификаторы записи в долгосрочные идентификаторы записей для получателей, включенных в диалоговое окно общего адреса. Для получателей, связанных с исходя из сообщения, подготовка получателей обрабатывается процессом разрешения имен. 
  
Чтобы подготовить список получателей, позвоните **в IAddrBook::P repareRecips**. **PrepareRecips** принимает структуру [ADRLIST](adrlist.md) и список тегов свойств. Структура **ADRLIST содержит** получателей, которые должны быть подготовлены, а список тегов свойств представляет свойства, которые должен поддерживать каждый получатель. **PrepareRecips** пытается разместить свойства, включенные в список тегов свойств в начале **структуры ADRLIST.** Если какие-либо из свойств в списке отсутствуют в структуре **ADRLIST,** MAPI вызывает поставщика адресной книги для их поставки. Если вам нужно проверить только долгосрочные идентификаторы записи, передайте NULL для _параметра lpSPropTagArray._ 
  
Например, предположим, что вы работаете с пятью получателями. Все пять получателей отображаются в **структуре ADRLIST** со следующими свойствами в следующем порядке: 
  
1. **PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)
    
2. **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)
    
3. **PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)
    
4. **PR_EMAIL_ADDRESS** [(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)
    
5. **PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)
    
Три других свойства включены в структуру **ADRLIST** для первых двух получателей. 
  
1. **PR_ACCOUNT** [(PidTagAccount)](pidtagaccount-canonical-property.md)
    
2. **PR_GIVEN_NAME** [(PidTagGivenName)](pidtaggivenname-canonical-property.md)
    
3. **PR_SURNAME** [(PidTagSurname)](pidtagsurname-canonical-property.md)
    
Так как все получатели должны иметь в качестве первых трех свойств **PR_ADDRTYPE,** **PR_ENTRYID** и **PR_HOME_TELEPHONE_NUMBER** [(PidTagHomeTelephoneNumber),](pidtaghometelephonenumber-canonical-property.md)создайте массив тегов свойств с этими свойствами и передайте его и структуру **ADRLIST** **в PrepareRecips**. **PrepareRecips** вызывает метод **IMAPIProp::GetProps** **для** получения PR_HOME_TELEPHONE_NUMBER, так как в настоящее время он не входит в структуру **ADRLIST.** Когда **PrepareRecips** возвращается, список получателей представляет собой объединенный список получателей с свойствами, включенными в структуру **ADRLIST,** которые отображаются первыми для каждого получателя. 
  
Список получателей для получателей 1 и 2 включает свойства в следующем порядке:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
8. **PR_ACCOUNT**
    
9. **PR_GIVEN_NAME**
    
10. **PR_SURNAME**
    
Список получателей для получателей 3, 4 и 5 включает свойства в следующем порядке:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
В качестве альтернативы вызову **IAddrBook::P repareRecips** для работы с свойствами вызываем метод [IMAPIProp::GetProps](imapiprop-getprops.md) каждого получателя и, при необходимости, его [метод IMAPIProp::SetProps.](imapiprop-setprops.md) Если задействован только один получатель, любой метод является удовлетворительным. Однако при вовлечении нескольких получателей вызов **PrepareRecips,** а не методы **IMAPIProp** экономит время и, если вы работаете удаленно, много удаленных вызовов процедур. **PrepareRecips** обрабатывает всех получателей одним вызовом, в то время как **GetProps** и **SetProps** делают по одному вызову для каждого получателя. 
  

