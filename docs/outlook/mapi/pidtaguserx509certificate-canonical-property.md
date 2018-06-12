---
title: Каноническое свойство PidTagUserX509Certificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserX509Certificate
api_type:
- COM
ms.assetid: 278bb9e4-3ff6-4bef-b208-7924f7a5e9b1
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: d27ef47a3ba387ae2e7acbcefc75b07ddd794e80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812042"
---
# <a name="pidtaguserx509certificate-canonical-property"></a>Каноническое свойство PidTagUserX509Certificate

  
  
**Применимо к**: Outlook 
  
Содержит сертификаты безопасности X.509 версии 3 для обмена сообщениями пользователя. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_USER_X509_CERTIFICATE  <br/> |
|Идентификатор:  <br/> |0x3A70  <br/> |
|Тип данных:  <br/> |PT_MV_BINARY  <br/> |
|Области:  <br/> |Пользователь почты MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство используется приложений, использующих безопасности открытого ключа. Он содержит двоичное представление одного или нескольких X.509 версии 3 безопасности сертификатов. 
  
Это свойство можно использовать различные приложения и клиентов для свои собственные сертификаты безопасности. Двоичный формат данных X.509 может зависеть от поставщиков. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Каноническое свойство имена сопоставляемых именам MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI имена каноническое свойств](mapping-mapi-names-to-canonical-property-names.md)

