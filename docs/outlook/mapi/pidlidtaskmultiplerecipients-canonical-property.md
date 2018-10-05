---
title: Каноническое свойство PidLidTaskMultipleRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMultipleRecipients
api_type:
- COM
ms.assetid: 28ba9997-72dd-465f-94a7-35a317a361ef
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3b260917e107086dee6176f73b6c82c3a1825327
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391173"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a>Каноническое свойство PidLidTaskMultipleRecipients

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Рекомендации по оптимизации о получателей задачи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskMultRecips  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008120  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Замечания

Если задано, это свойство должно быть присвоено побитовую операцию **или** ноль или более из следующих значений. 
  
|**Имя**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|Sent  <br/> |0x00000001  <br/> |Задача имеет несколько получателей.  <br/> |
|Получено  <br/> |0x00000002  <br/> |Несмотря на то, что подсказка отправлено не задан, клиент обнаружил, что задачи несколько получателей.  <br/> |
|Резерв  <br/> |0x00000004  <br/> |Это значение зарезервировано.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Определяет несколько объектов, которые модель электронный эквивалент задач, назначений задач и обновления задач.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

