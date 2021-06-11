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
ms.openlocfilehash: d6e189f78dec2fc92f1804be93e7885b61734b03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431423"
---
# <a name="pidtagidentitydisplay-canonical-property"></a>Каноническое свойство PidTagIdentityDisplay

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит имя отображения удостоверения поставщика услуг, определенное в системе обмена сообщениями. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W  <br/> |
|Идентификатор:  <br/> |0x3E00  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства отображаются не как свойства на любом объекте, а только как столбец в таблице состояния. Он является частью удостоверения поставщика услуг, обнажающего строку таблицы состояния. Удостоверение поставщика обычно ссылается на его учетную запись на сервере, но может ссылаться на любое представление, определенное поставщиком в системе обмена сообщениями. 
  
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

