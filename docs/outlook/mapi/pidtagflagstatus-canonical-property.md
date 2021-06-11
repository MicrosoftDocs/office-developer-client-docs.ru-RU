---
title: Каноническое свойство PidTagFlagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagStatus
api_type:
- HeaderDef
ms.assetid: b5117360-0939-4535-83fe-3b4a240b5217
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bca8fccaa43bb3157b3d4e2af7d6aafa64972b41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316298"
---
# <a name="pidtagflagstatus-canonical-property"></a>Каноническое свойство PidTagFlagStatus

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает состояние флага объекта сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_FLAG_STATUS  <br/> |
|Идентификатор:  <br/> |0x1090  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство не должно существовать на объекте, связанном с собранием, и не должно существовать на объекте задачи. При заданной на других объектах сообщений это свойство должно быть заданной для одного из следующих значений:
  
|**Числовая величина**|**Имя**|**Описание**|
|:-----|:-----|:-----|
|Не присутствует  <br/> |Н/Д  <br/> |Unflagged  <br/> |
|0x00000001  <br/> |followupComplete  <br/> |Пометка завершена  <br/> |
|0x00000002  <br/> |followupFlagged  <br/> |Помечено  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Указывает свойства и операции, связанные с маркировкой.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

