---
title: Каноническое свойство PidTagOriginalAuthorSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorSearchKey
api_type:
- COM
ms.assetid: 4a10cf99-c5e6-4a24-b531-3aebb7800bfe
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 09331e1201b6f6e45bb9e26e618ee59e67efbf8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356261"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a>Каноническое свойство PidTagOriginalAuthorSearchKey

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит ключ поиска автора первой версии сообщения, то есть сообщение, перед которым вы пересылаете или ответили.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ОРИГИНАЛ_АУСОР_СЕАРЧ_КЭЙ  <br/> |
|Идентификатор:  <br/> |0x0056  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Сервер  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является одним из свойств адреса автора сообщения. При первой отправке сообщения клиентскому приложению следует задать для этого свойства значение свойства **пр_сендер_сеарч_кэй**[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) . Он никогда не изменяется при пересылке сообщения или ответе на него. 
  
Исходные свойства автора допускают сохранение данных извне локального домена обмена сообщениями. Когда сообщение поступает из другого домена обмена сообщениями (например, из Интернета), эти свойства предоставляют способ гарантировать, что исходные данные не будут потеряны.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

