---
title: Каноническое свойство PidTagFormDesignerGuid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormDesignerGuid
api_type:
- HeaderDef
ms.assetid: 8d7f5789-610c-47f6-a109-5513d677ef60
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b0e0847a3a9e21f080a852738ec8afbc98a2263f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412242"
---
# <a name="pidtagformdesignerguid-canonical-property"></a>Каноническое свойство PidTagFormDesignerGuid

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит уникальный идентификатор объекта, который используется для разработки формы.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_FORM_DESIGNER_GUID  <br/> |
|Идентификатор:  <br/> |0x3309  <br/> |
|Тип данных:  <br/> |PT_GUID  <br/> |
|Область:  <br/> |MAPI общие  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство обычно содержит глобальный уникальный идентификатор (GUID) программы разработки, которая используется для создания формы. Это свойство может быть пустым. 
  
Структура [MAPIUID](mapiuid.md) содержит определение уникального идентификатора. 
  
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

