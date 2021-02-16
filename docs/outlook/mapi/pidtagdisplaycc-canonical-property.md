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
  
Содержит список ASCII отображаемого имени всех получателей сообщений копии (CC), разделенных точками с заглухой (;). 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W  <br/> |
|Идентификатор:  <br/> |0x0E03  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Хранилище сообщений вычисляет эти свойства объектов сообщений с помощью метода [IMessage::ModifyRecipients.](imessage-modifyrecipients.md) Хранилище сообщений также поддерживает эти свойства, чтобы оно всегда отображало последнее сохраненное состояние сообщения. Значение синхронизируется во время каждого вызова [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
  
Если в сообщении нет получателей копии, хранилище сообщений должно ответить на вызов [IMAPIProp::GetProps](imapiprop-getprops.md) с возвращаемым значением S_OK и пустой строкой для этих свойств. 
  
В связи с возможной необходимостью локализации MAPI предоставляет следующие рекомендации для всех имен получателей:
  
- Все имена должны быть локализованы. 
    
- Точка с запоем должна быть символом, используемым для раздельного имен в свойствах **PR_DISPLAY_BCC** ([PidTagDisplayBcc),](pidtagdisplaybcc-canonical-property.md) **PR_DISPLAY_CC** и **PR_DISPLAY_TO** ([PidTagDisplayTo).](pidtagdisplayto-canonical-property.md) В MAPI имена получателей не допускаются. 
    
- Перед тем как сделать сведения о свойстве видимыми в пользовательском интерфейсе, клиенты должны перевести все точки с заданной точки с заданной точки в этом свойстве в локализованный знак сепаратора. 
    
- При перенаправлении сообщений клиентам не нужно переводить знаки в строке получателя копии. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

