---
title: Каноническое свойство PidTagOriginallyIntendedRecipEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEntryId
api_type:
- COM
ms.assetid: fc288a7a-1927-484e-b860-9cc118672ed2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cf9a070e8f892cb7bd4668b3f92397070e5b2284
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430142"
---
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a>Каноническое свойство PidTagOriginallyIntendedRecipEntryId

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи первоначально предназначенного получателя автопроизводиющего сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINALLY_INTENDED_RECIP_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x1012  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является одним из свойств адресов для первоначально предназначенного получателя сообщений. Он должен быть задат автоматическим агентом, переададовав сообщение.
  
Это свойство соответствует атрибуту отчета X.400 для каждого получателя.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

