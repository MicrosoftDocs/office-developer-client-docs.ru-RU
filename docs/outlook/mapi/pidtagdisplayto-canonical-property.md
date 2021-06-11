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
  
Содержит список отображаемого имени основных получателей сообщений , разделенных зайколонами (;). 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W  <br/> |
|Идентификатор:  <br/> |0x0E04  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Хранилище сообщений вычисляет эти свойства на объектах сообщений с помощью метода [IMessage::ModifyRecipients.](imessage-modifyrecipients.md) Хранилище сообщений также сохраняет эти свойства, чтобы оно всегда отражало последнее сохраненное состояние сообщения. Значение синхронизируется во время каждого вызова метода [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
  
Если сообщение не имеет основных получателей, хранилище сообщений должно отвечать на вызов [IMAPIProp::GetProps](imapiprop-getprops.md) с возвратным значением S_OK и пустой строкой для **PR_DISPLAY_TO**. 
  
В связи с возможной необходимостью локализации MAPI предоставляет эти рекомендации для всех имен получателей:
  
- Все имена должны быть локализованы. 
    
- Полуколон должен быть персонажем, используемым для отдельных имен  в **PR_DISPLAY_BCC** [(PidTagDisplayBcc),](pidtagdisplaybcc-canonical-property.md) **PR_DISPLAY_CC** [(PidTagDisplayCc)](pidtagdisplaycc-canonical-property.md)и PR_DISPLAY_TO свойствах. Семиколоны не допускаются в именах получателей в MAPI. 
    
- Перед тем, как сделать сведения видимыми в пользовательском интерфейсе, клиенты должны перевести **каждый** полуколон, PR_DISPLAY_TO связанных свойств с локализованным сепаратором. 
    
- При перенаправлении сообщений клиентам не нужно переводить символы сепаратора в основной строке получателя. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

