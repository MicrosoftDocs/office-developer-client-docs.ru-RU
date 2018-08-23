---
title: Каноническое свойство PidTagOriginalSenderSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderSearchKey
api_type:
- COM
ms.assetid: 164eb9dd-e553-459e-99c1-3da0284bb01f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d4a49af0585058c2203807bf091c34808376a7dc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591746"
---
# <a name="pidtagoriginalsendersearchkey-canonical-property"></a>Каноническое свойство PidTagOriginalSenderSearchKey

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит ключ поиска для отправителя первая версия сообщения, то есть, сообщение перед пересылку и ответ.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_SENDER_SEARCH_KEY  <br/> |
|Идентификатор:  <br/> |0x005C  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство является одним из свойств адреса для исходного отправителя сообщения. В первой отправки сообщения клиентское приложение следует этому свойству присвоено значение свойства **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)). Никогда не изменяется при сообщение будет переслано или ответ.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
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

