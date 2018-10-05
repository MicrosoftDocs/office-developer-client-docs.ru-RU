---
title: Каноническое свойство PidTagAttachPayloadProviderGuidString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadProviderGuidString
api_type:
- HeaderDef
ms.assetid: c9d4b561-53b3-492b-9324-9376dd7abddf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5051784ea08316477f3c8888ada9170e3d99c2b5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389046"
---
# <a name="pidtagattachpayloadproviderguidstring-canonical-property"></a>Каноническое свойство PidTagAttachPayloadProviderGuidString

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение поля заголовка X MIME-полезной нагрузки-поставщика-Guid.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_PAYLOAD_PROV_GUID_STR, PR_ATTACH_PAYLOAD_PROV_GUID_STR_A, PR_ATTACH_PAYLOAD_PROV_GUID_STR_W  <br/> |
|Идентификатор:  <br/> |0x3719  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Приложения Outlook  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы задать значения этих свойств, клиенты MIME указывайте поле заголовка X--поставщика — код Guid полезных данных MIME лицо, которое будет анализироваться как вложение.
  
Читатели MIME, должен скопировать это значение поля заголовка на значение соответствующего свойства. Читатели MIME следует игнорировать это поле заголовка при его отображении в сущности MIME, анализируется как сообщение или текст сообщения, а не как вложение.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразование conventions стандартных электронной почты Интернета объекты сообщений.
    
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

