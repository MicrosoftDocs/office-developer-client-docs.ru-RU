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
ms.openlocfilehash: ab2efebe91f871452b243150367b83a1d53f8a52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810804"
---
# <a name="pidtagaccount-canonical-property"></a>Каноническое свойство PidTagAccount

  
  
**Относится к**: Outlook 
  
Содержит имя учетной записи получателя. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W  <br/> |
|Идентификатор:  <br/> |0x3A00  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства предоставляют идентификации и доступа к сведениям для получателя. Они определены получателя и их организации.
  
Эти свойства обычно содержит имя электронной почты получателя, то есть, последний компонент адрес электронной почты, который уникальным образом идентифицирующее получателя в локальной организации. Имя электронной почты соответствует различающееся имя X.400, который должен быть краткое имя быть уникальным в рамках определенного домена обмена мгновенными сообщениями.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контакты и списки рассылки.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовков

mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[IMailUser : IMAPIProp](imailuserimapiprop.md)


[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

