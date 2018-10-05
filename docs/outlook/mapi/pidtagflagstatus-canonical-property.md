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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390557"
---
# <a name="pidtagflagstatus-canonical-property"></a>Каноническое свойство PidTagFlagStatus

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает состояние флага объекта message.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_FLAG_STATUS  <br/> |
|Идентификатор:  <br/> |0x1090  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство должно отсутствовать для объекта, связанные с собрания и не должно быть для объекта задачи. Если установлено на другие объекты сообщения, это свойство должно быть задано одно из следующих значений:
  
|**Числовое значение**|**Имя**|**Описание**|
|:-----|:-----|:-----|
|Этот параметр не указан  <br/> |Н/Д  <br/> |Без отметки  <br/> |
|0x00000001  <br/> |followupComplete  <br/> |Отмеченные завершена  <br/> |
|0x00000002  <br/> |followupFlagged  <br/> |Отмеченные  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Задает свойства и операции, связанные с флагов.
    
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

