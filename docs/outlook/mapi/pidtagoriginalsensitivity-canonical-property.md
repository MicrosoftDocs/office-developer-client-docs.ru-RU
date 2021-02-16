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
ms.openlocfilehash: e712a4cc49541ee4330f479d7a03af323bdbc887
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341232"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a>Каноническое свойство PidTagOriginalSensitivity

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение конфиденциальности, назначенное отправителю первой версии сообщения, то есть сообщение перед переадаемой или ответом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_SENSITIVITY  <br/> |
|Идентификатор:  <br/> |0x002E  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Клиентские приложения должны установить для этого свойства то же **значение,** что и свойство PR_SENSITIVITY ([PidTagSensitivity)](pidtagsensitivity-canonical-property.md)при первой отправке сообщения. В дальнейшем его не следует менять.
  
Это свойство используется поставщиком транспорта для защиты конфиденциальности скопированные записи. Это позволяет, например, блокировать изменение исходного текста сообщения в виде переададновения или ответа на сообщение, которое изначально было помечено SENSITIVITY_PRIVATE **.**
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для объектов сообщений электронной почты.
    
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

