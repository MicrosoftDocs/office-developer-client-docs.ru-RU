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
ms.openlocfilehash: d2b00c67984d090274a17028ee74e46bee482e2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331579"
---
# <a name="pidlidmeetingtype-canonical-property"></a>Каноническое свойство PidLidMeetingType

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает тип приглашения на собрание или обновления собрания.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидмитингтипе  <br/> |
|Набор свойств:  <br/> |Псетид_митинг  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00000026  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Комментарии

Значение этого свойства должно быть равно одному из следующих значений:
  
|**Свойство**|**Value**|**Описание**|
|:-----|:-----|:-----|
|Мтжемпти  <br/> |0x00000000  <br/> |Неопределенные.  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |Начальное приглашение на собрание.  <br/> |
|Мтгфулл  <br/> |0x00010000  <br/> |Полное обновление.  <br/> |
|Мтгинфо  <br/> |0x00020000  <br/> |Информационное обновление.  <br/> |
|Мтгаутофдате  <br/> |0x00080000  <br/> |Новое приглашение на собрание или обновление собрания было получено после этого.  <br/> |
|Мтгделегаторкопи  <br/> |0x00100000  <br/> |Это значение устанавливается для копии представителя, когда представитель обрабатывает объекты, связанные с собранием.  <br/> |
   
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

