---
title: Каноническое свойство PidTagCorrelate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelate
api_type:
- HeaderDef
ms.assetid: be34993e-ffcc-47f5-b2d4-95ffa707bc5c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 063e41bf9fe306b3862e302abb4495ca56e3087b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575457"
---
# <a name="pidtagcorrelate-canonical-property"></a>Каноническое свойство PidTagCorrelate

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если отправитель сообщения запрашивает взаимосвязи компонентов системы обмена сообщениями.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CORRELATE  <br/> |
|Идентификатор:  <br/> |0x0E0C  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство используется для запроса корреляции входящих отчетов с помощью исходного отправленное сообщение. Когда поставщика транспорта обнаруживает отправленное сообщение с набором **PR_CORRELATE** значение TRUE, свойство **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) присваивается идентификатор система передачи сообщений для этого сообщения.
  
 **PR_CORRELATE** следует использовать с системой обмена сообщениями систем, которые поддерживают корреляции по идентификатору MTS, такие как X.400. 
  
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

