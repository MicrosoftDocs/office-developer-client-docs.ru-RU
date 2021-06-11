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
ms.openlocfilehash: 7e9994da72bbc38a546f220e5ecf8768b80c6f1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331957"
---
# <a name="pidtagcontentcount-canonical-property"></a>Каноническое свойство PidTagContentCount

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит количество сообщений в папке, как вычислено в хранилище сообщений.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTENT_COUNT  <br/> |
|Идентификатор:  <br/> |0x3602  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство, вычисленное в хранилище сообщений, используется для двух различных, хотя и связанных, целей. На объекте MapiFolder содержится количество сообщений в папке. В строке заголовка в классизированных таблицах MAPI содержится количество не связанных сообщений в категории, соответствующей этой строке заголовка.
  
Номер, содержащийся в этом свойстве, не включает связанные записи в папке. **PR_CONTENT_UNREAD** [(PidTagContentUnreadCount)](pidtagcontentunreadcount-canonical-property.md)содержит количество непрочитанные сообщения для папки. Клиентские приложения могут читать, но не изменять это свойство **и PR_CONTENT_UNREAD.** 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Microsoft Exchange Server протоколы.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции папок.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Включает допустимые операции для основных объектов таблицы.
    
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

