---
title: Каноническое свойство PidTagSupplementaryInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIi.PidTagSupplementaryInfo
api_type:
- COM
ms.assetid: 2d4231b5-4096-4c0d-b694-65e2d04172b8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: de9635fa77cd0c282723e0f76eabd6bc0d0dbab9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429756"
---
# <a name="pidtagsupplementaryinfo-canonical-property"></a>Каноническое свойство PidTagSupplementaryInfo

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит дополнительные сведения для использования в отчете.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SUPPLEMENTARY_INFO, PR_SUPPLEMENTARY_INFO_A, PR_SUPPLEMENTARY_INFO_W  <br/> |
|Идентификатор:  <br/> |0x0C1B  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Получатель MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства содержат сведения, созданные агентом передачи сообщений или поставщиком транспорта, связанными с отчетом. Он обычно используется для доставки или неделивного текста отчета, который возник с помощью системы обмена сообщениями.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

