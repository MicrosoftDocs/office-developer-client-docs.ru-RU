---
title: Каноническое свойство PidTagDeferredSendUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendUnits
api_type:
- HeaderDef
ms.assetid: 2386be9f-18c9-4949-a2aa-efc8e212801c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: becc076efe0f4f805eb2a8db071b70ad731ee256
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359908"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a>Каноническое свойство PidTagDeferredSendUnits

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает единицу времени, на которое должно умножаться значение свойства **PR_DEFERRED_SEND_NUMBER** [(PidTagDeferredSendNumber).](pidtagdeferredsendnumber-canonical-property.md)
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DEFERRED_SEND_UNITS  <br/> |
|Идентификатор:  <br/> |0x3FEC  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Если за установлено, это свойство должно иметь одно из следующих значений:
  
|||
|:-----|:-----|
|**PidTagDeferredSendUnits** <br/> |Описание  <br/> |
|0  <br/> |Минуты, например 60 секунд  <br/> |
|1   <br/> |Часы, например 60x60 секунд  <br/> |
|2   <br/> |День, например 24x60x60 секунд  <br/> |
|3   <br/> |Неделя, например 7x24x60x60 секунд  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

