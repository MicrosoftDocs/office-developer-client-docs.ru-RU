---
title: Каноническое свойство PidTagImplicitConversionProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImplicitConversionProhibited
api_type:
- HeaderDef
ms.assetid: c6cb5a86-0105-4743-9f8e-b832e898da52
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a0e18ef529b65317abd9446408ed73638c792809
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420670"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a>Каноническое свойство PidTagImplicitConversionProhibited

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если агенту передачи сообщений (MTA) запрещено делать неявные преобразования текста сообщений.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_IMPLICIT_CONVERSION_PROHIBITED  <br/> |
|Идентификатор:  <br/> |0x0016  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Сервер  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство имеет значение TRUE, система обмена сообщениями не должна выполнять преобразование содержимого для сообщения, если оно не будет явно запрошено для каждого получателя с помощью свойства **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

