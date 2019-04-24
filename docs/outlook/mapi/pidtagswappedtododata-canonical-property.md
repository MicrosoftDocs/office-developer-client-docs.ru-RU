---
title: Каноническое свойство PidTagSwappedToDoData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3ecfa1e89688ae525a28e221424fb4a8194fc217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359138"
---
# <a name="pidtagswappedtododata-canonical-property"></a>Каноническое свойство PidTagSwappedToDoData

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поддерживает второй набор значений свойств, которые не влияют на состояние объекта Message.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_СВАППЕД_ТОДО_ДАТА  <br/> |
|Идентификатор:  <br/> |0x0E2D  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Несъемный MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Действует как дополнительный флаг расположение хранилища, если поддерживаются флаги отправителя или отправители отправителя, эта структура предоставляет расположение, в котором хранятся все свойства, связанные с протоколом отМеток, которые поддерживаются в отметках отправителя и все свойства, связанные с протоколом настройки напоминаний, которые поддерживаются в памятках отправителя без предоставления флага отправителя или напоминания о отправителю получателям сообщения.
  
Аналогично, эта структура предоставляет расположение, в котором хранятся все свойства, относящиеся к протоколу поМеток, которые поддерживаются в флагах получателей и свойствах, связанных с протоколом настройки напоминаний, которые поддерживаются в получателе. напоминания о ранее отправленном сообщении.
  
Дополнительные сведения об этом свойстве см. в разделе [[MS — оксофлаг]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Задает свойства и операции, связанные с пометкой.
    
[[MS — ОКСОРМДР]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Задает свойства и модель взаимодействия для сообщений электронной почты и других объектов.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

