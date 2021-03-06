---
title: Каноническое свойство PidTagRecordKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecordKey
api_type:
- COM
ms.assetid: a12fb9a2-799d-4112-b26c-4b2854c47cc2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7a3ae7db1fb97e97f7d0939b67f139af62477bf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355267"
---
# <a name="pidtagrecordkey-canonical-property"></a>Каноническое свойство PidTagRecordKey

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит уникальный двоичный идентификатор для определенного объекта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECORD_KEY  <br/> |
|Идентификатор:  <br/> |0x0FF9  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Свойства ID  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство упрощает поиск ссылок на объект, например поиск строки в таблице содержимого. Это свойство нельзя использовать для открытия объекта; используйте идентификатор записи для этой цели.
  
Подобект вложения должен быть однозначно определен в сообщении этим свойством. Этот идентификатор является единственной характеристикой вложения, гарантированной для того, чтобы оставаться на том же уровне после закрытия и повторного открытия сообщения. Поставщик магазина должен сохранить это свойство во всех сеансах, чтобы обеспечить эту гарантию.
  
Для папок это свойство содержит ключ, используемый в таблице иерархии папок. Обычно это то же значение, что и свойство **PR_ENTRYID** [(PidTagEntryId).](pidtagentryid-canonical-property.md)
  
Для магазинов сообщений это свойство идентично **свойству PR_STORE_RECORD_KEY** [(PidTagStoreRecordKey).](pidtagstorerecordkey-canonical-property.md)
  
В объекте магазина сообщений это свойство должно быть уникальным для всех поставщиков магазинов. Один из способов сделать это **—** объединить значение свойства [PR_MDB_PROVIDER (PidTagStoreProvider)](pidtagstoreprovider-canonical-property.md)для магазина (уникального для этого типа поставщика) с структурой [GUID](guid.md) или другим значением, уникальным для определенного магазина сообщений. 
  
Это свойство всегда доступно с помощью [метода IMAPIProp::GetProps](imapiprop-getprops.md) после первого вызова метода [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Некоторые поставщики могут сделать ее доступной сразу после мгновенной. 
  
Клиент или поставщик услуг может сравнить значения из этого свойства с помощью memcmp. Это невозможно для значений идентификатора входа. Однако это свойство гарантированно будет уникальным в одном хранилище сообщений или контейнере адресной книги; два объекта из разных контейнеров могут иметь одинаковое значение этого свойства.
  
Одно различие между записями и ключами поиска в том, что ключ записи является специфическим для объекта, в то время как ключ поиска может быть скопирован на другие объекты. Например, две копии объекта могут иметь одно и то же **значение PR_SEARCH_KEY** [(PidTagSearchKey),](pidtagsearchkey-canonical-property.md)но должны иметь разные значения для этого свойства.
  
В следующей таблице суммируются важные различия между PR_ENTRYID **,** **PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)и этим свойством. 
  
|**Характеристика**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Необходимые для объектов вложений  <br/> |Нет  <br/> |Да  <br/> |Нет  <br/> |
|Необходимые для объектов папок  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Необходимые для объектов хранения сообщений  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Необходимые для объектов состояния  <br/> |Да  <br/> |Нет  <br/> |Нет  <br/> |
|Creatable клиентом  <br/> |Нет  <br/> |Нет  <br/> |Да  <br/> |
|Доступно перед вызовом **в SaveChanges** <br/> |Может быть,  <br/> |Может быть,  <br/> |Сообщения Да Другие Может быть  <br/> |
|Изменено в операции копирования  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Изменение клиентом после копирования  <br/> |Нет  <br/> |Нет  <br/> |Да  <br/> |
|Уникальный в ...  <br/> |Весь мир  <br/> |Экземпляр поставщика  <br/> |Весь мир  <br/> |
|Двоичная сопоставимая (как с memcmp)  <br/> |Нет - используйте **IMAPISupport:: CompareEntryIDs** <br/> |Да  <br/> |Да  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

