---
title: Каноническое свойство PidLidTaskActualEffort
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskActualEffort
api_type:
- COM
ms.assetid: 8e9a9432-bf50-4333-82ec-fba19dff8006
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0782191010341019ebea71ebf545dec490521520
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810556"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a>Каноническое свойство PidLidTaskActualEffort

  
  
**Относится к**: Outlook 
  
Указывает, что пользователь выполнять задачи в минутах.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskActualEffort  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008110  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Замечания

Значение должно быть больше или равно 0 и меньше, чем 0x5AE980DF (1,525,252,319), где 480 минут равно один день и 2400 минут равно 1 неделя (8 часов рабочего дня и пять дней в неделе).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов списка рассылки и контактов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

