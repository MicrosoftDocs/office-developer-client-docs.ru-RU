---
title: Каноническое свойство PidTagImportance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6bef8b05f2fbf94b74ee126b80dfc6ae0c5e9d11
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400833"
---
# <a name="pidtagimportance-canonical-property"></a>Каноническое свойство PidTagImportance

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение, которое указывает мнение отправителя сообщения о важность сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_IMPORTANCE  <br/> |
|Идентификатор:  <br/> |0x0017  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Не следует путать это свойство и свойство **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)). Importance указывает значение для пользователей, а приоритет указывает порядок или скорость, при которой сообщения направляются программным обеспечением системы обмена сообщениями. Более высокий приоритет обычно указывает выше затрат. Важность выше обычно связан с другой дисплей с помощью пользовательского интерфейса. 
  
Это свойство может иметь только один из следующих значений:
  
IMPORTANCE_LOW 
  
> Сообщение имеет Низкая важность.
    
IMPORTANCE_HIGH 
  
> Сообщение имеет высокой важности.
    
IMPORTANCE_NORMAL 
  
> Сообщение имеет обычную.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
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

