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
ms.openlocfilehash: f9800b1822ca6881c451e01e890d582c77b64546
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566749"
---
# <a name="pidtagsupplementaryinfo-canonical-property"></a>Каноническое свойство PidTagSupplementaryInfo

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит дополнительные сведения для использования в отчете.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SUPPLEMENTARY_INFO, PR_SUPPLEMENTARY_INFO_A, PR_SUPPLEMENTARY_INFO_W  <br/> |
|Идентификатор:  <br/> |0x0C1B  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Получатель MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства содержат сведения, сгенерированные агента передачи сообщений или транспорта, связанные с поставщиком к отчету. Обычно используется для доставки или недоставке текст отчета, которая была создана с помощью системы обмена сообщениями.
  
## <a name="related-resources"></a>Связанные ресурсы

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

