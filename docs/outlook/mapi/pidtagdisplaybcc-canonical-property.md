---
title: Каноническое свойство PidTagDisplayBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayBcc
api_type:
- HeaderDef
ms.assetid: ab5bcd67-d54e-46e9-b94e-a652aac3e81c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 74669d102462e1a825568615d1d30346e99e90a6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388261"
---
# <a name="pidtagdisplaybcc-canonical-property"></a>Каноническое свойство PidTagDisplayBcc

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит список ASCII отображаемые имена получателей скрытой копии (СК) сообщения, разделенные точкой с запятой (;).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W  <br/> |
|Идентификатор:  <br/> |0x0E02  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Замечания

Хранилище сообщений вычисляет эти свойства сообщения объектов с помощью метода [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . Хранилище сообщений также поддерживает эти свойства, чтобы он всегда отражает последнее состояние сохраненного сообщения. Значение синхронизируется во время каждого вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
  
Если сообщение не имеет скрытой копии получателей, хранилища сообщений должны ответить на звонок [IMAPIProp::GetProps](imapiprop-getprops.md) с возвращаемое значение S_OK и пустая строка для **PR_DISPLAY_BCC**. 
  
Из-за возможных необходимость локализации MAPI предоставляет эти руководства для всех получателей:
  
- Все имена должна появиться возможность локализуется. 
    
- Точка с запятой должна быть символ, который используется для разделения имен в **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) и свойства **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)). Точка с запятой не допускается в рамках получателей в MAPI. 
    
- Клиенты должны переведите каждой точкой с запятой, возникала в этом свойстве для локализованных разделитель перед внесением сведения свойство visible в пользовательском интерфейсе. 
    
- При пересылке сообщения, клиенты не требуется переводить разделители в строке получателей скрытой копии. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Описывает формат сообщений, используемые для отправки сведения, относящиеся к общим папкам на стороне клиента.
    
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

