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
  
Содержит список ASCII отображаемого имени всех получателей сообщений с слепой копией углерода (BCC), разделенных полуколонами (;).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W  <br/> |
|Идентификатор:  <br/> |0x0E02  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Хранилище сообщений вычисляет эти свойства на объектах сообщений с помощью метода [IMessage::ModifyRecipients.](imessage-modifyrecipients.md) Хранилище сообщений также сохраняет эти свойства, чтобы оно всегда отражало последнее сохраненное состояние сообщения. Значение синхронизируется во время каждого вызова метода [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
  
Если в сообщении нет получателей слепой копии углерода, хранилище сообщений должно отвечать на вызов [IMAPIProp::GetProps](imapiprop-getprops.md) с возвратным значением S_OK и пустой строкой для **PR_DISPLAY_BCC**. 
  
В связи с возможной необходимостью локализации MAPI предоставляет эти рекомендации для всех имен получателей:
  
- Все имена должны быть локализованы. 
    
- Полуколон должен быть персонажем, используемым для отдельных имен в свойствах **PR_DISPLAY_BCC,** **PR_DISPLAY_CC** [(PidTagDisplayCc)](pidtagdisplaycc-canonical-property.md)и PR_DISPLAY_TO  [(PidTagDisplayTo).](pidtagdisplayto-canonical-property.md) Семиколоны не допускаются в именах получателей в MAPI. 
    
- Перед тем, как сделать сведения о свойстве видимыми в пользовательском интерфейсе, клиенты должны перевести каждый полуколон, с которым сталкиваются в этом свойстве, в локализованный символ сепаратора. 
    
- При перенаправлении сообщений клиентам не нужно переводить символы сепаратора на слепую строку получателя копирования углерода. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Описывает формат сообщений, используемых для отправки сведений, связанных с совместной папкой клиента.
    
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

