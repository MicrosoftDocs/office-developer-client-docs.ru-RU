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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 0bfa3a01613c49b122e92e4ac281e5b20b5f07ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810516"
---
# <a name="pidlidresponsestatus-canonical-property"></a>Каноническое свойство PidLidResponseStatus

  
  
**Применимо к**: Outlook 
  
Указывает состояние ответа для участника.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidResponseStatus  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008218  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Области:  <br/> |Meetings (собрания);  <br/> |
   
## <a name="remarks"></a>Замечания

Состояние ответа должно быть одно из значений в таблице ниже.
  
|**Состояние ответа**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |Нет ответа необходим для этого объекта. Это обоснование для объектов встречи и собрания объекты ответа.  <br/> |
|respOrganized  <br/> |0x00000001  <br/> |Приглашение на собрание принадлежит организатора.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Это значение на участника собрания указывает, что участник условно принял приглашение на собрание.  <br/> |
|respAccepted  <br/> |0x00000003  <br/> |Это значение на участника собрания t указывает, что участник принял запрос на собрание.  <br/> |
|respDeclined  <br/> |0x00000004  <br/> |Это значение на участника собрания указывает, что участник отклонил запрос на собрание.  <br/> |
|respNotResponded  <br/> |0x00000005  <br/> |Это значение на участника собрания указывает, что участник собрания еще не ответил. Это значение — на приглашения на собрание, обновление собрания и Отмена собрания.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Каноническое свойство имена сопоставляемых именам MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI имена каноническое свойств](mapping-mapi-names-to-canonical-property-names.md)

