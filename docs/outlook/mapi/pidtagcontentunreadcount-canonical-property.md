---
title: Каноническое свойство PidTagContentUnreadCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ce7092840037345ae99b31c39cfbd4ac96b99ff5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811001"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a>Каноническое свойство PidTagContentUnreadCount

  
  
**Относится к**: Outlook 
  
Содержит количество непрочитанных сообщений в папке, вычисленный магазином сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTENT_UNREAD  <br/> |
|Идентификатор:  <br/> |0x3603  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство, вычисленный с хранилища сообщений используется для двух разных, на то, что связанные целей. Для объекта папки MAPI в нем количество сообщений в папке. В строке заголовка в таблицах по категориям MAPI он содержит количество непрочитанных сообщений не связанные в категории, соответствующий этой строке заголовка.
  
Это свойство содержит количество сообщений в таблице содержимое папки, для которого флаг MSGFLAG_READ не установлен в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Свойство **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) содержит общее количество сообщений для папки. **PR_CONTENT_COUNT** и этого свойства доступны только для чтения к клиентам. 
  
Некоторые клиентские приложения отображение строки заголовка категории по-разному в зависимости от значения этого свойства. К примеру клиент может отображать категории, который содержит непрочитанных сообщений в полужирным шрифтом. Это свойство не может использоваться как категории и попытка для этого результаты в значении MAPI_E_INVALID_PARAMETER возвращенный методом [IMAPITable::SortTable](imapitable-sorttable.md) . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Microsoft Exchange Server.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции папки.
    
[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Включает в себя разрешенных операций для базовых объектов в таблице.
    
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

