---
title: Каноническое свойство PidTagAttachSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachSize
api_type:
- HeaderDef
ms.assetid: 768b3215-dd9f-4aa0-b52c-178ca81a7b07
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f3e4f19ab43a3da7c4840d762d5131813c83d996
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361091"
---
# <a name="pidtagattachsize-canonical-property"></a>Каноническое свойство PidTagAttachSize

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит сумму в bytes размеров всех свойств на вложении. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_SIZE  <br/> |
|Идентификатор:  <br/> |0x0E20  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Рекомендуется, чтобы подобекты вложения подвергали **PR_ATTACH_SIZE** свойству. В сумму,  PR_ATTACH_SIZE, входит размер свойства  [PR_ATTACH_DATA_BIN (PidTagAttachDataBinary)](pidtagattachdatabinary-canonical-property.md)или **PR_ATTACH_DATA_OBJ** [(PidTagAttachDataObject).](pidtagattachdataobject-canonical-property.md) Соответственно, **PR_ATTACH_SIZE** обычно больше, чем содержимое только вложения. 
  
Это свойство можно использовать для проверки приблизительного размера вложения перед выполнением удаленной передачи с помощью модема и отображения индикаторов прогресса при сохранении вложения на диске. Это особенно полезно с присоединенными объектами OLE. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagMessageSize](pidtagmessagesize-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

