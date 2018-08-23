---
title: Каноническое свойство PidTagAttachAdditionalInformation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachAdditionalInformation
api_type:
- HeaderDef
ms.assetid: 75f092f2-ee3f-45c2-a46f-e1dff2e22b2e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8df81920b9d2e88b23438fd398bde7d8e426b248
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587693"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a>Каноническое свойство PidTagAttachAdditionalInformation

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Предоставляет сведения о типе файла для вложения отличных от Windows.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_ADDITIONAL_INFO  <br/> |
|Идентификатор:  <br/> |0x370F  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство предоставляет метаданные о конкретной вложений на основании кодирование вложений. Например если свойство **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) содержит файлы, **PR_ATTACH_ADDITIONAL_INFO** содержит строку, представляющую создатель и тип файла в формате «:CREA:TYPE» зашифрованный файл Macintosh. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
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

