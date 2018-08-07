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
ms.openlocfilehash: 799f83b397cbef9d7dcb6c9a88154b88afe35675
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19811009"
---
# <a name="pidtagcontrolid-canonical-property"></a>Каноническое свойство PidTagControlId

  
  
**Относится к**: Outlook 
  
Содержит уникальный идентификатор для элемента управления, используемый в диалоговом окне. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTROL_ID  <br/> |
|Идентификатор:  <br/> |0x3F07  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Таблица отображения MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство содержит уникальный идентификатор для элемента управления. Этот идентификатор должен содержать структуры [GUID](guid.md) и двоичное значение типа **LONG**. Все элементы управления в диалоговом окне должны использовать же **идентификатор GUID** для идентификации поставщика услуг, а все элементы управления, следует использовать уникальное значение **LONG** , чтобы убедиться, что элементы управления не перекрывались. 
  
Это свойство используется в уведомления. Например уведомлений, отправленных в таблице отображения необходимо установить это свойство для уникальной идентификации элемента управления для обновления. 
  
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

