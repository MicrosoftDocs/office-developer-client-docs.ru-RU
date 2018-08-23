---
title: Каноническое свойство PidTagIdentityEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityEntryId
api_type:
- HeaderDef
ms.assetid: 61a9d403-e0e5-45c3-8d18-4d53207ab927
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a8810b6c39b909ebaa612496824150499cd15165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584844"
---
# <a name="pidtagidentityentryid-canonical-property"></a>Каноническое свойство PidTagIdentityEntryId

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи для поставщика услуг удостоверения, как определено в системе обмена сообщениями. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_IDENTITY_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x3E01  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство не отображается как свойство для любого объекта, но только в виде столбцов в таблице состояния. Он является частью идентификатор поставщика услуг, предоставление в строке состояния в таблице. Поставщик удостоверений обычно относится к его учетной записи на сервере, но можно ссылаться на любое представление, которое определяет поставщик в системе обмена сообщениями. 
  
В этом proprerty обычно имеет значение идентификатор записи соответствующие адресной книги. 
  
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

