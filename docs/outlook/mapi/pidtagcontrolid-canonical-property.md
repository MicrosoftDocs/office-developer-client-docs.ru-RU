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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит уникальный идентификатор элемента управления, используемого в диалоговом окне. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTROL_ID  <br/> |
|Идентификатор:  <br/> |0x3F07  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Таблица отображения MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство содержит уникальный идентификатор для элемента управления. Этот идентификатор должен содержать структуру [GUID](guid.md) и двоичное значение типа **Long**. Все элементы управления в диалоговом окне должны использовать один **GUID** для идентификации поставщика услуг, а каждый элемент управления должен использовать уникальное **длинное** значение, чтобы избежать конфликта элементов управления. 
  
Это свойство используется в уведомлениях. Например, уведомления, отправляемые в таблице отображения, должны задавать это свойство, чтобы уникальным образом определить обновляемый элемент управления. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

