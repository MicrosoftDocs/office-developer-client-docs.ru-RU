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
ms.openlocfilehash: 099df2211e87e253ab1be520378b3a2b2ca7d4c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423337"
---
# <a name="pidtagidentityentryid-canonical-property"></a>Каноническое свойство PidTagIdentityEntryId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор элемента для удостоверения поставщика услуг в соответствии с определением в системе обмена сообщениями. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ИДЕНТИТИ_ЕНТРИД  <br/> |
|Идентификатор:  <br/> |0x3E01  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство не отображается как свойство ни для одного объекта, но только как столбец в таблице "состояние". Он является частью удостоверения поставщика услуг, предоставляющего строку таблицы состояния. Удостоверение поставщика обычно относится к его учетной записи на сервере, но может ссылаться на любое представление, которое определяет поставщик в системе обмена сообщениями. 
  
Для этого пропрерти обычно задается соответствующий идентификатор записи адресной книги. 
  
Поставщик услуг, представляя любое из свойств Identity, должен отказаться от всех этих свойств. Поставщики одной и той же службы сообщений должны предоставлять одни и те же значения для свойств Identity. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

