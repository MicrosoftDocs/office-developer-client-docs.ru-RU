---
title: Каноническое свойство PidLidMeetingType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ebc7ed4563040e16c71e1df1094667f87a4c09b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572370"
---
# <a name="pidlidmeetingtype-canonical-property"></a>Каноническое свойство PidLidMeetingType

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает тип приглашения на собрание или приглашения обновления.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidMeetingType  <br/> |
|Набор свойств:  <br/> |PSETID_Meeting  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00000026  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Meetings (собрания);  <br/> |
   
## <a name="remarks"></a>Замечания

Значение этого свойства необходимо присвоить одно из следующих:
  
|**Свойство**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|mtgEmpty  <br/> |0x00000000  <br/> |Не определено.  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |Начальное собрание.  <br/> |
|mtgFull  <br/> |0x00010000  <br/> |Полное обновление.  <br/> |
|mtgInfo  <br/> |0x00020000  <br/> |Информационные обновления.  <br/> |
|mtgOutOfDate  <br/> |0x00080000  <br/> |Файлы более новых приглашения на собрание или обновление собрания было получено после этой команды.  <br/> |
|mtgDelegatorCopy  <br/> |0x00100000  <br/> |Это значение на копии сотрудника при объекты собрании значками делегат.  <br/> |
   
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

