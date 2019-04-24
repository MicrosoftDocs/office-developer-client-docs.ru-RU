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
ms.openlocfilehash: d463be4a14ecf478bdcbddc50b4ad9360829befc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355155"
---
# <a name="pidtagrenderingposition-canonical-property"></a>Каноническое свойство PidTagRenderingPosition

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит смещение (в символах), используемое для отображения вложения в тексте основного сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_РЕНДЕРИНГ_ПОСИТИОН  <br/> |
|Идентификатор:  <br/> |0x370B  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Вложение MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Если указанное смещение равно-1 (0xFFFFFFFF), то вложение не отображается с помощью этого свойства. Все значения, отличные от-1, указывают положение в свойстве **пр_боди** ([PidTagBody](pidtagbody-canonical-property.md)), в котором будет отображаться вложение.
  
 **Note (Примечание** ) Символ, указанный этим свойством в **пр_боди** , заменяется вложением. Как правило, этот символ является пробелом, хотя также можно использовать специальный замещающий символ. 
  
Это свойство выражается в символах. В некоторых наборах символов это значение не соответствует байтам. Приложения, поддерживающие Юникод, могут вычислять положение на основе двухбайтовых символов. Приложения с двухбайтовым набором знаков (DBCS) должны сканировать текст вплоть до значения этого свойства, так как их представление символов зависит от одного до двух байтов на символ.
  
Это свойство не следует использовать в тексте в формате RTF. Положение отрисовки указывается в формате RTF с помощью escape-последовательности, которая называется заполнителем вложенного объекта. Эта последовательность состоит из строки `\objattph` , за которой следует один символ, обычно пробел, который заменяется отрисовкой вложений. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

