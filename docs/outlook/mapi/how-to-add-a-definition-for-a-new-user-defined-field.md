---
title: Добавление определения для нового пользовательского поля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2879299d152d8fea7690162ae55a22f337f5fd59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428167"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a>Добавление определения для нового пользовательского поля
 
**Относится к**: Outlook 2013 | Outlook 2016 
  
При добавлении пользовательского поля в элемент Microsoft Outlook определение поля добавляется в соответствующую структуру [потока PropertyDefinition.](propertydefinition-stream-structure.md) Используйте следующую процедуру для добавления нового определения поля в структуру потока PropertyDefinition. 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a>Добавление определения для нового пользовательского поля

1. Скопируйте существующие определения полей структуры потока PropertyDefinition в новый массив определений полей. 
    
2. Если существующие определения полей имеют формат PropDefV1, преобразуйте их в формат PropDefV2. Дополнительные сведения о форматах определений полей см. в разделах [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) и [FieldDefinition Stream Structure.](fielddefinition-stream-structure.md)
    
3. Создайте определение нового пользовательского поля в формате PropDefV2 и добавьте его в массив.
    
4. Установите элемент Version структуры потока PropertyDefinition как 0x0103, если элемент Version не имеет этого значения.
    
5. Приращение элемента FieldDefinitionCount на 1.
    
6. Храните массив в качестве значения элемента FieldDefinitions.
    
## <a name="see-also"></a>См. также

- [Структура потока PropertyDefinition](propertydefinition-stream-structure.md)

