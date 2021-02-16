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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409582"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a>Каноническое свойство PidTagOriginalAuthorSearchKey

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит ключ поиска автора первой версии сообщения, то есть сообщение перед переадащением или ответом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_AUTHOR_SEARCH_KEY  <br/> |
|Идентификатор:  <br/> |0x0056  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является одним из свойств адреса для автора сообщения. При первой отправке сообщения клиентские приложения должны установить для этого свойства значение свойства **PR_SENDER_SEARCH_KEY**[PidTagSenderSearchKey.](pidtagsendersearchkey-canonical-property.md) Оно никогда не меняется, когда сообщение переадовыно или отвечает на него. 
  
Исходные свойства автора позволяют сохранить информацию из-за пределов локального домена обмена сообщениями. Когда сообщение поступает из другого домена обмена сообщениями, например из Интернета, эти свойства обеспечивают способ обеспечения того, чтобы исходная информация не была потеряна.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

