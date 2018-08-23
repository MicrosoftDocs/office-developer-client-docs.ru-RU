---
title: Каноническое свойство PidLidToDoTitle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9973e68dbceea03f31bfc47ede34f004fa3f39b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570417"
---
# <a name="pidlidtodotitle-canonical-property"></a>Каноническое свойство PidLidToDoTitle

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит текст, при этом задаваемый пользователем для идентификации этот объект сообщения в списке дел консолидированной среды.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidToDoTitle  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x000085A4  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство не должен задаваться на задачу. Для указания пустой свойство, не задавайте это свойство строку нулевой длины, но вместо этого удалите его. 
  
Когда пометка объекта message и свойство не существует, клиент указывайте значение **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) для данного свойства.
  
В списке дел консолидированной Если это свойство не существует, клиент следует заменить значение свойства **PR_NORMALIZED_SUBJECT** при отображении этого свойства в списке дел. 
  
Для объекта черновика сообщения Если клиент реализует флаги отправителя, это свойство должно быть присвоено совпадает со значением **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Задает свойства и операции, связанные с флагов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
  
[������������ �������� PidLidFlagRequest](pidlidflagrequest-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

