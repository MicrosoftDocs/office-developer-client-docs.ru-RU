---
title: Каноническое свойство PidTagTitle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTitle
api_type:
- COM
ms.assetid: f35bbcc3-15dd-40ab-9bf4-bdb21f95d464
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 825922bec95a24fe718cdb7db82851a820c364ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812004"
---
# <a name="pidtagtitle-canonical-property"></a>Каноническое свойство PidTagTitle

  
  
**Относится к**: Outlook 
  
Содержит название должности получателя.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_TITLE, PR_TITLE_A, PR_TITLE_W  <br/> |
|Идентификатор:  <br/> |0x3A17  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Пользователь почты MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства предоставляют идентификации и доступа к сведениям для получателя. Они определены получателя и организации получателя. 
  
Эти свойства обычно используются для указания заголовок официальную задания получателя, например ведущего программиста, а не производственная класса, такие как программиста. Обычно не используется для заголовков «суффикс», например Esq. или набору доменов Обнаружения.
  
Включить общие значения для этого свойства: генеральный директор, программист II, свяжите профессора и руководитель группы разработки. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контакты и списки рассылки.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
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

