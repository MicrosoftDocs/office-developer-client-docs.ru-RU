---
title: Каноническое свойство PidTagOriginalSensitivity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSensitivity
api_type:
- COM
ms.assetid: 70a87cf8-2011-4669-90fd-2711c3352e30
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6d461c88e96a3f749595b3e071737107480472aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811476"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a>Каноническое свойство PidTagOriginalSensitivity

  
  
**Относится к**: Outlook 
  
Со значением, назначенные отправителем первая версия сообщение содержит то есть сообщение перед пересылку и ответ.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_SENSITIVITY  <br/> |
|Идентификатор:  <br/> |0x002E  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Клиентское приложение следует этому свойству присвоено значение такое же значение как свойство **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) при первом сообщения. Оно должно быть задано впоследствии.
  
Это свойство используется поставщик транспорта для защиты конфиденциальности на скопированной записи. Включение его, например, для блокировки изменения исходного текста сообщения в прямого из или в ответ на сообщение, которое изначально помечено **SENSITIVITY_PRIVATE**.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)
