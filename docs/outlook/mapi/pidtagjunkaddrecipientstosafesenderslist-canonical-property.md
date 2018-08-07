---
title: Каноническое свойство PidTagJunkAddRecipientsToSafeSendersList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkAddRecipientsToSafeSendersList
api_type:
- HeaderDef
ms.assetid: 78543caa-e6ec-4ac7-bfdd-70c56f8fd955
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8c104af106a885f42f8063bcf5fb55d654f2688e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811284"
---
# <a name="pidtagjunkaddrecipientstosafesenderslist-canonical-property"></a>Каноническое свойство PidTagJunkAddRecipientsToSafeSendersList

  
  
**Относится к**: Outlook 
  
Указывает ли получателей почты, добавляемого в список надежных отправителей.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_JUNK_ADD_RECIPS_TO_SSL  <br/> |
|Идентификатор:  <br/> |0x6103  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Нежелательной почты  <br/> |
   
## <a name="remarks"></a>Замечания

Если этот параметр указан, это свойство должно иметь значение 0 или 1. Значение 1 указывает, что получателей почты должны быть добавлены в список надежных отправителей. Значение 0 указывает, что получателей почты не следует добавить в список надежных отправителей.
  
Если это свойство со значением 1, SMTP-адреса получателей сообщения электронной почты необходимо добавить для надежных отправителей предложение условия правила нежелательной электронной почты. Если это свойство равно 0, никаких действий не требуется.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.
    
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

