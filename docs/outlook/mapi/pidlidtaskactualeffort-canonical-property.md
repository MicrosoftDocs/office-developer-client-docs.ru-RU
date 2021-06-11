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
ms.openlocfilehash: 7eb51396f4575a8f8f9ce15aff84eb894773e979
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331173"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a>Каноническое свойство PidLidTaskActualEffort

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает количество минут, за которые пользователь выполнил задачу.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskActualEffort  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008110  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Примечания

Значение должно быть больше или равно 0 и менее 0x5AE980DF (1 525 252 319), где 480 минут равно одному дню и 2400 минут равно одной неделе (восемь часов в рабочий день и пять дней в неделю).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для объектов списка контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

