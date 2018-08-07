---
title: Каноническое свойство PidTagStoreRecordKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreRecordKey
api_type:
- COM
ms.assetid: 27347302-bd52-4f62-98f1-6c37f9a66463
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4598ca5e654308f7701b1dd66adb227599773b7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811986"
---
# <a name="pidtagstorerecordkey-canonical-property"></a>Каноническое свойство PidTagStoreRecordKey

  
  
**Относится к**: Outlook 
  
Содержит уникальный идентификатор сравнимые двоичный файл (ключ записи) хранилища сообщений, в котором находится объект.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_STORE_RECORD_KEY  <br/> |
|Идентификатор:  <br/> |0x0FFA  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Идентификатор свойства  <br/> |
   
## <a name="remarks"></a>Замечания

Для хранилища сообщений это свойство идентичен свойство магазина собственные **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)).
  
Отношения между это свойство и **PR_RECORD_KEY** -то же, что связь между **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) и **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

