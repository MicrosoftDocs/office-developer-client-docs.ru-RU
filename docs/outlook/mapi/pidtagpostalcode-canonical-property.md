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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338523"
---
# <a name="pidtagpostalcode-canonical-property"></a>Каноническое свойство PidTagPostalCode

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит почтовый код для почтового адреса получателя.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_POSTAL_CODE, PR_POSTAL_CODE_A, PR_POSTAL_CODE_W, PR_BUSINESS_ADDRESS_POSTAL_CODE, PR_BUSINESS_ADDRESS_POSTAL_CODE_A, PR_BUSINESS_ADDRESS_POSTAL_CODE_W  <br/> |
|Идентификатор:  <br/> |0x3A2A  <br/> |
|Тип данных:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Область:  <br/> |Пользователь почты MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства предоставляют сведения для идентификации и доступа получателя. Они определяются получателем и его организацией. 
  
Почтовый код является специфическим для страны или региона получателя. В США это свойство содержит ZIP-код.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

