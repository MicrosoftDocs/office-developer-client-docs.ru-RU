---
title: Каноническое свойство PidTagAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccount
api_type:
- HeaderDef
ms.assetid: bec199b5-abfd-4686-ad59-21092212e1a5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2962f973aa87b88f237ded69573df9ef312a7bc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359782"
---
# <a name="pidtagaccount-canonical-property"></a>Каноническое свойство PidTagAccount

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит имя учетной записи получателя. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W  <br/> |
|Идентификатор:  <br/> |0x3A00  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства предоставляют идентификацию и сведения о доступе для получателя. Они определяются получателем и организацией.
  
Эти свойства обычно содержат имя электронной почты получателя, то есть конечный компонент адреса электронной почты, который однозначно идентифицирует получателя в локальной организации. Имя электронной почты соответствует имени X.400, которое должно быть коротким именем, гарантированно уникальным в определенном домене обмена сообщениями.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для контактов и личных списков рассылки.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовки

mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[IMailUser : IMAPIProp](imailuserimapiprop.md)


[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

