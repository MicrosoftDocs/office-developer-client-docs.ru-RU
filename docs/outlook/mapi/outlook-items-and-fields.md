---
title: Outlook Элементы и поля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b40752d4a5f445368752ad4caf5c919f6e0ce27b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409120"
---
# <a name="outlook-items-and-fields"></a>Outlook Элементы и поля

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook предоставляет типы элементов, которые специализируются на их функциональности (например, почтовые элементы, встречи, контакты, задачи и заметки). Outlook стандартные поля для каждого типа элемента, обычно именуемого встроенными полями. Outlook также позволяет пользователям создавать настраиваемые поля, которые обычно называются пользовательскими полями. Каждое поле связано с типом данных и значением. Примерами типов данных являются **Currency,** **Date/Time,** **Duration,** **Integer,** **Keywords** и **Text**. Пользователи могут определять настраиваемые поля с помощью конструктора форм в Outlook.
  
На уровне программируемости каждый элемент представлен [объектом IMessage.](imessageimapiprop.md) Каждое пользовательское поле связано с определением поля и значением. 
  
### <a name="field-definition"></a>Определение поля

Определение поля включает имя, тип данных и другие сведения о поле. Для каждого элемента Outlook определения всех пользовательских полей в свойстве [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) соответствующего **объекта IMessage.** Свойство **PidLidPropertyDefinitionStream** содержит двоичный поток, известный как [PropertyDefinition,](propertydefinition-stream-structure.md) содержащий определения полей. Дополнительные сведения о структурах потоков для определений полей см. в [руб.](stream-structures.md)
  
### <a name="field-value"></a>Значение поля

Каждое пользовательское поле элемента имеет значение, которое хранится в соответствующем имени свойства. Это свойство с именем находится в PS_PUBLIC_STRINGS свойств и имеет строку символов Юникод в качестве имени свойства. Тип данных свойства соответствует типу поля. Если свойство не присутствует в **объекте IMessage,** Outlook предполагает разумное значение по умолчанию для свойства. Например, для типа строки Outlook пустую строку, если свойства нет. 
  
## <a name="see-also"></a>См. также



[Добавление определения для нового User-Defined поля](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Пример потока PropertyDefinition](propertydefinition-stream-sample.md)
  
[Структуры потока](stream-structures.md)
  
[Структура потока PropertyDefinition](propertydefinition-stream-structure.md)
  
[Структура потока FieldDefinition](fielddefinition-stream-structure.md)
  
[Структура skipBlock Stream](skipblock-stream-structure.md)
  
[Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
  
[Структура потока PackedAnsiString](packedansistring-stream-structure.md)
  
[Структура потока PackedUnicodeString](packedunicodestring-stream-structure.md)

