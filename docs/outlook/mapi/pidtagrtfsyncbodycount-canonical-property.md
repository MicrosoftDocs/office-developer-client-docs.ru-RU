---
title: Каноническое свойство PidTagRtfSyncBodyCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCount
api_type:
- COM
ms.assetid: b7267be4-8d5c-4dc7-86b2-651e03e84f9b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6f6e687412dfce1e5fcee6b4a4d64f3e5106455f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398803"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a>Каноническое свойство PidTagRtfSyncBodyCount

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит число значительные символов из текста сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RTF_SYNC_BODY_COUNT  <br/> |
|Идентификатор:  <br/> |0x1007  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Сообщение MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Функция [RTFSync](rtfsync.md) вычисляет число символов в текст, используя только те, которые считаются важными к сообщению. Например некоторые пробелов и других допускающие игнорирование символы опускаются из числа. 
  
Это свойство является свойством дополнительный форматированный текст (RTF). Эти свойства, используемые функцией **RTFSync** и не предназначен для непосредственного использования в клиентских приложениях. 
  
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

