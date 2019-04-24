---
title: Каноническое свойство PidLidResponseStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8c8e284752c6fd47eb7a8f227e2dbfeceebea596
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345761"
---
# <a name="pidlidresponsestatus-canonical-property"></a>Каноническое свойство PidLidResponseStatus

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает состояние отклика участника.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидреспонсестатус  <br/> |
|Набор свойств:  <br/> |Псетид_аппоинтмент  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008218  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Комментарии

Состояние отклика должно быть одним из значений в приведенной ниже таблице.
  
|**Состояние ответа**|**Value**|**Описание**|
|:-----|:-----|:-----|
|Респноне  <br/> |0x00000000  <br/> |Для этого объекта ответ не нужен. Это относится к объектам встреч и объектам ответа на собрания.  <br/> |
|Респорганизед  <br/> |0x00000001  <br/> |Это собрание принадлежит организатору.  <br/> |
|Респтентативе  <br/> |0x00000002  <br/> |Это значение на собрании участника указывает на то, что участник принял приглашение на собрание под вопросом.  <br/> |
|Респакцептед  <br/> |0x00000003  <br/> |Это значение на совещании "т" пользователя указывает на то, что участник принял приглашение на собрание.  <br/> |
|Респдеклинед  <br/> |0x00000004  <br/> |Это значение на собрании участника указывает на то, что участник отклонил приглашение на собрание.  <br/> |
|Респнотреспондед  <br/> |0x00000005  <br/> |Это значение на собрании участника указывает на то, что участника еще не ответил. Это значение находится в приглашении на собрание, обновлении собрания и отмене собрания.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

