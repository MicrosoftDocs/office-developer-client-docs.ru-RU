---
title: Каноническое свойство PidLidIsException
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsException
api_type:
- COM
ms.assetid: 802321fb-4261-4c3e-9de3-8b4f490dae13
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 18dfa8a5936902afe0272274f7a48d01b28f94f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315451"
---
# <a name="pidlidisexception-canonical-property"></a>Каноническое свойство PidLidIsException

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, что объект, представляющий исключение (включая потерянный экземпляр).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ЛИД_ИС_ЕКСЦЕПТИОН  <br/> |
|Набор свойств:  <br/> |Псетид_митинг  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x0000000A  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Замечания

Значение FALSE указывает, что объект, представляющий повторяющиеся ряды или один экземпляр. Отсутствие этого свойства для любого объекта указывает значение FALSE, за исключением внедренного сообщения Exception, для которого предполагается значение TRUE.
  
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

