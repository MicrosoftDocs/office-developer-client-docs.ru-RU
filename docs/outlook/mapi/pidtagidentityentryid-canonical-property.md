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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор входа для удостоверения поставщика услуг, определенный в системе обмена сообщениями. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_IDENTITY_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x3E01  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство не появляется как свойство на любом объекте, а только как столбец в таблице состояния. Он является частью удостоверения поставщика услуг, обнажающего строку таблицы состояния. Удостоверение поставщика обычно ссылается на его учетную запись на сервере, но может ссылаться на любое представление, определенное поставщиком в системе обмена сообщениями. 
  
Этот реквизит обычно заданной для соответствующего идентификатора записи адресной книги. 
  
Поставщик услуг, обставленный любыми свойствами удостоверений, должен предоставить все из них. Поставщики, принадлежащие к одной и той же службе сообщений, должны выставлять те же значения для свойств удостоверений. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

