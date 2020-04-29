---
title: Каноническое свойство PidTagMiniIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMiniIcon
api_type:
- HeaderDef
ms.assetid: a436b590-63f3-413c-a9c2-7664567e0ff0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ea7f9e0ed57c56b48399b9ffd1ea42db28daf249
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405417"
---
# <a name="pidtagminiicon-canonical-property"></a>Каноническое свойство PidTagMiniIcon

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит точечный рисунок значка половинной емкости для формы.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MINI_ICON  <br/> |
|Идентификатор:  <br/> |0x0FFC  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Общий обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство содержит изображение значка размером 32 × 32, аналогичное содержимому элемента. ICO, но только верхний левый 16 × 16 пикселя считается существенным. Обычно это свойство копируется из. ICO файл, указанный в строке Смалликон соответствующего раздела [Description] файла конфигурации формы.
  
 **Note (Примечание** ) Некоторые платформы не поддерживают 16 × 16 значков пикселей. Формат 32 × 32 для этого свойства можно использовать в таком случае, но клиентские приложения должны знать о несоответствиях отображения. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagIcon](pidtagicon-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

