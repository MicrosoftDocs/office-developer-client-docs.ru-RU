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
ms.openlocfilehash: 12226039457782162eb74a19713fa77936332f80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565146"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a>Каноническое свойство PidTagIdentitySearchKey

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит ключ поиска для поставщика услуг удостоверения, как определено в системе обмена сообщениями. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_IDENTITY_SEARCH_KEY  <br/> |
|Идентификатор:  <br/> |0x3E05  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство не отображается как свойство для любого объекта, но только в виде столбцов в таблице состояния. Он является частью идентификатор поставщика услуг, предоставление в строке состояния в таблице. Поставщик удостоверений обычно относится к его учетной записи на сервере, но можно ссылаться на любое представление, которое определяет поставщик в системе обмена сообщениями. 
  
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

