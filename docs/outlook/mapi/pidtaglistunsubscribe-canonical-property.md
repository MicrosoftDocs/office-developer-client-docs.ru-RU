---
title: Каноническое свойство PidTagListUnsubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListUnsubscribe
api_type:
- HeaderDef
ms.assetid: 4e6bfbc7-7586-43cc-9380-daa0fe3d85a5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1a4011a22f1029cc4002d4506eb4d335bd280bec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593440"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a>Каноническое свойство PidTagListUnsubscribe

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит значение в поле Заголовок списка отписаться сообщение Multipurpose Internet Mail Extensions (MIME).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W  <br/> |
|Идентификатор:  <br/> |0x1045  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Замечания

Для создания списка отписаться поле заголовка, клиенты необходимо задать эти свойства нужное значение. Записи MIME необходимо скопировать значения этих свойств поля заголовка отписаться списка.
  
Чтобы задать значение эти свойства списка, связанные с сервера, клиенты MIME необходимо создать поля заголовка, как указано в следующей таблице.
  
|**Свойство**|**Имя поля Предпочитаемый заголовка**|**Альтернативные заголовок поля имя**|
|:-----|:-----|:-----|
|**PR_LIST_UNSUBSCRIBE** <br/> |Список отписаться  <br/> |X список отписаться  <br/> |
   
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

