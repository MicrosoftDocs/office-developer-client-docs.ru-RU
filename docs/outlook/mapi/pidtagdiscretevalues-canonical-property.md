---
title: Каноническое свойство PidTagDiscreteValues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDiscreteValues
api_type:
- HeaderDef
ms.assetid: 958f3cf7-953a-43f4-9102-ad35edf5e813
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6d6974302e3413db3590abbbd3e6567976c6ac72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404843"
---
# <a name="pidtagdiscretevalues-canonical-property"></a>Каноническое свойство PidTagDiscreteValues

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит true, если отчет о ненастроений применяется только к дискретным членам списка рассылки, а не ко всему списку. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DISCRETE_VALUES  <br/> |
|Идентификатор:  <br/> |0x0E0E  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |MAPI, не передаваемый  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство используется в отчете о ненастройстве, если сообщение не может быть доставлено одному или более членам списка рассылки. Его цель — ограничить попытки повторной передачи только отдельными участниками, а не списком рассылки в целом. 
  
Таблица получателей отчета о ненастройстве содержит записи для всех получателей, которым не удалось доставить сообщение, а также для списков рассылки, если таково, к которым они принадлежат. Поставщик транспорта должен установить для этого свойства true для каждой записи списка рассылки. и он должен скопировать **свойства PR_DISPLAY_NAME** [(PidTagDisplayName),](pidtagdisplayname-canonical-property.md) **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)и **PR_SEARCH_KEY** ([PidTagSearchKey)](pidtagsearchkey-canonical-property.md)из списка рассылки в свойства **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName),](pidtagoriginaldisplayname-canonical-property.md) **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId)](pidtagoriginalentryid-canonical-property.md)и **PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey)](pidtagoriginalsearchkey-canonical-property.md)для каждого члена этого списка рассылки. 
  
 **PR_DISCRETE_VALUES** не следует устанавливать для записи получателя отчетов о ненастроений, кроме списка рассылки. 
  
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

