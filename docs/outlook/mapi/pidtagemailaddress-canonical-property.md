---
title: Каноническое свойство PidTagEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmailAddress
api_type:
- HeaderDef
ms.assetid: bbd1e187-172e-4612-9efe-7c8e52967dfe
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: efcb72d872836adce544f3a90cf093de1f3713a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338642"
---
# <a name="pidtagemailaddress-canonical-property"></a>Каноническое свойство PidTagEmailAddress

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит адрес электронной почты пользователя для обмена сообщениями. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W  <br/> |
|Идентификатор:  <br/> |0x3003  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Общие MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства являются примерами свойств базового адреса для всех пользователей обмена сообщениями. Это строка с нулью, формат которой имеет значение только для системы обмена сообщениями. 
  
Эти свойства используются в сочетании со свойствами **PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)и **PR_MESSAGE_CLASS** ([PidTagMessageClass)](pidtagmessageclass-canonical-property.md)в адресовке сообщений. Формат строки квалифиц **PR_ADDRTYPE.** 
  
Допустимые значения этого свойства: 
  
```cpp
network/postoffice/user 
Bruce@XYZZY.COM 
/c=US/a=att/p=Microsoft/o=Finance/ou=Purchasing/s=Furthur/g=Joe 
 
```

## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразуется из стандартных интернет-соглашений электронной почты в объекты сообщений.
    
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

