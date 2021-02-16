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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит смещение (в символах) для отображения вложения в основном тексте сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RENDERING_POSITION  <br/> |
|Идентификатор:  <br/> |0x370B  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Вложение MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Если предоставленное смещение составляет -1 (0xFFFFFFFF), вложение не отрисовка с помощью этого свойства. Все значения, кроме -1, указывают положение в свойстве **PR_BODY** ([PidTagBody),](pidtagbody-canonical-property.md)в котором должно быть отрисовлено вложение.
  
 **Примечание** Символ, указанный этим свойством **в** PR_BODY заменяется вложением. Обычно этот символ является пробелом, хотя также можно использовать специальный замеделя. 
  
Это свойство выражается символами. В некоторых наборах символов это не эквивалентно ветвям. Приложения Юникод могут вычислять положение на основе двух byte символов. Double-Byte приложения набора символов (DBCS) должны сканировать текст до значения этого свойства, так как их представление символов зависит от одного или двухбайт на символ.
  
Это свойство не должно использоваться с текстом RTF. Положение отрисовки указывается в RTF escape-последовательностью, называемой местом вложения объекта. Эта последовательность состоит из строки, за которой следует один символ, обычно пробел, который будет заменен визуализацией  `\objattph` вложения. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

