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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360818"
---
# <a name="pidtagdisplaybcc-canonical-property"></a>Каноническое свойство PidTagDisplayBcc

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит список отображаемых имен получателей скрытой копии (BCC), разделенных точкой с запятой (;).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ДИСПЛАЙ_БКК, ПР_ДИСПЛАЙ_БКК_А, ПР_ДИСПЛАЙ_БКК_В  <br/> |
|Идентификатор:  <br/> |0x0E02  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Хранилище сообщений вычисляет эти свойства объектов сообщений с помощью метода [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) . Кроме того, хранилище сообщений поддерживает эти свойства, чтобы всегда отображалось последнее сохраненное состояние сообщения. Значение синхронизируется во время каждого вызова метода [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . 
  
Если у сообщения нет получателей скрытой копии, то хранилище сообщений должно отвечать на вызов [IMAPIProp::](imapiprop-getprops.md) /PROPS с возвращаемым значением S_OK и пустой строкой для **пр_дисплай_бкк**. 
  
Из-за возможной локализации MAPI предоставляет следующие рекомендации для всех имен получателей:
  
- Все имена должны быть локализованы. 
    
- Точка с запятой должна быть символом, который используется для разделения имен в свойствах **пр_дисплай_бкк**, **пр_дисплай_кк** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) и **пр_дисплай_то** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)). Точки с запятой не допускаются в именах получателей в MAPI. 
    
- Клиенты должны перевести каждую точку с запятой, обнаруженную в этом свойстве, на локализованный символ разделителя, прежде чем сделать сведения о свойстве видимыми в пользовательском интерфейсе. 
    
- При пересылке сообщений клиентам не нужно преобразовывать символы разделения в строку получателей скрытой копии. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Описывает формат сообщений, используемых для отправки сведений, связанных с общими папками на клиенте.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

