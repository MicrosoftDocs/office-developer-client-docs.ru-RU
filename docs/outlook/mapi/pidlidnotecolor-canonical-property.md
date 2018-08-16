---
title: Каноническое свойство PidLidNoteColor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNoteColor
api_type:
- COM
ms.assetid: 9d4b8f5f-1789-497c-8010-f83da9ba5966
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7ff0bb5ec1eb56724bee7be7dec13f0474711083
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810427"
---
# <a name="pidlidnotecolor-canonical-property"></a>Каноническое свойство PidLidNoteColor

  
  
**Относится к**: Outlook 
  
Задает цвет фона предложенного заметки. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidNoteColor  <br/> |
|Набор свойств:  <br/> |PSETID_Note  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008B00  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Записки  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство должно быть одно из записей в следующей таблице:
  
|**Значение**|**Цвет**|
|:-----|:-----|
|0x00000000  <br/> |Синий  <br/> |
|0x00000001  <br/> |Зеленый  <br/> |
|0x00000002  <br/> |Розовым  <br/> |
|0x00000003  <br/> |Желтый  <br/> |
|0x00000004  <br/> |Белый  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXONOTE]](http://msdn.microsoft.com/library/6bf4ed7e-316c-4a3c-be27-5ec93e7ab39f%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые на заметки.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)
