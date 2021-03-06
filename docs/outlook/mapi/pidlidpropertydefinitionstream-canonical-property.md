---
title: Каноническое свойство PidLidPropertyDefinitionStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPropertyDefinitionStream
api_type:
- COM
ms.assetid: ead35049-e60e-4b46-bf12-f73d77cd36b2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b5ddb87111cfb0039cb1150338945615bbd5afc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315941"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a>Каноническое свойство PidLidPropertyDefinitionStream

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Представляет определения определенных пользователем полей и параметры привязки данных встроенных полей сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidPropDefStream  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008540  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Конфигурация времени запуска  <br/> |
   
## <a name="remarks"></a>Примечания

Значение свойства **PidLidPropertyDefinitionStream** сохранено в рамках настраиваемого определения формы для сообщения. 
  
Значение этого свойства — двоичный поток. Сведения о структуре этого потока см. в [разделе PropertyDefinition Stream Structure.](propertydefinition-stream-structure.md) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Outlook Элементы и поля](outlook-items-and-fields.md)
  
[Добавление определения для нового User-Defined поля](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Пример потока PropertyDefinition](propertydefinition-stream-sample.md)
  
[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

