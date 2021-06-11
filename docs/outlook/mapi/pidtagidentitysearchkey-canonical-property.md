---
title: Каноническое свойство PidTagIdentitySearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentitySearchKey
api_type:
- HeaderDef
ms.assetid: 5fe55ba7-4ecd-4a43-ab5b-2ef595c2cdd9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5f5f5eaa41d6256bed69b2cd9a91208181d5bda1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423750"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a>Каноническое свойство PidTagIdentitySearchKey

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит ключ поиска для удостоверения поставщика услуг, определенный в системе обмена сообщениями. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_IDENTITY_SEARCH_KEY  <br/> |
|Идентификатор:  <br/> |0x3E05  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство не появляется как свойство на любом объекте, а только как столбец в таблице состояния. Он является частью удостоверения поставщика услуг, обнажающего строку таблицы состояния. Удостоверение поставщика обычно ссылается на его учетную запись на сервере, но может ссылаться на любое представление, определенное поставщиком в системе обмена сообщениями. 
  
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

