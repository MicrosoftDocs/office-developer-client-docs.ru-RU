---
title: Элементы Outlook и полей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 71c67c37cc4f9cd3ddd7a55c37c4ebd6ddd35cfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810083"
---
# <a name="outlook-items-and-fields"></a>Элементы Outlook и полей

  
  
**Применимо к**: Outlook 
  
Microsoft Outlook предоставляет типы элементов, которые специализируются функциональные возможности (, например почтовых элементов, встречи, контакты, задачи и заметки). Outlook предоставляет стандартных полей для каждого типа элемента, обычно называемую встроенных полей. Outlook позволяет пользователям создавать настраиваемые поля, обычно называемую пользовательских полей. В каждом поле связан с типом данных и значением. Примеры типов данных, **валюты**, **Даты и времени**, **длительность**, **целое число**, **ключевые слова**и **текст**. Пользователи могут определять настраиваемые поля с помощью конструктора форм в Outlook.
  
На уровне программирования каждого элемента представлен объектом [IMessage](imessageimapiprop.md) . В каждом поле пользовательских связан с определения поля и значения. 
  
### <a name="field-definition"></a>Определение поля

Определение поля включает в себя имя, тип данных и другие сведения о поле. Для каждого элемента Outlook хранятся определения всех пользовательских полей в свойстве [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) соответствующего объекта **IMessage** . Свойство **PidLidPropertyDefinitionStream** содержит двоичный поток, известных как [Определение свойства](propertydefinition-stream-structure.md) , которое содержит определения полей. Дополнительные сведения о потоке структуры для определения полей можно [Структур потока](stream-structures.md).
  
### <a name="field-value"></a>Значение поля

Каждый пользовательские поля элемента имеет значение, которая хранится в соответствующем именованное свойство. Именованные свойства PS_PUBLIC_STRINGS набор свойств и его строку знаков Юникод в качестве имени свойства. Тип данных свойства соответствует типа поля. Если свойство не существует в объекте **IMessage** , Outlook предполагается значение разумные по умолчанию для свойства. Например для типа string, Outlook предполагается пустая строка, если свойство не указан. 
  
## <a name="see-also"></a>См. также



[Добавьте определение для нового пользовательского поля](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Определение свойства потока образца](propertydefinition-stream-sample.md)
  
[Поток структуры](stream-structures.md)
  
[Определение свойства потока структуры](propertydefinition-stream-structure.md)
  
[Структура FieldDefinition потока](fielddefinition-stream-structure.md)
  
[Структура SkipBlock потока](skipblock-stream-structure.md)
  
[Структура FirstSkipBlockContent потока](firstskipblockcontent-stream-structure.md)
  
[Структура PackedAnsiString потока](packedansistring-stream-structure.md)
  
[Структура PackedUnicodeString потока](packedunicodestring-stream-structure.md)
