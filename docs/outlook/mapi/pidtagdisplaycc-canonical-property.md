---
title: Каноническое свойство PidTagDisplayCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayCc
api_type:
- HeaderDef
ms.assetid: 00377e78-a208-4942-a7a6-893b2a71ab0b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2bf862317ca1d2f2a09a71e1af62b82661b33326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360811"
---
# <a name="pidtagdisplaycc-canonical-property"></a>Каноническое свойство PidTagDisplayCc

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит список отображаемых имен всех получателей сообщений копии (CC), разделенных точкой с запятой (;). 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DISPLAY_CC, PR_DISPLAY_CC_A PR_DISPLAY_CC_W  <br/> |
|Идентификатор:  <br/> |0x0E03  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Хранилище сообщений вычисляет эти свойства объектов сообщений с помощью метода [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) . Кроме того, хранилище сообщений поддерживает эти свойства, чтобы всегда отображалось последнее сохраненное состояние сообщения. Значение синхронизируется во время каждого вызова [IMAPIProp:: SaveChanges](imapiprop-savechanges.md). 
  
Если у сообщения нет получателей копии, то хранилище сообщений должно отвечать на вызов [IMAPIProp::::/PROPS](imapiprop-getprops.md) со значением, возвращаемым S_OK, и пустой строкой для этих свойств. 
  
Из-за возможной локализации MAPI предоставляет следующие рекомендации для всех имен получателей:
  
- Все имена должны быть локализованы. 
    
- Точка с запятой должна быть символом, который используется для разделения имен в свойствах **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**и **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)). Точки с запятой не допускаются в именах получателей в MAPI. 
    
- Клиенты должны перевести каждую точку с запятой, обнаруженную в этом свойстве, на локализованный символ разделителя, прежде чем сделать сведения о свойстве видимыми в пользовательском интерфейсе. 
    
- При пересылке сообщений клиентам не нужно преобразовывать символы разделения в строку получателей копии копии. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

