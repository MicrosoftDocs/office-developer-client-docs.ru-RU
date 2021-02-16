---
title: Каноническое свойство PidTagSentMailEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentMailEntryId
api_type:
- COM
ms.assetid: 8f14dc15-d7d7-4894-b6a8-0d589f576c42
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e7aef8e9ba605d47b110a496e46f629df60a28ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342513"
---
# <a name="pidtagsentmailentryid-canonical-property"></a>Каноническое свойство PidTagSentMailEntryId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи папки, в которой сообщение должно быть перемещено после отправки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SENTMAIL_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x0E0A  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |MAPI, не передаваемый  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство часто копируется из свойства **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId),](pidtagipmsentmailentryid-canonical-property.md)стандартной папки "Отправленные" клиентского приложения.
  
Клиентские приложения используют это свойство со свойством **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit)](pidtagdeleteaftersubmit-canonical-property.md)для управления тем, что происходит с сообщением после его отправки. Следует установить один или несколько из них, но не оба.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.
    
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

