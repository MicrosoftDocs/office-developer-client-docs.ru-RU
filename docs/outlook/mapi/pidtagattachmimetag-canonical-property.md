---
title: Каноническое свойство PidTagAttachMimeTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMimeTag
api_type:
- HeaderDef
ms.assetid: cbc4585d-f970-4b22-ac08-d7fc91bff3d3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f05fa0816db3b412329372ad392c673c240eb59e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327246"
---
# <a name="pidtagattachmimetag-canonical-property"></a>Каноническое свойство PidTagAttachMimeTag

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит сведения о форматировании для вложения с многоцелевыми почтовыми расширениями в Интернете (MIME). 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A PR_ATTACH_MIME_TAG_W  <br/> |
|Идентификатор:  <br/> |0x370E  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Если свойство **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) содержит значение **OID_MIMETAG**, поставщик транспорта должен просмотреть эти свойства, чтобы определить способ форматирования вложения. 
  
Эти свойства копируются из параметра Content – Type входящего заголовка MIME. Композиция строки определена в документе RFC 1521. Формат — тип/подтип, например Application/Binary или text/plain. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS — ОКСОРММС]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Задает свойства сообщений, закодированных с помощью управления правами.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

