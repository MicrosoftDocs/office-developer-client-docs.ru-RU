---
title: Каноническое свойство PidLidRecurrenceType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrenceType
api_type:
- COM
ms.assetid: 81ad2e8a-661f-4fc7-bee4-848db3285e31
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8f3c385c29589638bc314cc15635a12bb157d949
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568744"
---
# <a name="pidlidrecurrencetype-canonical-property"></a>Каноническое свойство PidLidRecurrenceType

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает тип повторения повторяющегося ряда.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidRecurType  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008231  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство определяет тип повторения повторяющегося ряда, используя один из перечисленных ниже значений.
  
|**Состояние**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|rectypeNone  <br/> |0  <br/> |Один экземпляр встречи.  <br/> |
|rectypeDaily  <br/> |1  <br/> |Ежедневный шаблон повторения.  <br/> |
|rectypeWeekly  <br/> |2  <br/> |Еженедельные шаблона повторения.  <br/> |
|rectypeMonthly  <br/> |3  <br/> |Месячная шаблона повторения.  <br/> |
|rectypeYearly  <br/> |4  <br/> |Ежегодный шаблон повторения.  <br/> |
   
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
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

