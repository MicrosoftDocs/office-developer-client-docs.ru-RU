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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит отображаемое имя для удостоверения поставщика услуг в соответствии с определением в системе обмена сообщениями. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ИДЕНТИТИ_ДИСПЛАЙ, ПР_ИДЕНТИТИ_ДИСПЛАЙ_А, ПР_ИДЕНТИТИ_ДИСПЛАЙ_В  <br/> |
|Идентификатор:  <br/> |0x3E00  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства не отображаются как свойства ни в одном объекте, но только в виде столбца в таблице состояния. Он является частью удостоверения поставщика услуг, предоставляющего строку таблицы состояния. Удостоверение поставщика обычно относится к его учетной записи на сервере, но может ссылаться на любое представление, которое определяет поставщик в системе обмена сообщениями. 
  
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

