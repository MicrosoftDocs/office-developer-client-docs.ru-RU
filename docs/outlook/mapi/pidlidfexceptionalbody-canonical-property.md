---
title: Каноническое свойство PidLidFExceptionalBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalBody
api_type:
- COM
ms.assetid: 327516e8-ed3f-40fc-9604-03a70aecef5a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 93eb98aee19ea3f46a4e01e2c80150c3efe893a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327463"
---
# <a name="pidlidfexceptionalbody-canonical-property"></a>Каноническое свойство PidLidFExceptionalBody

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, что объект встроенного сообщения исключения имеет тело, отличащееся от повторяющегося объекта календаря.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidFExceptionalBody  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008206  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Собрания  <br/> |
   
## <a name="remarks"></a>Примечания

Если значение этого свойства true, то объект встроенного сообщения исключения должен иметь тело. Если значение этого свойства false или если свойство не существует, клиент или сервер должны получить тело из повторяющегося объекта календаря.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

