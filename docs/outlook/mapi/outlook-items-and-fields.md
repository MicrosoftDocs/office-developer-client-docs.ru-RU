---
title: Элементы и поля Outlook
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
# <a name="outlook-items-and-fields"></a>Элементы и поля Outlook

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook предоставляет типы элементов, специализированные для их функциональности (например, почтовые элементы, встречи, контакты, задачи и заметки). Outlook предоставляет стандартные поля для каждого типа элемента, обычно именуемого встроенными полями. Outlook также позволяет пользователям создавать настраиваемые поля, которые обычно называются пользовательскими полями. Каждое поле связано с типом данных и значением. Примеры типов данных: **"Валюта",** **"Дата/время",** **"Длительность",** **"Integer",** **"Ключевые слова"** и **"Текст".** Пользователи могут определять настраиваемые поля с помощью конструктора форм в Outlook.
  
На уровне программируемости каждый элемент представлен объектом [IMessage.](imessageimapiprop.md) Каждое пользовательское поле связано с определением поля и значением. 
  
### <a name="field-definition"></a>Определение поля

Определение поля включает имя, тип данных и другие сведения о поле. Для каждого элемента Outlook сохраняет определения всех пользовательских полей в свойстве [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) соответствующего **объекта IMessage.** Свойство **PidLidPropertyDefinitionStream** содержит двоичный поток, известный как [PropertyDefinition,](propertydefinition-stream-structure.md) содержащий определения полей. Дополнительные сведения о структурах потоков для определений полей см. в [подстройки Stream.](stream-structures.md)
  
### <a name="field-value"></a>Значение поля

Каждое определяемого пользователем поле элемента имеет значение, которое хранится в соответствующем именоваемом свойстве. Это именоватое свойство находится в PS_PUBLIC_STRINGS свойства и имеет строку символов Юникода в качестве имени свойства. Тип данных свойства соответствует типу поля. Если свойство не присутствует в объекте **IMessage,** Outlook принимает разумное значение по умолчанию для свойства. Например, для типа строки Outlook предполагает пустую строку, если свойства нет. 
  
## <a name="see-also"></a>См. также



[Добавление определения для нового поля User-Defined](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Пример потока PropertyDefinition](propertydefinition-stream-sample.md)
  
[Структуры потоков](stream-structures.md)
  
[Структура потока PropertyDefinition](propertydefinition-stream-structure.md)
  
[Структура потока FieldDefinition](fielddefinition-stream-structure.md)
  
[Структура потока SkipBlock](skipblock-stream-structure.md)
  
[Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
  
[Структура потока PackedAnsiString](packedansistring-stream-structure.md)
  
[Структура потока PackedUnicodeString](packedunicodestring-stream-structure.md)

