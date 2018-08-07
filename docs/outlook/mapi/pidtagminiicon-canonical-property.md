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
ms.openlocfilehash: 04d78bddc7bae27ba23cccf676eb6e7412ffc0db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811383"
---
# <a name="pidtagminiicon-canonical-property"></a>Каноническое свойство PidTagMiniIcon

  
  
**Относится к**: Outlook 
  
Содержит растрового изображения значка наполовину размер для формы.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MINI_ICON  <br/> |
|Идентификатор:  <br/> |0x0FFC  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство содержит изображение значка, то же, что содержимое в размером 32 на 32 пикселя. Файл ICO, но только верхнем левом углу 16 × 16 пикселей, считаются значительные. Это свойство обычно копируются из. ICO-файла, указанного в строке SmallIcon соответствующий раздел [Описание] файла конфигурации формы.
  
 **Примечание** Некоторые платформы выполните не значки поддержки 16 × 16 пикселей. Формат размером 32 на 32 это свойство можно использовать в таком случае, но клиентские приложения следует иметь в виду несоответствия отображения. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagIcon](pidtagicon-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

