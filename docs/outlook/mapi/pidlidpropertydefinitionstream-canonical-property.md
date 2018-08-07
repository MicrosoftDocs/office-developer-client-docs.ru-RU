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
ms.openlocfilehash: f7f764d95c2fc36ba6af617333cb47d266cd2aa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810469"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a>Каноническое свойство PidLidPropertyDefinitionStream

  
  
**Относится к**: Outlook 
  
Представляет параметры привязки данных встроенных полей сообщения и определения пользовательских полей.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidPropDefStream  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008540  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Конфигурация во время выполнения  <br/> |
   
## <a name="remarks"></a>Замечания

Значение свойства **PidLidPropertyDefinitionStream** сохраняется как часть определения настраиваемую форму в качестве сообщения. 
  
Значение этого свойства — это двоичный поток. Сведения о структуре этого потока Просмотр [Структуры потока определение свойства](propertydefinition-stream-structure.md). 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Поля и элементы Outlook](outlook-items-and-fields.md)
  
[Добавление определения для нового пользовательского поля](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Пример потока PropertyDefinition](propertydefinition-stream-sample.md)
  
[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

