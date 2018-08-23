---
title: Каноническое свойство PidTagAttachmentFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentFlags
api_type:
- HeaderDef
ms.assetid: 42981aac-f9e7-45dd-91a2-15d9784f30aa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0701bb2cf08c79a69c9cd21e9acf1ce4e8ac4ee1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593076"
---
# <a name="pidtagattachmentflags-canonical-property"></a>Каноническое свойство PidTagAttachmentFlags

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает, специально для данного объекта вложения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACHMENT_FLAGS  <br/> |
|Идентификатор:  <br/> |0x7FFD  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Должен быть 0x00000000, если не переопределено других протоколов, расширение сообщения и вложения объектов протокол как было указано в [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
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

