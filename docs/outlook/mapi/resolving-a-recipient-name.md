---
title: Разрешение имя получателя
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 256412f6ccbe66da067411bf9f66ad0478cf5ca2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812138"
---
# <a name="resolving-a-recipient-name"></a>Разрешение имя получателя

  
  
**Применимо к**: Outlook 
  
Когда сообщение можно решить, список получателей построения со свойствами, относящиеся к каждому получателю. С момента отправки сообщения один из этих свойств должен быть долгосрочного запись идентификатор получателя. Чтобы убедиться, что для каждого получателя, содержит свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), передайте [ADRLIST](adrlist.md) структуры, описывающие список получателей в содержимое параметра _lpAdrList_ к вызову [IAddrBook:: ResolveName](iaddrbook-resolvename.md).
  
 **ResolveName** начинает обработку, игнорируя записи в структуре **ADRLIST** , которые уже разрешены, как указано в присутствия идентификатор записи в соответствующем структура [ADRENTRY](adrentry.md) **SPropValue** массив. Рассмотрим процедуру **ResolveName** автоматически устанавливает идентификаторы единичных записей для двух типов получателей: 
  
- Получатели с адресом в формате адреса в Интернете
    
- Получатели с адресом следующий формат:
    
     `displayname[address type:email address]`
    
Для всех остальных записей **ResolveName** поиск точного совпадения на отображаемое имя в адресной книге. **ResolveName** использует свойство **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) для определения набора контейнеров для поиска и порядок поиска. MAPI вызывает метод [IABContainer::ResolveNames](iabcontainer-resolvenames.md) каждые контейнера, чтобы разрешить всем именам. Так как некоторые контейнеров не поддерживают **ResolveNames**, если контейнер возвращает MAPI_E_NO_SUPPORT, MAPI применяется ограничение свойства **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) от его содержимое в таблице. Все контейнеры адресной книги требуются для поддержки разрешение имен с это ограничение. Когда все имена разрешаются, больше не контейнер вызовы выполняются. Вызвали контейнеров, но остаются неоднозначные или нерешенные имена, MAPI отображает диалоговое окно, если это возможно пригласить пользователя для разрешения имен остальных.
  
Ограничение **PR_ANR** совпадает со значением свойства **PR_ANR** относительно отображаемое имя в структуре **ADRLIST** . Ограничение представление таблицы содержимого контейнера с ограничением свойство **PR_ANR** вызывает поставщик адресной книги для выполнения «лучше всего подбора» тип поиска, сравнение с свойство, которое имеет смысл для поставщика. Например один поставщик адресной книги всегда может совпадать имена в список получателей с **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), в то время как другой может позволить администратору выбрать свойство.
  
 **Чтобы задать ограничение свойства PR_ANR на таблицу содержимого контейнер адресной книги**
  
1. Создание структуры [SRestriction](srestriction.md) , как показано в следующем коде: 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. Вызовите метод [IMAPITable::Restrict](imapitable-restrict.md) таблицы, передачи структуры **SRestriction** в качестве параметра _lpRestriction_ содержимое. 
    

