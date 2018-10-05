---
title: Каноническое свойство PidTagPostalCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPostalCode
api_type:
- COM
ms.assetid: dd8e04b3-8959-4df4-ba2c-f6371180929b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 67be9232d7e80dbbabe93fbe408b3d3fc8b832ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389072"
---
# <a name="pidtagpostalcode-canonical-property"></a>Каноническое свойство PidTagPostalCode

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит почтовый индекс для почтового адреса получателя.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_POSTAL_CODE, PR_POSTAL_CODE_A, PR_POSTAL_CODE_W, PR_BUSINESS_ADDRESS_POSTAL_CODE, PR_BUSINESS_ADDRESS_POSTAL_CODE_A, PR_BUSINESS_ADDRESS_POSTAL_CODE_W  <br/> |
|Идентификатор:  <br/> |0x3A2A  <br/> |
|Тип данных:  <br/> |PT_UNICODE PT_STRING8  <br/> |
|Область:  <br/> |Пользователь почты MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства предоставляют идентификации и доступа к сведениям для получателя. Они определены получателя и их организации. 
  
Почтовый индекс для получателя страны или региона. В Соединенных Штатах Америки это свойство содержит ПОЧТОВЫЙ индекс.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контакты и списки рассылки.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

