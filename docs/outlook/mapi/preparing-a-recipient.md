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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения подготавливают получателей, преобразуя их краткосрочные идентификаторы записей в долгосрочные идентификаторы записей и, возможно, добавляя, изменяя или изменяя свойства. Вы можете подготовить получателей, которые являются частью списка получателей, для сообщений или получателей, не связанных с сообщением. Как правило, клиенты звонят по адресу [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) напрямую, чтобы преобразовыть краткосрочные идентификаторы записей в долгосрочные идентификаторы записей для получателей, включенных в диалоговое окно общего адреса. Для получателей, связанных с исходяменем, подготовка получателей обрабатывается процессом разрешения имен. 
  
Чтобы подготовить список получателей, вызовите **IAddrBook::P repareRecips.** **PrepareRecips** принимает структуру [ADRLIST](adrlist.md) и список тегов свойств. Структура **ADRLIST** содержит получателей, которых необходимо подготовить, а список тегов свойств представляет свойства, которые должен поддерживать каждый получатель. **PrepareRecips** пытается разместить свойства, включенные в список тегов свойств, в начале структуры **ADRLIST.** Если какие-либо свойства в списке отсутствуют в структуре **ADRLIST,** MAPI вызывает поставщик адресной книги, чтобы предоставить их. Если вам нужно проверить только долгосрочные идентификаторы записей, передайте NULL для параметра _lpSPropTagArray._ 
  
Например, предположим, что вы работаете с пятью получателями. Все пять получателей отображаются в структуре **ADRLIST** со следующими свойствами в следующем порядке: 
  
1. **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)
    
2. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **PR_SEARCH_KEY** ([PidTagSearchKey)](pidtagsearchkey-canonical-property.md)
    
4. **PR_EMAIL_ADDRESS** ([PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)
    
5. **PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)
    
Три других свойства включены в структуру **ADRLIST** для первых двух получателей. 
  
1. **PR_ACCOUNT** ([PidTagAccount)](pidtagaccount-canonical-property.md)
    
2. **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))
    
Так как все получатели должны иметь в качестве первых трех свойств **PR_ADDRTYPE,** **PR_ENTRYID** и **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber),](pidtaghometelephonenumber-canonical-property.md)создайте массив тегов свойств с этими свойствами и передайте его и структуру **ADRLIST** **в PrepareRecips**. **PrepareRecips** вызывает метод **IMAPIProp::GetProps** **каждого** получателя для получения PR_HOME_TELEPHONE_NUMBER, так как в настоящее время он не является частью структуры **ADRLIST.** Когда **prepareRecips** возвращает, список получателей представляет объединенный список получателей со свойствами, включенными в структуру **ADRLIST,** который первым появляется для каждого получателя. 
  
Список получателей 1 и 2 содержит свойства в следующем порядке:
  
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
    
Список получателей 3, 4 и 5 содержит свойства в следующем порядке:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
В качестве альтернативы вызову **IAddrBook::P repareRecips** для работы со свойствами вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) каждого получателя и, при необходимости, его [метод IMAPIProp::SetProps.](imapiprop-setprops.md) Если задействован только один получатель, любая методика удовлетворительна. Однако если задействовано несколько получателей, вызов **Метода PrepareRecips,** а не **метода IMAPIProp** экономит время и, если вы работаете удаленно, много удаленных вызовов процедур. **PrepareRecips** обрабатывает всех получателей в одном вызове, в то время как **GetProps** и **SetProps** делают один вызов для каждого получателя. 
  

