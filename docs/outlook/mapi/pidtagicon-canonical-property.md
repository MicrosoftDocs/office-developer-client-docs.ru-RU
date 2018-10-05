---
title: Каноническое свойство PidTagIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIcon
api_type:
- HeaderDef
ms.assetid: 815dabf3-3cac-40e1-b6ff-51db2ff5096a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ad8d6934b5e57429de5039e9420742caa9dd4294
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397697"
---
# <a name="pidtagicon-canonical-property"></a>Каноническое свойство PidTagIcon

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит растрового изображения значка полный размер для формы. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ICON  <br/> |
|Идентификатор:  <br/> |0x0FFD  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |MAPI передаваемого  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство содержит изображение значка, то же, что содержимое в размером 32 на 32 пикселя. Файл ICO. Это свойство обычно копируются из. ICO-файла, указанного в строке LargeIcon соответствующий раздел [Описание] файла конфигурации формы. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagMiniIcon](pidtagminiicon-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

