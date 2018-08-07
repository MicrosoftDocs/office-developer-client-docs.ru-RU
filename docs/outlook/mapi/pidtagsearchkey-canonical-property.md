---
title: Каноническое свойство PidTagSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 169afc3b8cf982c4767802542b900ae80822cd01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811878"
---
# <a name="pidtagsearchkey-canonical-property"></a>Каноническое свойство PidTagSearchKey

  
  
**Относится к**: Outlook 
  
Содержит двоичный сравнимые ключ, который определяет соответствующих объектов для поиска.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SEARCH_KEY  <br/> |
|Идентификатор:  <br/> |0x300B  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Идентификатор свойства  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство содержит трассировку для связанные объекты, такие как копии сообщения и упрощает поиск нежелательных вхождения, такие как повторяющиеся получателей.
  
MAPI использует определенные правила для создания ключей поиска для получателей сообщений. Ключ поиска образуется путем объединения тип адреса (в верхнем регистре), двоеточие ":", адреса электронной почты в каноническое формы и конечный символ null. Каноническое формы здесь означает, что к регистру адреса отображаются в случае правильный и адреса, которые не учитывают регистр преобразуются в верхний регистр. Это важно сохранения взаимосвязи между сообщения.
  
Для объектов-сообщение этому свойству можно получить через метод [IMAPIProp::GetProps](imapiprop-getprops.md) сразу после создания сообщения. Для других объектов доступных после первого вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Поскольку это свойство является изменяемым, нестабильна его можно получить через **GetProps** до вызова **SaveChanges** завершена значения установить или изменить с помощью метода [IMAPIProp::SetProps](imapiprop-setprops.md) . 
  
Для профилей MAPI также предоставляет раздел жестко заданного профиля с именем **MUID_PROFILE_INSTANCE**, с помощью этого свойства, как его отдельное свойство. Этот ключ гарантированно уникальным во всех профилей, когда-либо созданных и может быть более надежным, чем свойство **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), который может быть например, удалены и заново с таким же именем.
  
В следующей таблице представлены важные различия между **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) и это свойство.
  
|**Характеристики**|PR_ENTRYID ***|PR_RECORD_KEY ***|PR_SEARCH_KEY ***|
|:-----|:-----|:-----|:-----|
|Требуется на объекты вложения  <br/> |Нет  <br/> |Да  <br/> |Нет  <br/> |
|Требуется на объектов папок  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Требуется на объектов хранилища сообщений  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Требуется на состояние объектов  <br/> |Да  <br/> |Нет  <br/> |Нет  <br/> |
|Возможно создание клиентом  <br/> |Нет  <br/> |Нет  <br/> |Да  <br/> |
|Доступные до **SaveChanges** <br/> |Зависит от реализации поставщика  <br/> |Зависит от реализации поставщика  <br/> |Для сообщений, Да. Для других пользователей он зависит от реализации поставщика.  <br/> |
|Изменения в операцию копирования  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Механизм клиента после копирования  <br/> |Нет  <br/> |Нет  <br/> |Да  <br/> |
|Уникальный в пределах...  <br/> |Весь мир  <br/> |Экземпляр поставщика  <br/> |Весь мир  <br/> |
|Двоичный сравнимые (как с memcmp)  <br/> |Нет — используйте [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Да  <br/> |Да  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagResponsibility](pidtagresponsibility-canonical-property.md)
  
[Каноническое свойство PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

