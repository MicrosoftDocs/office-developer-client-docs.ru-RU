---
title: Каноническое свойство PidTagRuleUserFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleUserFlags
api_type:
- COM
ms.assetid: c5dfb21f-b35e-4521-bf2b-e3d03d98d75d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 235efce341e1870f0c33917f1c6d42b021727308
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321345"
---
# <a name="pidtagruleuserflags-canonical-property"></a>Каноническое свойство PidTagRuleUserFlags

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Это свойство задается клиентом для эксклюзивного использования клиента. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_РУЛЕ_УСЕР_ФЛАГС  <br/> |
|Идентификатор:  <br/> |0x6678  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Правила на стороне сервера  <br/> |
   
## <a name="remarks"></a>Замечания

Сервер должен сохранить значение этого свойства, если оно было задано клиентом. Сервер должен игнорировать его во время оценки и обработки правила.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОРУЛЕ]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Управляет входящими сообщениями электронной почты на сервере.
    
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

