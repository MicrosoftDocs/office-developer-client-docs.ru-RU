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
ms.openlocfilehash: f1aa54c3364185d322137ef41f6aface31c5c556
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587420"
---
# <a name="pidtagdiscretevalues-canonical-property"></a>Каноническое свойство PidTagDiscreteValues

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если о недоставке применяется только для отдельных участников в список рассылки, а не всего списка. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DISCRETE_VALUES  <br/> |
|Идентификатор:  <br/> |0x0E0E  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |MAPI передаваемого  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство используется в рамках о недоставке, когда сообщение не может быть доставлено, для одного или нескольких членов списка рассылки. Он предназначен для ограничения повторной передачи пытается отдельные элементы и не списка рассылки в целом. 
  
Таблице получателей о недоставке содержит записи для всех получателей, к которому сообщение не может быть доставлено, а также для списков рассылки, если они существуют, к которым они относятся. Поставщика транспорта следует этому свойству присвоено значение TRUE для каждой записи списка рассылки, и он должен скопировать **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) и **PR_SEARCH_KEY** ([ PidTagSearchKey](pidtagsearchkey-canonical-property.md)) из списка рассылки, чтобы **PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md)), **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) и **PR_ORIGINAL_SEARCH_KEY** ([ PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md)) свойства для каждого элемента этого списка рассылки. 
  
 **PR_DISCRETE_VALUES** не должен устанавливаться запись получателя отчет о недоставке отличный от списка рассылки. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

