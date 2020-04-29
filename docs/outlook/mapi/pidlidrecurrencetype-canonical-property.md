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
ms.openlocfilehash: 7a0ea0dfe236341815fe94fb570908d7034fc83e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315913"
---
# <a name="pidlidrecurrencetype-canonical-property"></a>Каноническое свойство PidLidRecurrenceType

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает тип повторяющегося ряда.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |диспидрекуртипе  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008231  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство указывает тип повторения повторяющейся серии с помощью одного из указанных ниже значений.
  
|**Состояние**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|ректипеноне  <br/> |нуль  <br/> |Встреча с одним экземпляром.  <br/> |
|ректипедаили  <br/> |1,1  <br/> |Ежедневный шаблон повторения.  <br/> |
|ректипевикли  <br/> |2  <br/> |Еженедельный шаблон повторения.  <br/> |
|ректипемонсли  <br/> |4  <br/> |Месячный шаблон повторения.  <br/> |
|ректипэйеарли  <br/> |4   <br/> |Шаблон ежегодного повторения.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

