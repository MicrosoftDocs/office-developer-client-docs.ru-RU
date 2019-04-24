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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339433"
---
# <a name="pidtagpriority-canonical-property"></a>Каноническое свойство PidTagPriority

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит относительный приоритет сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ПРИОРИТИ  <br/> |
|Идентификатор:  <br/> |0x0026  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>Комментарии

Это свойство и свойство **пр_импортанце** ([PidTagImportance](pidtagimportance-canonical-property.md)) не следует путать. Важность указывает на значение для пользователей, а Priority указывает порядок или скорость, при которой сообщение должно быть отправлено программным обеспечением системы обмена сообщениями. Более высокий приоритет обычно указывает на более высокую стоимость. Более высокая важность обычно связана с другим отображением пользовательского интерфейса.
  
Приоритет сообщения отчета должен совпадать с приоритетом исходного сообщения.
  
Это свойство может иметь только одно из следующих значений:
  
ПРИО_НОНУРЖЕНТ 
  
> Сообщение не является срочным.
    
ПРИО_НОРМАЛ 
  
> Сообщение имеет обычный приоритет.
    
ПРИО_УРЖЕНТ 
  
> Сообщение срочно.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

