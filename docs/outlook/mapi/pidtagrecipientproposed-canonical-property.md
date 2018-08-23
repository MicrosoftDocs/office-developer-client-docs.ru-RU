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
ms.openlocfilehash: 2e00f121bf52f2c6fcbe797fb8f6126584444411
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580693"
---
# <a name="pidtagrecipientproposed-canonical-property"></a>Каноническое свойство PidTagRecipientProposed

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает, были ли получены участник собрания.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_PROPOSED  <br/> |
|Идентификатор:  <br/> |0x5FE1  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Получатель транспорта  <br/> |
   
## <a name="remarks"></a>Замечания

Значение TRUE для этого свойства указывает, что участник предложенное новые даты и времени. Значение FALSE или отсутствие этого свойства означает, что участник не еще не ответил, либо самыми последними ответа от участника не включить новые даты / времени предложения. Это значение не должно быть значение TRUE для участников в ряду.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
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

