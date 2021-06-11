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
|Связанные свойства:  <br/> |PR_PRIORITY  <br/> |
|Идентификатор:  <br/> |0x0026  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Электронная почта  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство и **PR_IMPORTANCE** [(PidTagImportance)](pidtagimportance-canonical-property.md)не следует путать. Значение указывает значение для пользователей, в то время как приоритет указывает порядок или скорость отправки сообщения программным обеспечением системы обмена сообщениями. Более высокий приоритет обычно указывает на более высокую стоимость. Более высокое значение обычно связано с другим отображением пользовательского интерфейса.
  
Приоритет сообщения отчетов должен быть таким же, как и приоритет исходного сообщения.
  
Это свойство может иметь одно из следующих значений:
  
PRIO_NONURGENT 
  
> Сообщение не является срочным.
    
PRIO_NORMAL 
  
> Сообщение имеет обычный приоритет.
    
PRIO_URGENT 
  
> Сообщение является срочным.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые на объектах сообщений электронной почты.
    
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

