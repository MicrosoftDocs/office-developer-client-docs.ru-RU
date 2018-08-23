---
title: Каноническое свойство PidTagRenderingPosition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRenderingPosition
api_type:
- COM
ms.assetid: bce46687-17dc-4a3f-96be-303d8755158e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 649490f18bb1a14a7056b49fd846e893fba304bd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575212"
---
# <a name="pidtagrenderingposition-canonical-property"></a>Каноническое свойство PidTagRenderingPosition

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит смещение в символы, следует использовать при визуализации вложения в тексте основного сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RENDERING_POSITION  <br/> |
|Идентификатор:  <br/> |0x370B  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Вложений MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Если заданный смещение равно -1 (0xFFFFFFFF), вложение не отображаются с использованием этого свойства. Все значения, отличные от -1 указывает положение в пределах свойства **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), в которой для отображения вложение.
  
 **Примечание** Символ, указанный в параметре это свойство **PR_BODY** заменяется вложение. Обычно это пробелами, несмотря на то, что также можно использовать специальный заполнитель. 
  
Это свойство выражается в символы. В некоторых наборах знаков, это не лежат в байтах. Юникод приложений можно вычислить положение, основываясь на двухбайтовых знаков. Из-за их представление знака может отличаться от одного до двух байт на символ приложений задать двухбайтовых знаков (DBCS) необходимо проверить текста до значения этого свойства.
  
Это свойство следует использовать не с текстом форматированный текст (RTF). Положения обозначается escape-последовательность называется заполнитель object вложений в формате RTF. Эта последовательность включает строку `\objattph` за которой следует один символ, обычно сколько места на диске, будет заменена с отображением вложения. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
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

