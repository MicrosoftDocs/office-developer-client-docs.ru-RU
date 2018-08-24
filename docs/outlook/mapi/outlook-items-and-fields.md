---
title: Поля и элементы Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: caa231842c5fd51deb80144f12fdf53e51ccc980
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582877"
---
# <a name="outlook-items-and-fields"></a>Поля и элементы Outlook

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook предоставляет типы элементов, которые специализируются функциональные возможности (, например почтовых элементов, встречи, контакты, задачи и заметки). Outlook предоставляет стандартных полей для каждого типа элемента, обычно называемую встроенных полей. Outlook позволяет пользователям создавать настраиваемые поля, обычно называемую пользовательских полей. В каждом поле связан с типом данных и значением. Примеры типов данных, **валюты**, **Даты и времени**, **длительность**, **целое число**, **ключевые слова**и **текст**. Пользователи могут определять настраиваемые поля с помощью конструктора форм в Outlook.
  
На уровне программирования каждого элемента представлен объектом [IMessage](imessageimapiprop.md) . В каждом поле пользовательских связан с определения поля и значения. 
  
### <a name="field-definition"></a>Определение поля

Определение поля включает в себя имя, тип данных и другие сведения о поле. Для каждого элемента Outlook хранятся определения всех пользовательских полей в свойстве [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) соответствующего объекта **IMessage** . Свойство **PidLidPropertyDefinitionStream** содержит двоичный поток, известных как [Определение свойства](propertydefinition-stream-structure.md) , которое содержит определения полей. Дополнительные сведения о потоке структуры для определения полей можно [Структур потока](stream-structures.md).
  
### <a name="field-value"></a>Значение поля

Каждый пользовательские поля элемента имеет значение, которая хранится в соответствующем именованное свойство. Именованные свойства PS_PUBLIC_STRINGS набор свойств и его строку знаков Юникод в качестве имени свойства. Тип данных свойства соответствует типа поля. Если свойство не существует в объекте **IMessage** , Outlook предполагается значение разумные по умолчанию для свойства. Например для типа string, Outlook предполагается пустая строка, если свойство не указан. 
  
## <a name="see-also"></a>См. также



[Добавление определения для нового пользовательского поля](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Пример потока PropertyDefinition](propertydefinition-stream-sample.md)
  
[Структуры потоков](stream-structures.md)
  
[Структура потока PropertyDefinition](propertydefinition-stream-structure.md)
  
[Структура потока FieldDefinition](fielddefinition-stream-structure.md)
  
[Структура потока SkipBlock](skipblock-stream-structure.md)
  
[Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
  
[Структура потока PackedAnsiString](packedansistring-stream-structure.md)
  
[Структура потока PackedUnicodeString](packedunicodestring-stream-structure.md)

