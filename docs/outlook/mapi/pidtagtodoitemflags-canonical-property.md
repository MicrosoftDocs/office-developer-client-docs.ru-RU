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
ms.openlocfilehash: 79f6c90d1ebd2257cc428e88dfce3d9ee9dfeccf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573469"
---
# <a name="pidtagtodoitemflags-canonical-property"></a>Каноническое свойство PidTagToDoItemFlags

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Представляет условие отмеченного элемента списка дел.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_TODO_ITEM_FLAGS  <br/> |
|Идентификатор:  <br/> |0x0E2B  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |MAPI передаваемого  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство представляет битовое поле, в котором каждый бит необходимо задать значение 1 ситуациях связанного условие в следующей таблице, в противном случае — 0.
  
||||
|:-----|:-----|:-----|
|Числовое значение  <br/> |Имя  <br/> |Описание  <br/> |
|Этот параметр не указан  <br/> |Н/Д  <br/> |Без отметки  <br/> |
|1  <br/> |todoTimeFlagged  <br/> |Объект является отметкой времени  <br/> |
|8  <br/> |todoRecipientFlagged  <br/> |Должны быть установлены только на объект черновика сообщения, а это означает, что объект имеет флаг для получателей.  <br/> |
   
Зарезервированные все биты, не указанные в таблице. Они должны игнорироваться, но должны быть сохранены, если они определены.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Задает свойства и операции, связанные с флагов.
    
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

