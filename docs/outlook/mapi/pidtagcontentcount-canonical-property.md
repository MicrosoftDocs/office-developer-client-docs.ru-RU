---
title: Каноническое свойство PidTagContentCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCount
api_type:
- HeaderDef
ms.assetid: 27c75031-a968-4636-98a6-4a5b7422f57c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3c542b07eac626da5fbbb6a96b4545ad3c8558b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810995"
---
# <a name="pidtagcontentcount-canonical-property"></a>Каноническое свойство PidTagContentCount

  
  
**Относится к**: Outlook 
  
Содержит количество сообщений в папку, вычисленный магазином сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTENT_COUNT  <br/> |
|Идентификатор:  <br/> |0x3602  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство, вычисленный с хранилища сообщений используется для двух разных, на то, что связанные целей. Для объекта MAPIFolder различными способами в нем количество сообщений в папке. В строке заголовка в таблицах по категориям MAPI оно содержит число не связанные сообщения в категории, соответствующий этой строке заголовка.
  
Номер, содержащиеся в этом свойстве не включает связанных записей в папке. **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) содержит количество непрочитанных сообщений для папки. Клиентское приложение можно читать, но не изменять это свойство и **PR_CONTENT_UNREAD**. 
  
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

