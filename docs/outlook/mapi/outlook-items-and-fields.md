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
  
Microsoft Outlook предоставляет типы элементов, которые могут быть специализированными для своих функций (например, почтовые элементы, встречи, контакты, задачи и заметки). Outlook предоставляет стандартные поля для каждого типа элементов, которые обычно называют встроенными полями. Кроме того, Outlook позволяет пользователям создавать настраиваемые поля, которые обычно называются пользовательскими полями. Каждое поле связано с типом данных и значением. Примерами типов данных являются " **Валюта**", " **Дата/время**", " **Продолжительность**" ****, " **целое число**", " **Ключевые слова**" и " Пользователи могут определять настраиваемые поля с помощью конструктора форм в Outlook.
  
На уровне программирования каждый элемент представлен объектом [iMessage](imessageimapiprop.md) . Каждое определяемое пользователем поле связано с определением поля и значением. 
  
### <a name="field-definition"></a>Определение поля

Определение поля включает имя, тип данных и другие сведения о поле. Для каждого элемента Outlook хранит определения всех полей, определенных пользователем, в свойстве [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) соответствующего объекта **iMessage** . Свойство **PidLidPropertyDefinitionStream** содержит двоичный поток, называемый [PropertyDefinition](propertydefinition-stream-structure.md) , который содержит определения полей. Дополнительные сведения о структурах потоков для определений полей приведены в разделе [структуры потоков](stream-structures.md).
  
### <a name="field-value"></a>Значение поля

Каждое определяемое пользователем поле элемента имеет значение, хранящееся в соответствующем именованном свойстве. Это именованное свойство находится в наборе свойств ПС_ПУБЛИК_СТРИНГС и имеет строку символов Юникода в качестве имени свойства. Тип данных свойства соответствует типу поля. Если свойство отсутствует в объекте **iMessage** , Outlook предполагает значение свойства по умолчанию. Например, для строкового типа в Outlook предполагается пустая строка, если свойство отсутствует. 
  
## <a name="see-also"></a>См. также



[Добавление определения для нового пользовательского поля](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Пример потока PropertyDefinition](propertydefinition-stream-sample.md)
  
[Структуры потока](stream-structures.md)
  
[Структура потока PropertyDefinition](propertydefinition-stream-structure.md)
  
[Структура потока FieldDefinition](fielddefinition-stream-structure.md)
  
[Структура потока SkipBlock](skipblock-stream-structure.md)
  
[Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
  
[Структура потока PackedAnsiString](packedansistring-stream-structure.md)
  
[Структура потока PackedUnicodeString](packedunicodestring-stream-structure.md)

