---
title: Каноническое свойство PidTagJunkThreshold
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkThreshold
api_type:
- HeaderDef
ms.assetid: 8067e2b5-02df-4b96-8f66-509f5a48c8aa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 078dfcc7c24870cf95a2a4b2385c34fbeb64fac0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326854"
---
# <a name="pidtagjunkthreshold-canonical-property"></a>Каноническое свойство PidTagJunkThreshold

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, как агрессивно входящие сообщения следует отправлять в папку нежелательной почты.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_JUNK_THRESHOLD  <br/> |
|Идентификатор:  <br/> |0x6101  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Спам  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство соответствует параметру фильтра high/low/none. Значение "0xFFFFFFFF" указывает на то, что фильтрация нежелательной почты не должна применяться, однако списки блокировки должны по-прежнему применяться. Значение "0x80000000" указывает, что вся почта является нежелательной почтой, за исключением сообщений от отправителей в списке надежных отправителей или отправленных получателям в списке доверенных получателей. Значения для этого:
  
|**Значение**|**Описание**|
|:-----|:-----|
|0xFFFFFFFF  <br/> |Фильтрация нежелательной почты  <br/> |
|0x00000006  <br/> |Низкая фильтрация нежелательной почты  <br/> |
|0x00000003  <br/> |Высокая фильтрация нежелательной почты  <br/> |
|0x80000000  <br/> |Только доверенные списки  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Включает обработку списков разрешить или блокировать и определение нежелательных сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

