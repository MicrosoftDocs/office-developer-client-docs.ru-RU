---
title: Каноническое свойство PidTagConversionWithLossProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversionWithLossProhibited
api_type:
- HeaderDef
ms.assetid: a18b560a-e054-45b3-946d-6504465db5b7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e5d9261a9f33d77d52cfd6e448e69a2c1e8df415
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585236"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a>Каноническое свойство PidTagConversionWithLossProhibited

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если сообщение передачи (агента) — это могут выполнять сообщение преобразования текста, которые потерю данных. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONVERSION_WITH_LOSS_PROHIBITED  <br/> |
|Идентификатор:  <br/> |0x000D  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Общие настройки  <br/> |
   
## <a name="remarks"></a>Замечания

Пример типа преобразования запрещено — это сопоставление «с потерей данных» в кодировке Юникод (два байта на знак) в набор однобайтовых знаков. 
  
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

