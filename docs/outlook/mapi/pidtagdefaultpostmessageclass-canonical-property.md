---
title: Каноническое свойство PidTagDefaultPostMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultPostMessageClass
api_type:
- HeaderDef
ms.assetid: 231c288f-547b-4463-9442-1499661b925e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0ab904625d3a23462a4fedf3b64f49c54b34ad28
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401729"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a>Каноническое свойство PidTagDefaultPostMessageClass

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит имя настраиваемой формы класс сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DEF_POST_MSGCLASS  <br/> |
|Идентификатор:  <br/> |0x36E5  <br/> |
|Тип данных:  <br/> |PT_STRING8  <br/> |
|Область:  <br/> |Контейнер MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Если это свойство задано для папки, значение должно содержать либо точно базового класса сообщения (например, «IPM. Контакт» для папки «Контакты» или «IPM. Встреча» для папки «Календарь»), или начинаться с базового класса сообщения (например, «IPM. [[[Contact.MyContact»).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
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

