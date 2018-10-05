---
title: Каноническое свойство PidTagDisplayTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTo
api_type:
- HeaderDef
ms.assetid: 700cc03b-5d98-40ce-adb5-a11fdac8aa28
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0c7ae8951b02f099161871b17ff59ea23f8fbcc4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396045"
---
# <a name="pidtagdisplayto-canonical-property"></a>Каноническое свойство PidTagDisplayTo

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит список отображаемые имена основной (по) получателей сообщения, разделенных точкой с запятой (;). 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W  <br/> |
|Идентификатор:  <br/> |0x0E04  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Замечания

Хранилище сообщений вычисляет эти свойства сообщения объектов с помощью метода [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . Хранилище сообщений также поддерживает эти свойства, чтобы он всегда отражает последнее состояние сохраненного сообщения. Значение синхронизируется во время каждого вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
  
Если сообщение не имеет основной получателей, хранилище сообщений должны отвечать на звонок [IMAPIProp::GetProps](imapiprop-getprops.md) с возвращаемое значение S_OK и пустая строка для **PR_DISPLAY_TO**. 
  
Из-за возможных необходимость локализации MAPI предоставляет эти руководства для всех получателей:
  
- Все имена должна появиться возможность локализуется. 
    
- Точка с запятой должна быть символ, который используется для разделения имен в **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) и **PR_DISPLAY_TO** свойств. Точка с запятой не допускается в рамках получателей в MAPI. 
    
- Клиенты следует перевести каждого сталкивались с запятой в **PR_DISPLAY_TO** и связанных с ними свойства для локализованных разделитель перед внесением сведения видны в пользовательском интерфейсе. 
    
- При пересылке сообщения, клиенты не требуется переводить разделители в строке основной получателя. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

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

