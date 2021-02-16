---
title: Каноническое свойство PidTagOriginalSenderEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEntryId
api_type:
- COM
ms.assetid: bd182589-afea-4967-92f5-ba1914e4db3f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bd32ef6540e0deec1b793bd49bab651d864754c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342618"
---
# <a name="pidtagoriginalsenderentryid-canonical-property"></a>Каноническое свойство PidTagOriginalSenderEntryId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи отправитель первой версии сообщения, то есть сообщение перед переадаемой или ответом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_SENDER_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x005B  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является одним из свойств адреса исходного отправитель сообщения. При первой отправке сообщения клиентские приложения должны установить для этого свойства значение свойства **PR_SENDER_ENTRYID** ([PidTagSenderEntryId).](pidtagsenderentryid-canonical-property.md) Оно никогда не меняется, когда сообщение переадовыно или отвечает на него.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для объектов сообщений электронной почты.
    
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

