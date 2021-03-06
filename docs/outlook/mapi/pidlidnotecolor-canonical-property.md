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
ms.openlocfilehash: 09d0ee3be704dc55452b615a23ac9cf20d9254d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331362"
---
# <a name="pidlidnotecolor-canonical-property"></a>Каноническое свойство PidLidNoteColor

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает предложенный фоновый цвет заметки. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidNoteColor  <br/> |
|Набор свойств:  <br/> |PSETID_Note  <br/> |
|Long ID (LID):  <br/> |0x00008B00  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Записки  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство должно быть одним из записей в следующей таблице:
  
|**Значение**|**Color**|
|:-----|:-----|
|0x00000000  <br/> |Синий  <br/> |
|0x00000001  <br/> |Зеленый  <br/> |
|0x00000002  <br/> |Розовая  <br/> |
|0x00000003  <br/> |Желтый  <br/> |
|0x00000004  <br/> |Белый  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXONOTE]](https://msdn.microsoft.com/library/6bf4ed7e-316c-4a3c-be27-5ec93e7ab39f%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые в заметках.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

