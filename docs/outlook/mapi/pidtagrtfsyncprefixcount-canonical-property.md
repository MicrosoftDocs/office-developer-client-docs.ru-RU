---
title: Каноническое свойство PidTagRtfSyncPrefixCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncPrefixCount
api_type:
- COM
ms.assetid: c2b15ac5-9e89-4ee2-812d-102d0b2ac56e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 61683534504b7451f126591af149d11306cff1bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389815"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a>Каноническое свойство PidTagRtfSyncPrefixCount

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит число допускающие игнорирование символы, отображаемые перед значительные символов сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RTF_SYNC_PREFIX_COUNT  <br/> |
|Идентификатор:  <br/> |0x1010  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Сообщение MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Количество символов префикса не включает пробелы.
  
Это свойство является свойством дополнительный форматированный текст (RTF). Дополнительные свойства RTF используется функцией [RTFSync](rtfsync.md) и не предназначен для непосредственного использования в клиентских приложениях. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.
    
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

