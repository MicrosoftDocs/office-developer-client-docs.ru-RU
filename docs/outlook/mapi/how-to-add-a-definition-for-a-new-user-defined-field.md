---
title: Добавьте определение для нового пользовательского поля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a2f9d1623c3733292ebf5c65452ac0d65f577c4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592719"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Добавьте определение для нового пользовательского поля
 
**Применимо к**: Outlook 2013 | Outlook 2016 
  
При добавлении пользовательских полей в элемент Microsoft Outlook вы добавьте определение поля в соответствующем структуру потока [Определение свойства](propertydefinition-stream-structure.md) . Используйте следующую процедуру, чтобы добавить новое определение поля на структуру потока определение свойства. 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>Добавление определения пользовательского поля

1. Копирование существующего определения полей структуры потока определение свойства новый массив определения поля. 
    
2. Если все существующие определения поля, в формате PropDefV1 преобразуйте их в формат PropDefV2. Дополнительные сведения о форматах определения поля [Определение свойства потока](propertydefinition-stream-structure.md) - [Структура потока FieldDefinition](fielddefinition-stream-structure.md)см.
    
3. Создание определения нового поля, выбранные пользователем в формате PropDefV2 и добавить его в массиве.
    
4. Установите элемент Version структуры потока определение свойства в качестве 0x0103, если элемент Version не были установлены для этого значения.
    
5. Увеличьте элемент FieldDefinitionCount на 1.
    
6. Сохраните как значение элемента FieldDefinitions массива.
    
## <a name="see-also"></a>См. также

- [Структура потока PropertyDefinition](propertydefinition-stream-structure.md)

