---
title: Каноническое свойство PidTagToDoItemFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagToDoItemFlags
api_type:
- COM
ms.assetid: bb7ccb45-ce08-4d22-9259-db15cd267e34
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6ddc7231afef0a224b92be7fe86216e56200ab70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284485"
---
# <a name="pidtagtodoitemflags-canonical-property"></a>Каноническое свойство PidTagToDoItemFlags

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Представляет To-Do пометки элемента.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_TODO_ITEM_FLAGS  <br/> |
|Идентификатор:  <br/> |0x0E2B  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |MAPI, не передаваемый  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является битным полем, в котором каждому биту следует установить 1, если применяется связанное условие в следующей таблице, в противном случае — 0.
  
||||
|:-----|:-----|:-----|
|Числовая величина  <br/> |Имя  <br/> |Описание  <br/> |
|Нет  <br/> |Недоступно  <br/> |Unflagged  <br/> |
|1   <br/> |todoTimeFlagged  <br/> |Объект помечен временем  <br/> |
|8   <br/> |todoRecipientFlagged  <br/> |Следует устанавливать только для объекта черновика сообщения, и это означает, что объект помечается для получателей.  <br/> |
   
Все биты, не указанные в таблице, зарезервированы. Они должны игнорироваться, но должны быть сохранены, если они установлены.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Указывает свойства и операции, связанные с помезданием.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

