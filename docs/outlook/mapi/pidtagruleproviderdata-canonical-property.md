---
title: Каноническое свойство PidTagRuleProviderData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProviderData
api_type:
- COM
ms.assetid: b04a277c-b483-4f54-b360-311034b9a7ee
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e4d209c4f185ff253476beb04913e6a64884f9b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335422"
---
# <a name="pidtagruleproviderdata-canonical-property"></a>Каноническое свойство PidTagRuleProviderData

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Непрозрачной свойство, которое клиент задает для исключительного использования клиента. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RULE_PROVIDER_DATA  <br/> |
|Идентификатор:  <br/> |0x6684  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Правила стороне сервера  <br/> |
   
## <a name="remarks"></a>Примечания

Сервер должен сохранить значение этого свойства, если оно было заданной клиентом, но при оценке и обработке правил должно игнорировать его содержимое.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Манипулирует входящие сообщения электронной почты на сервере.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств. 
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagRuleProvider](pidtagruleprovider-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

