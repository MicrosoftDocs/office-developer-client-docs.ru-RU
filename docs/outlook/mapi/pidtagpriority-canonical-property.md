---
title: Каноническое свойство PidTagPriority
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b9c0f5ebeae21d6d683bbb5def727d29a34bcdb6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385454"
---
# <a name="pidtagpriority-canonical-property"></a>Каноническое свойство PidTagPriority

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит относительный приоритет сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PRIORITY  <br/> |
|Идентификатор:  <br/> |0x0026  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Электронная почта  <br/> |
   
## <a name="remarks"></a>Замечания

Не следует путать это свойство и свойство **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)). Importance указывает значение для пользователей, а приоритет указывает порядок или скорость, при которой сообщения направляются программным обеспечением системы обмена сообщениями. Более высокий приоритет обычно указывает выше затрат. Важность выше обычно связан с другой дисплей с помощью пользовательского интерфейса.
  
Приоритет сообщения отчета должен совпадать с приоритетом исходное сообщение об.
  
Это свойство может иметь только один из следующих значений:
  
PRIO_NONURGENT 
  
> Сообщение не является срочным.
    
PRIO_NORMAL 
  
> Сообщение имеет обычным приоритетом.
    
PRIO_URGENT 
  
> Сообщение является срочным.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
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

