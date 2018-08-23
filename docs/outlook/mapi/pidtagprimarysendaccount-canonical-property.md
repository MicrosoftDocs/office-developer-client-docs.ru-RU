---
title: Каноническое свойство PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPrimarySendAccount
api_type:
- COM
ms.assetid: 2f268b3b-2e4c-4aea-8879-bdd0ac1df35c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a0f4ae75117dff3610175b785ab3f982cc7e7552
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590409"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a>Каноническое свойство PidTagPrimarySendAccount

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит строку с именем первого сервера, который используется для отправки сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PRIMARY_SEND_ACCOUNT  <br/> |
|Идентификатор:  <br/> |0x0E28  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Учетная запись  <br/> |
   
## <a name="remarks"></a>Замечания

Указывает первый сервер, который клиент должен использовать для отправки почты. Зависит от реализации имеет формат из этих свойств. Эти свойства можно использовать клиента, чтобы определить, какой сервер для направления почты через, но является необязательным, и значение не имеет значения для сервера.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

