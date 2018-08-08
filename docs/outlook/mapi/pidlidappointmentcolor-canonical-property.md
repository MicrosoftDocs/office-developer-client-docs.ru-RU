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
ms.openlocfilehash: 251377a7b9118437aff3fbb6b2b9376cbf70375c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810094"
---
# <a name="pidlidappointmentcolor-canonical-property"></a>Каноническое свойство PidLidAppointmentColor

  
  
**Относится к**: Outlook 
  
Определяет цвет, используемый при отображении в календаре.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidApptColor  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008214  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство определяет цвет, используемый при отображении в календаре. Клиент или сервер следует установить это значение для обеспечения обратной совместимости с клиентами, возраст которых. Вместо этого он может отображать календаря на основе значения свойства **ключевые слова** ([PidNameKeywords](pidnamekeywords-canonical-property.md)), как указано в [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx). Если задано значение должно быть одно из следующих действий.
  
|**Значение**|**Цвет**|
|:-----|:-----|
|0x00000000  <br/> |Нет  <br/> |
|0x00000001  <br/> |Красный  <br/> |
|0x00000002  <br/> |Синий  <br/> |
|0x00000003  <br/> |Зеленый  <br/> |
|0x00000004  <br/> |Серый цвет  <br/> |
|0x00000005  <br/> |Оранжевый  <br/> |
|0x00000006  <br/> |Голубой  <br/> |
|0x00000007  <br/> |Оливковый  <br/> |
|0x00000008  <br/> |Сиреневый  <br/> |
|0x00000009  <br/> |Сине-зеленый  <br/> |
|0x0000000A  <br/> |Желтый  <br/> |
   
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

