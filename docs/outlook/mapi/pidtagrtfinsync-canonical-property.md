---
title: Каноническое свойство PidTagRtfInSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfInSync
api_type:
- COM
ms.assetid: 443cc68e-7898-4285-a606-f916fcd18554
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 85e517601d291f144652befa267d8fd8f76dea64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811770"
---
# <a name="pidtagrtfinsync-canonical-property"></a>Каноническое свойство PidTagRtfInSync

  
  
**Относится к**: Outlook 
  
Содержит значение TRUE, если свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) имеет то же содержимое текста как свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) для данного сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RTF_IN_SYNC  <br/> |
|Идентификатор:  <br/> |0x0E1F  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Электронная почта  <br/> |
   
## <a name="remarks"></a>Замечания

Значение TRUE означает, что свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), версия обычного текста сообщения и свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) версии форматированный текст (RTF), идентичны за исключением пробелы в **PR_BODY** и форматирование в **PR_RTF_COMPRESSED**. Текст в двух версий состоит из те же символы в той последовательности.
  
Значение FALSE, означает, что две версии не синхронизированы для текстового контента, но позволяют выполнять синхронизацию с помощью функции [RTFSync](rtfsync.md) . Изменил одной версии и не имеет другой версии. 
  
Значение не означает, что две версии, если оба существует, или когда-либо существовало не удалось выполнить синхронизацию. Одной версии был удален или изменен радикально, что синхронизация невозможна.
  
Клиентское приложение, которое были изменены **PR_RTF_COMPRESSED** необходимо задать значение FALSE в этом свойстве для принудительной синхронизации. Хранилищ принять во внимание RTF сообщений следует выполнять синхронизацию с помощью **RTFSync** во время вызова [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Принять во внимание RTF клиентов следует проверить значение **PR_RTF_IN_SYNC** перед чтением **PR_RTF_COMPRESSED**и сначала вызывать **RTFSync** , если это необходимо. 
  
Если **PR_BODY** у которого изменения отличное от его пробелы, хранилище сообщений необходимо удалить **PR_RTF_IN_SYNC** для завершения синхронизации. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
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

