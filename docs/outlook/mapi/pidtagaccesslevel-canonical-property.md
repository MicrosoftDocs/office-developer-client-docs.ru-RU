---
title: Каноническое свойство PidTagAccessLevel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccessLevel
api_type:
- HeaderDef
ms.assetid: 8f7119c7-ffc3-47cf-aa1b-b4e56bcc5a24
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5138f5d255f6a90d2891fe2cf5ce92513463fa31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331999"
---
# <a name="pidtagaccesslevel-canonical-property"></a>Каноническое свойство PidTagAccessLevel

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает уровень доступа клиента к объекту.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_АКЦЕСС_ЛЕВЕЛ  <br/> |
|Идентификатор:  <br/> |0x0FF7  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Свойства управления доступом  <br/> |
   
## <a name="remarks"></a>Комментарии

Для клиента это свойство доступно только для чтения. Он должен иметь одно из следующих значений:
  
|**Value**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |Только чтение  <br/> |
|0x00000001  <br/> |Изменение  <br/> |
   
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
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

