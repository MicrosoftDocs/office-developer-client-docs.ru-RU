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
ms.openlocfilehash: 972df747e0ee459996b9b4da5732be1490fbd08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417128"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a>Каноническое свойство PidTagConversionWithLossProhibited

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит true, если агенту передачи сообщений запрещено преобразование текста сообщения, которое теряет сведения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONVERSION_WITH_LOSS_PROHIBITED  <br/> |
|Идентификатор:  <br/> |0x000D  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Общая конфигурация  <br/> |
   
## <a name="remarks"></a>Примечания

В качестве примера запрещенного типа преобразования можно привести сопоставление "lossy" из Юникода (два на символ) в однобайтовом наборе символов. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

