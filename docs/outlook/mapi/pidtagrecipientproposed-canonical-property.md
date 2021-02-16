---
title: Каноническое свойство PidTagRecipientProposed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposed
api_type:
- COM
ms.assetid: 8cb0e46c-0937-482f-be78-1f2e5261b210
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1b09d8d7621121b3652ceb9824f6d36b53844206
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283137"
---
# <a name="pidtagrecipientproposed-canonical-property"></a>Каноническое свойство PidTagRecipientProposed

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, ответил ли участник собрания.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_PROPOSED  <br/> |
|Идентификатор:  <br/> |0x5FE1  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Получатель транспорта  <br/> |
   
## <a name="remarks"></a>Примечания

Значение TRUE для этого свойства указывает, что участник предлагает новую дату и/или время. Значение FALSE или отсутствие этого свойства означает либо то, что участник еще не ответил, либо последний ответ участника не включал новое предложение даты и времени. Это значение не должно быть TRUE для участников повторяющегося ряда.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.
    
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

