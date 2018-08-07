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
ms.openlocfilehash: 51241009262471bf30f7d71e3108b896bbce8df7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812060"
---
# <a name="preparing-a-recipient"></a>Подготовка получателя

  
  
**Относится к**: Outlook 
  
Клиентское приложение подготавливает получателей, преобразование их краткосрочных идентификаторы записей для долгосрочного идентификаторы записей и возможно добавления, изменения или изменение порядка свойств. Можно подготовить получателей, которые являются частью списка получателей сообщения или получателей, не относящихся к сообщению. Как правило клиенты вызывать [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) непосредственно для перевода краткосрочных идентификаторы записей в долгосрочного идентификаторы записей для получателей, включенных в стандартным диалоговым окном адрес. Для получателей, которые связаны с исходящих сообщений подготовки получателями обрабатывается процесса разрешения имен. 
  
Чтобы подготовить список получателей, вызовите **IAddrBook::PrepareRecips**. **PrepareRecips** принимает структуру [ADRLIST](adrlist.md) и список тегов свойств. Структура **ADRLIST** содержит получателей для подготовки во время список свойств тега представляет свойства, которые должны поддерживать каждого получателя. **PrepareRecips** предпринимает попытку свойства, которые включены в список свойств тега в начале структуры **ADRLIST** . Если какие-либо свойства в списке отсутствуют структура **ADRLIST** , MAPI вызывает поставщик адресной книги, чтобы предоставить им. Если необходимо проверить наличие долгосрочного идентификаторы записей, передайте значение NULL для параметра _lpSPropTagArray_ . 
  
Например предположим, что вы работаете с пятью получателей. Все получатели отображаются в структуре **ADRLIST** следующие свойства в следующем порядке: 
  
1. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
2. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
4. **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
5. **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
Три свойства включены в структуре **ADRLIST** для первых двух получателей. 
  
1. **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))
    
2. **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))
    
Поскольку всех получателей должны иметь свои первые три свойства **PR_ADDRTYPE**, **PR_ENTRYID**и **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), создание массива тега свойства с помощью этих свойств и передайте он и структуре **ADRLIST** для **PrepareRecips**. **PrepareRecips** вызывает метод **IMAPIProp::GetProps** каждого получателя, чтобы получить **PR_HOME_TELEPHONE_NUMBER** , так как он не является частью структуры **ADRLIST** . При возврате **PrepareRecips** списка получателей представляет объединенного списка получателей со свойствами в структуре **ADRLIST** может выглядеть для каждого получателя. 
  
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
    
Список получателей для получателей, 3, 4 и 5 включает в себя свойства в следующем порядке:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
В качестве альтернативы для вызова **IAddrBook::PrepareRecips** для работы со свойствами, вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) каждого получателя и, при необходимости его метод [IMAPIProp::SetProps](imapiprop-setprops.md) . Когда выполняется только один получатель, либо метод удовлетворяют. Тем не менее, когда задействованы несколько получателей, вызов **PrepareRecips** , а не методы **IMAPIProp** экономит время и, работающие удаленно, много удаленных вызовов процедур. **PrepareRecips** обрабатывает всех получателей в одном вызове, тогда как **GetProps** и **SetProps** выполнение одного звонка для каждого получателя. 
  

