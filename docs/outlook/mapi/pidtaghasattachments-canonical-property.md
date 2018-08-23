---
title: Каноническое свойство PidTagHasAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagHasAttachments
api_type:
- HeaderDef
ms.assetid: fd236d74-2868-46a8-bb3d-17f8365931b6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 505f9bb80c86b956cd920348f2120f7fc8494d8b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587504"
---
# <a name="pidtaghasattachments-canonical-property"></a>Каноническое свойство PidTagHasAttachments

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если сообщение содержит по крайней мере одного вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_HASATTACH  <br/> |
|Идентификатор:  <br/> |0x0E1B  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство копирует хранилища сообщений из флаг **MSGFLAG_HASATTACH** свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Клиентское приложение затем можно использовать **PR_HASATTACH** для сортировки вложений сообщений в средстве просмотра сообщений. 
  
Значение этого свойства обновляются с помощью метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
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

