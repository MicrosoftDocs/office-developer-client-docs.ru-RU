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
  
Клиентское приложение подготавливает получателей путем преобразования краткосрочных идентификаторов записей в долгосрочные идентификаторы записей и, возможно, для добавления, изменения или изменения порядка свойств. Можно подготовить получателей, которые входят в список получателей, для сообщений или получателей, не связанных с сообщением. Как правило, клиенты вызывают [IAddrBook::P репаререЦипс](iaddrbook-preparerecips.md) напрямую, чтобы перевести краткосрочные идентификаторы записей в долгосрочные идентификаторы записей для получателей, включенных в диалоговое окно Общий адрес. Для получателей, связанных с исходящим сообщением, подготовка получателей обрабатывается с помощью процесса разрешения имен. 
  
Чтобы подготовить список получателей, вызовите **IAddrBook::P репаререЦипс**. **ПрепаререЦипс** принимает в качестве значения структуру [ADRLIST](adrlist.md) и список тегов свойств. Структура **ADRLIST** содержит получателей для подготовки, в то время как список тегов свойств представляет свойства, которые должны поддерживаться каждым получателем. **ПрепаререЦипс** пытается поместить свойства, включенные в список тегов свойств, в начале структуры **ADRLIST** . Если какое бы то ни было из свойств в списке отсутствует в структуре **ADRLIST** , MAPI вызывает поставщик адресной книги для их предоставления. Если требуется проверить только долгосрочные идентификаторы записей, передайте значение NULL для параметра _лпспроптагаррай_ . 
  
Например, предположим, что вы работаете с пятью получателями. Все пять получателей отображаются в структуре **ADRLIST** со следующими свойствами в следующем порядке: 
  
1. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
2. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
4. **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
5. **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
Для первых двух получателей в структуру **ADRLIST** включены три других свойства. 
  
1. **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))
    
2. **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))
    
Так как все получатели должны иметь в качестве первых трех свойств **PR_ADDRTYPE**, **PR_ENTRYID**и **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), создайте массив тегов свойств с этими свойствами и передайте его и структуру **ADRLIST** в **препаререЦипс**. **ПрепаререЦипс** вызывает метод **IMAPIProp::-PROPS** каждого получателя, чтобы получить **PR_HOME_TELEPHONE_NUMBER** , так как он в настоящее время не является частью структуры **ADRLIST** . Когда возвращается значение **препаререЦипс** , список получателей представляет объединенный список получателей со свойствами, включенными в структуру **ADRLIST** , которые первыми появлялись для каждого получателя. 
  
Список получателей для получателей 1 и 2 содержит свойства в следующем порядке:
  
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
    
Список получателей для получателей 3, 4 и 5 содержит свойства в следующем порядке:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
В качестве альтернативы вызову **IAddrBook::P репаререЦипс** для работы со свойствами, вызывайте каждый метод [IMAPIProp::](imapiprop-getprops.md) и при необходимости метод [IMAPIProp:: SetProps](imapiprop-setprops.md) . Если используется только один получатель, любой из способов является удовлетворительным. Однако при использовании нескольких получателей вызов **препаререЦипс** , а не методы **IMAPIProp** экономит время и, при удаленном запуске, множество вызовов удаленных процедур. **ПрепаререЦипс** обрабатывает все получатели в одном вызове **, а** в **SetProps** — один вызов для каждого получателя. 
  

