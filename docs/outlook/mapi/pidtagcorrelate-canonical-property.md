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
ms.openlocfilehash: ea217808a163c7f16bbaa3c5a959fd32c8cbe10c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405221"
---
# <a name="pidtagcorrelate-canonical-property"></a>Каноническое свойство PidTagCorrelate

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит TRUE, если отправитель сообщения запрашивает функцию корреляции системы обмена сообщениями.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CORRELATE  <br/> |
|Идентификатор:  <br/> |0x0E0C  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство используется для запроса корреляции входящих отчетов с исходным отправленным сообщением. Когда поставщик транспорта сталкивается с  отправленным сообщением с PR_CORRELATE для true, он задает свойство **PR_CORRELATE_MTSID** [(PidTagCorrelateMtsid)](pidtagcorrelatemtsid-canonical-property.md)для идентификатора системы передачи сообщений (MTS) для этого сообщения.
  
 **PR_CORRELATE** следует использовать с системами обмена сообщениями, поддерживаюми корреляцию идентификатора МТС, например X.400. 
  
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

