---
title: Каноническое свойство PidTagSwappedToDoData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3ecfa1e89688ae525a28e221424fb4a8194fc217
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386672"
---
# <a name="pidtagswappedtododata-canonical-property"></a>Каноническое свойство PidTagSwappedToDoData

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Поддерживает второй набор значений свойств, которые не влияют на отмеченного состояние объекта сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SWAPPED_TODO_DATA  <br/> |
|Идентификатор:  <br/> |0x0E2D  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |MAPI передаваемого  <br/> |
   
## <a name="remarks"></a>Замечания

Если поддерживается флаги отправителя или напоминания отправителя будет действовать как флаг дополнительного места хранения данных, эта структура предоставляет расположение, в котором хранятся все свойства, относящиеся к информационные Пометка протокола, которые поддерживаются в флаги отправителя и всех свойства относящиеся к протокола параметры напоминания, которые поддерживаются в отправителя напоминаний без предоставление доступа к сведениям о напоминание отправителя в список получателей сообщения или флаг отправителя.
  
Аналогично эта структура предоставляет расположение, в котором хранятся все свойства относящиеся к информационного протокола Пометка, поддерживаемые в получателей флаги и свойства, относящиеся к протокола параметры напоминания, которые поддерживаются в получателя напоминания на ранее отправленное сообщение.
  
Дополнительные сведения об этом свойстве можно [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Задает свойства и операции, связанные с флагов.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Задает свойства и модель взаимодействия для электронной почты и других объектов напоминания.
    
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

