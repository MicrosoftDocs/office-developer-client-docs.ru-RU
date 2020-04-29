---
title: Каноническое свойство PidLidAppointmentColor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentColor
api_type:
- COM
ms.assetid: 91147e85-f440-4463-850b-efc9bdbd36d1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1ea0830a06f303da8243f927e4a07cc744951ca9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345439"
---
# <a name="pidlidappointmentcolor-canonical-property"></a>Каноническое свойство PidLidAppointmentColor

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает цвет, используемый при отображении календаря.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |диспидапптколор  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008214  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство указывает цвет, используемый при отображении календаря. Клиент или сервер должен установить это значение для обратной совместимости со старыми клиентами. Вместо этого он может отображать календарь на основе значения свойства **keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)), как указано в [[MS-окскмсг]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx). Если задано значение, значение должно быть одним из следующих.
  
|**Значение**|**Color**|
|:-----|:-----|
|0x00000000  <br/> |Нет  <br/> |
|0x00000001  <br/> |Красный  <br/> |
|0x00000002  <br/> |Синий  <br/> |
|0x00000003  <br/> |Зеленый  <br/> |
|0x00000004  <br/> |Серы  <br/> |
|0x00000005  <br/> |Апельсин  <br/> |
|0x00000006  <br/> |Cyan  <br/> |
|0x00000007  <br/> |Оливковый  <br/> |
|0x00000008  <br/> |Сиреневый  <br/> |
|0x00000009  <br/> |Сине-зеленая  <br/> |
|0x0000000A  <br/> |Желтый  <br/> |
   
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

