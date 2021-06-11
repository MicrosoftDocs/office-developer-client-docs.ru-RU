---
title: Структура потока PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 479339762867aa778bc8bc8baa1f21f6bc34b441
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438591"
---
# <a name="propertydefinition-stream-structure"></a>Структура потока PropertyDefinition

**Область применения**: Outlook 2013 | Outlook 2016 
  
Структура потока PropertyDefinition — это массив структур [потока FieldDefinition,](fielddefinition-stream-structure.md) содержащих определения для всех пользовательских полей в элементе Microsoft Outlook, а также параметры привязки данных для некоторых встроенных полей. 
  
Можно программным образом управлять структурой потока PropertyDefinition. Однако аналогичные результаты можно добиться с помощью Outlook конструктора форм и, в частности, диалоговое окно **Properties** для управления, связанного с данными. 
  
Определения поля в структуре потока PropertyDefinition могут быть одним из двух форматов: PropDefV1 и PropDefV2. Outlook поддерживает и PropDefV1, и PropDefV2. Все определения полей в одной структуре потока PropertyDefinition должны быть одного формата. Дополнительные сведения о том, как отличаются PropDefV1 и PropDefV2, см. в [разделах FieldDefinition Stream Structure.](fielddefinition-stream-structure.md)
  
Элементы данных в этом потоке хранятся в порядке маленького byte, немедленно следуя друг за другом в порядке, указанном ниже.
  
- Версия: WORD (2 bytes), формат определений полей в структуре потока PropertyDefinition. В следующей таблице представлены возможные значения.
    
    |**Значение**|**Описание**|
    |:-----|:-----|
    |0x0102  <br/> |Формат PropDefV1.  <br/> |
    |0x0103  <br/> |Формат PropDefV2.  <br/> |
   
- FieldDefinitionCount: DWORD (4 bytes), количество определений полей в этом потоке. Это количество элементов массива в элементе данных FieldDefinitions.
    
- FieldDefinitions: массив структур потока FieldDefinition. Количество этого массива равно элементу данных FieldDefinitionCount.
    
## <a name="see-also"></a>См. также

- [Outlook Элементы и поля](outlook-items-and-fields.md)
- [Добавление определения для нового User-Defined поля](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [Пример потока PropertyDefinition](propertydefinition-stream-sample.md)
- [Структуры потока](stream-structures.md)

