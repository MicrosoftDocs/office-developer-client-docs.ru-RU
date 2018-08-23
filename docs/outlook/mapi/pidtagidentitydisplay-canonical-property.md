---
title: Каноническое свойство PidTagIdentityDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityDisplay
api_type:
- HeaderDef
ms.assetid: ad9756c1-c1f9-4ab3-a58a-31e574dd9530
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6cfc4d6eab5b2f19bcfd4c7e2a8fc9fa1494afa4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585579"
---
# <a name="pidtagidentitydisplay-canonical-property"></a>Каноническое свойство PidTagIdentityDisplay

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит отображаемое имя для поставщика услуг удостоверения, как определено в системе обмена сообщениями. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W  <br/> |
|Идентификатор:  <br/> |0x3E00  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства не отображаются как свойства любого объекта, но только в виде столбцов в таблице состояния. Он является частью идентификатор поставщика услуг, предоставление в строке состояния в таблице. Поставщик удостоверений обычно относится к его учетной записи на сервере, но можно ссылаться на любое представление, которое определяет поставщик в системе обмена сообщениями. 
  
Поставщик службы передачи Свойства identity должны предоставлять все из них. Поставщики, относящихся к одной службы сообщения должны предоставлять те же значения для свойства identity. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

