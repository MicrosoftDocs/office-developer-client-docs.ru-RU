---
title: Каноническое свойство PidTagControlId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b27f59e0bfdcac8eca1751af2f07139f12e2b3a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416022"
---
# <a name="pidtagcontrolid-canonical-property"></a>Каноническое свойство PidTagControlId

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит уникальный идентификатор для управления, используемого в диалоговом окне. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTROL_ID  <br/> |
|Идентификатор:  <br/> |0x3F07  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Таблица отображения MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство содержит уникальный идентификатор для управления. Этот идентификатор должен содержать структуру [GUID](guid.md) и двоичное значение типа **LONG**. Все элементы управления в диалоговом окне должны использовать один и тот же **GUID** для идентификации поставщика услуг, и каждый элемент управления должен использовать уникальное значение **LONG** для обеспечения того, чтобы элементы управления не сталкивались. 
  
Это свойство используется в уведомлениях. Например, уведомления, отправленные на таблице отображения, должны установить это свойство для уникальной идентификации управления для обновления. 
  
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

