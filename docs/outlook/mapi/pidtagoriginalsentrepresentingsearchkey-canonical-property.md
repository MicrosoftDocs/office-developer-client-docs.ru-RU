---
title: Каноническое свойство PidTagOriginalSentRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 0fb1b803-f8b4-4d6d-8e2a-836daa98ac63
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ee23e2f25370a253b914779b3bfd0ab82fd08c7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340980"
---
# <a name="pidtagoriginalsentrepresentingsearchkey-canonical-property"></a>Каноническое свойство PidTagOriginalSentRepresentingSearchKey

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит ключ поиска пользователя обмена сообщениями, от имени которого было отправлено исходное сообщение.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY  <br/> |
|Идентификатор:  <br/> |0x005F  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является одним из свойств адреса исходного представленного отправитель сообщения. Он используется в цепочке беседы.
  
Клиентские приложения, отправляющие сообщение от имени другого клиента, должны установить для этого свойства значение **свойства PR_SENT_REPRESENTING_SEARCH_KEY** [(PidTagSentRepresentingSearchKey)](pidtagsentrepresentingsearchkey-canonical-property.md)при первой отправке сообщения. После этого его не следует менять.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для объектов сообщений электронной почты.
    
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

