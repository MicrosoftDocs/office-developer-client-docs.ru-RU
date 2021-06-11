---
title: Каноническое свойство PidTagPostOfficeBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPostOfficeBox
api_type:
- COM
ms.assetid: 3c2968bb-9625-4ebe-a8a0-cce8ef1651f4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c56d6d1301f15596eeda8dd5361a236226431b06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344403"
---
# <a name="pidtagpostofficebox-canonical-property"></a>Каноническое свойство PidTagPostOfficeBox

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит номер или идентификатор почтового ящика получателя.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_POST_OFFICE_BOX, PR_POST_OFFICE_BOX_A, PR_POST_OFFICE_BOX_W, PR_BUSINESS_ADDRESS_POST_OFFICE_BOX, PR_BUSINESS_ADDRESS_POST_OFFICE_BOX_A, PR_BUSINESS_ADDRESS_POST_OFFICE_BOX_W  <br/> |
|Идентификатор:  <br/> |0x3A2B  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Пользователь почты MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства предоставляют идентификацию и сведения о доступе для получателя. Они определяются получателем и организацией. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для контактов и личных списков рассылки.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

