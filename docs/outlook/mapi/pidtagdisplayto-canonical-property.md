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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360790"
---
# <a name="pidtagdisplayto-canonical-property"></a>Каноническое свойство PidTagDisplayTo

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит список отображаемых имен основных получателей сообщения (к), разделенных точкой с запятой (;). 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ДИСПЛАЙ_ТО, ПР_ДИСПЛАЙ_ТО_А, ПР_ДИСПЛАЙ_ТО_В  <br/> |
|Идентификатор:  <br/> |0x0E04  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Хранилище сообщений вычисляет эти свойства объектов сообщений с помощью метода [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) . Кроме того, хранилище сообщений поддерживает эти свойства, чтобы всегда отображалось последнее сохраненное состояние сообщения. Значение синхронизируется во время каждого вызова метода [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . 
  
Если у сообщения нет основного получателя, то оно должно отвечать на вызов [IMAPIProp::::](imapiprop-getprops.md) /PROPS со значением, возвращаемым значением S_OK, и пустой строкой для **пр_дисплай_то**. 
  
Из-за возможной локализации MAPI предоставляет следующие рекомендации для всех имен получателей:
  
- Все имена должны быть локализованы. 
    
- Точка с запятой должна быть символом, который используется для разделения имен в свойствах **пр_дисплай_бкк** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **Пр_дисплай_кк** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) и **пр_дисплай_то** . Точки с запятой не допускаются в именах получателей в MAPI. 
    
- Клиенты должны перевести каждую точку с запятой, обнаруженную в **пр_дисплай_то** , и связанные свойства на локализованный символ разделителя перед отображением информации в пользовательском интерфейсе. 
    
- При пересылке сообщений клиентам не требуется переводить символы разделения на строку основного получателя. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
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

