---
title: Разрешение имени получателя
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a3faed3dda2461cab749c824fc97c2074e62375f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405868"
---
# <a name="resolving-a-recipient-name"></a>Разрешение имени получателя

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Когда сообщение адресовано, список получателей строится со свойствами, связанными с каждым получателем. К моменту сообщения одно из этих свойств должно быть долгосрочным идентификатором записи получателя. Чтобы убедиться, что каждый получатель содержит свойство **PR_ENTRYID** ([PidTagEntryId),](pidtagentryid-canonical-property.md)передайте структуру [ADRLIST,](adrlist.md) описывая список получателей, в содержимом параметра _lpAdrList_ в вызове [IAddrBook::ResolveName.](iaddrbook-resolvename.md)
  
 **ResolveName** начинает обработку, игнорируя записи в структуре **ADRLIST,** которые уже были разрешены, на что указывает наличие идентификатора записи в соответствующем массиве **SPropValue** структуры [ADRENTRY.](adrentry.md) Затем **ResolveName автоматически** назначает идентификаторы одноавтоматной записи двум типам получателей: 
  
- Получатели с адресом, отформатированный как адрес Интернета
    
- Получатели с адресом, отформатированный следующим образом:
    
     `displayname[address type:email address]`
    
Для всех остальных записей **ResolveName** выполняет поиск точного совпадения в отображаемом имени в адресной книге. **ResolveName** использует **свойство PR_AB_SEARCH_PATH** [(PidTagAbSearchPath)](pidtagabsearchpath-canonical-property.md)для определения набора контейнеров для поиска и порядка поиска. MAPI вызывает метод [IABContainer::ResolveNames](iabcontainer-resolvenames.md) каждого контейнера, чтобы попытаться разрешить все имена. Так как некоторые контейнеры не поддерживают **ResolveNames,** если контейнер возвращает MAPI_E_NO_SUPPORT, MAPI применяет ограничение свойства **PR_ANR** ([PidTagAnr)](pidtaganr-canonical-property.md)к таблице содержимого. Все контейнеры адресной книги необходимы для поддержки разрешения имен с этим ограничением. После разрешения всех имен никакие дополнительные вызовы контейнеров не будут выполнены. Если все контейнеры были вызваны, но неоднозначные или не разрешенные имена остаются, MAPI по возможности отображает диалоговое окно, в котором пользователю будет предложено разрешить оставшиеся имена.
  
Ограничение **PR_ANR** соответствует значению свойства  PR_ANR отображаемого имени в **структуре ADRLIST.** Ограничение представления таблицы содержимого контейнера с помощью ограничения свойства **PR_ANR** приводит к выполнению поставщиком адресной книги "наилучшего угадать" типа поиска, совпадая со свойством, которое имеет смысл для поставщика. Например, один поставщик адресной книги всегда может соответствовать именам в списке получателей PR_DISPLAY_NAME **(** [PidTagDisplayName),](pidtagdisplayname-canonical-property.md)а другой может позволить администратору выбрать свойство.
  
 **Настройка ограничения PR_ANR свойств для таблицы содержимого контейнера адресной книги**
  
1. Создайте [структуру SRestriction,](srestriction.md) как показано в следующем коде: 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. Вызовите метод [IMAPITable::Restrict](imapitable-restrict.md) таблицы содержимого, передав **структуру SRestriction** в качестве параметра _lpRestriction._ 
    

