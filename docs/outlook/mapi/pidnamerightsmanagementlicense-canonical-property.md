---
title: Каноническое свойство PidNameRightsManagementLicense
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameRightsManagementLicense
api_type:
- COM
ms.assetid: ca3c9317-7873-4f37-b78f-b35467c81c29
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 889b823a55c39ebc19e52c8cc9a1d078a5732a01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315024"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a>Каноническое свойство PidNameRightsManagementLicense

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Кэшрует лицензию на использование сообщения электронной почты, управляемого правами.
  
|||
|:-----|:-----|
|Дружелюбные имена:  <br/> |Нет  <br/> |
|Набор свойств:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Имя свойства:  <br/> |DRMLicense  <br/> |
|Тип данных:  <br/> |PT_MV_BINARY  <br/> |
|Область:  <br/> |Безопасный обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Примечания

Если свойство присутствует в сообщении электронной почты, управляемом правами, первое значение этого нескольких двоичных свойств должно содержать лицензию на сжатие ZLIB (как указано в [RFC1950]) для сообщения электронной почты, управляемого правами.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Указывает свойства сообщений в кодированной кодировки с управлением правами.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

