---
title: Каноническое свойство PidTagListSubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bee11c495d7f1ef21f9af70e6aa89f8c0d0f78b4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389605"
---
# <a name="pidtaglistsubscribe-canonical-property"></a>Каноническое свойство PidTagListSubscribe

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение в поле Заголовок списка подписка сообщение Multipurpose Internet Mail Extensions (MIME).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W  <br/> |
|Идентификатор:  <br/> |0x1044  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Замечания

Для создания поля заголовка подписка списка клиентов необходимо установить значение этих свойств нужное значение. Записи MIME необходимо скопировать значения этих свойств поля заголовка подписка списка.
  
Чтобы задать значение свойства, связанные с сервера эти клиенты MIME необходимо создать поля заголовка, как указано в следующей таблице.
  
|**Свойство**|**Имя поля Предпочитаемый заголовка**|**Альтернативные заголовок поля имя**|
|:-----|:-----|:-----|
|**PidTagListSubscribe** <br/> |Подписка списка  <br/> |X список подписки  <br/> |
   
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

