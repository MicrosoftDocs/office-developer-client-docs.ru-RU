---
title: Решение имени получателя
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
# <a name="resolving-a-recipient-name"></a>Решение имени получателя

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Когда сообщение адресовано, список получателей строится со свойствами, связанными с каждым получателем. К моменту отправления сообщения одним из этих свойств должен быть долгосрочный идентификатор входа получателя. Чтобы убедиться, что **каждый получатель** включает свойство [PR_ENTRYID (PidTagEntryId),](pidtagentryid-canonical-property.md)передайте структуру [ADRLIST,](adrlist.md) описывая список получателей в содержимом параметра  _lpAdrList_ в вызове [в IAddrBook::ResolveName](iaddrbook-resolvename.md).
  
 **ResolveName** начинает обработку, игнорируя уже разрешенные записи в структуре **ADRLIST,** о чем свидетельствует наличие идентификатора записи в массиве **SPropValue** соответствующей структуры [ADRENTRY.](adrentry.md) Далее **ResolveName** автоматически назначает идентификаторы разовой записи двум типам получателей: 
  
- Получатели с адресом, отформатированный в виде интернет-адреса
    
- Получатели с адресом, отформатированные следующим образом:
    
     `displayname[address type:email address]`
    
Для всех оставшихся записей **ResolveName** ищет адресную книгу для точного совпадения на отображаемом имени. **ResolveName** **использует свойство PR_AB_SEARCH_PATH** [(PidTagAbSearchPath)](pidtagabsearchpath-canonical-property.md)для определения набора контейнеров для поиска и порядка поиска. MAPI вызывает [метод IABContainer::ResolveNames](iabcontainer-resolvenames.md) каждого контейнера, чтобы попытаться устранить все имена. Так как некоторые контейнеры не поддерживают **ResolveNames,** если контейнер возвращается  MAPI_E_NO_SUPPORT, MAPI применяет ограничение свойств PR_ANR [(PidTagAnr)](pidtaganr-canonical-property.md)к его таблице содержимого. Все контейнеры адресной книги необходимы для поддержки разрешения имен с помощью этого ограничения. После того, как все имена будут устранены, дополнительные вызовы контейнеров не будут сделаны. Если все контейнеры были вызваны, но остаются неоднозначные или неурегулированные имена, MAPI отображает диалоговое окно, если это возможно, чтобы побудить пользователя разрешить оставшиеся имена.
  
Ограничение **PR_ANR** соответствует значению свойства  PR_ANR имени отображения в **структуре ADRLIST.** Ограничение представления таблицы содержимого контейнера с  ограничением свойств PR_ANR позволяет поставщику адресной книги выполнять поиск по "наилучшему угадайку", совпадая с свойством, которое имеет смысл для поставщика. Например, один поставщик адресных книг может всегда соответствовать именам в списке получателей **PR_DISPLAY_NAME** [(PidTagDisplayName),](pidtagdisplayname-canonical-property.md)а другой может разрешить администратору выбрать свойство.
  
 **Установить ограничение PR_ANR свойств в таблице содержимого контейнера адресной книги**
  
1. Создайте [структуру SRestriction,](srestriction.md) как показано в следующем коде: 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. Вызов метода [IMAPITable:::Restrict](imapitable-restrict.md) таблицы содержимого, передав структуру **SRestriction** в качестве _параметра lpRestriction._ 
    

