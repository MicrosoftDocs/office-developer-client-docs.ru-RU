---
title: Каноническое свойство PidTagInternetReferences
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReferences
api_type:
- HeaderDef
ms.assetid: 645fe61d-414a-455e-b034-db3cfd003b9d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4558fcdba11aed92eb21972ed62320209ade77ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811262"
---
# <a name="pidtaginternetreferences-canonical-property"></a>Каноническое свойство PidTagInternetReferences

  
  
**Относится к**: Outlook 
  
Содержит значение поля заголовка сообщения Multipurpose Internet Mail Extensions (MIME) ссылки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W  <br/> |
|Идентификатор:  <br/> |0x1039  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Замечания

Для создания ссылки на поля заголовка, клиенты необходимо задать эти свойства нужное значение. Записи MIME необходимо скопировать значения этих свойств поля заголовка ссылки.
  
Для установки значения этих свойств, клиенты MIME должен записи нужное значение в поле Заголовок справочные материалы. Читатели MIME, должен скопировать значение поля заголовка ссылки на эти свойства. Читатели MIME усекать значение эти свойства, если оно превышает 64 КБ в длину.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
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

