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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382584"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a>Каноническое свойство PidLidTaskActualEffort

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
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

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов списка рассылки и контактов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

