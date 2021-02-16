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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331257"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a>Каноническое свойство PidTagRtfSyncBodyCount

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит количество важных символов текста сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RTF_SYNC_BODY_COUNT  <br/> |
|Идентификатор:  <br/> |0x1007  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Сообщение MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Функция [RTFSync](rtfsync.md) вычисляет количество символов в тексте, используя только те, которые считаются значимыми для сообщения. Например, некоторые пробелы и другие игнорируемые символы не учитываются в подсчете. 
  
Это свойство является вспомогательным свойством RTF. Эти свойства используются функцией **RTFSync** и не предназначены для непосредственного использования клиентских приложений. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.
    
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

