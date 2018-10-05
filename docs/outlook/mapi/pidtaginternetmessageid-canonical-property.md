---
title: Каноническое свойство PidTagInternetMessageId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetMessageId
api_type:
- HeaderDef
ms.assetid: 5c93d00c-a199-4d45-9bf6-87bd2ffe4784
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c2cc0eabd9c329953d9b0d252418549ea1c588a1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391929"
---
# <a name="pidtaginternetmessageid-canonical-property"></a>Каноническое свойство PidTagInternetMessageId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Соответствует поле идентификатор сообщения, как указано в [RFC2822].
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W  <br/> |
|Идентификатор:  <br/> |0x1035  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства должны быть настроены на все сообщения электронной почты.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
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

