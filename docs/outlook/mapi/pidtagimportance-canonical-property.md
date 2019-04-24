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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327925"
---
# <a name="pidtagimportance-canonical-property"></a>Каноническое свойство PidTagImportance

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение, указывающее на отправителя сообщения о важности сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ИМПОРТАНЦЕ  <br/> |
|Идентификатор:  <br/> |0x0017  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общий обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Комментарии

Это свойство и свойство **пр_приорити** ([PidTagPriority](pidtagpriority-canonical-property.md)) не следует путать. Важность указывает на значение для пользователей, а Priority указывает порядок или скорость, при которой сообщение должно быть отправлено программным обеспечением системы обмена сообщениями. Более высокий приоритет обычно указывает на более высокую стоимость. Более высокая важность обычно связана с другим отображением пользовательского интерфейса. 
  
Это свойство может иметь только одно из следующих значений:
  
ИМПОРТАНЦЕ_ЛОВ 
  
> Сообщение имеет низкую важность.
    
ИМПОРТАНЦЕ_ХИГХ 
  
> Сообщение имеет высокую важность.
    
ИМПОРТАНЦЕ_НОРМАЛ 
  
> Сообщение имеет обычную важность.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
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

