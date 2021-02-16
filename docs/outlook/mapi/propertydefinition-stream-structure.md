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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Структура потока PropertyDefinition — это массив структур [потока FieldDefinition,](fielddefinition-stream-structure.md) содержащий определения для всех пользовательских полей в элементе Microsoft Outlook, а также параметры привязки данных для некоторых встроенных полей. 
  
Вы можете программным образом управлять структурой потока PropertyDefinition. Однако аналогичные результаты можно получить с помощью конструктора форм  Outlook и, в частности, диалоговое окно "Свойства" для привязанного к данным управления. 
  
Определения полей в структуре потока PropertyDefinition могут иметь один из двух форматов: PropDefV1 и PropDefV2. Outlook поддерживает propDefV1 и PropDefV2. Все определения полей в одной структуре потока PropertyDefinition должны иметь одинаковый формат. Дополнительные сведения о том, чем отличаются PropDefV1 и PropDefV2, см. в структуре [потока FieldDefinition.](fielddefinition-stream-structure.md)
  
Элементы данных в этом потоке хранятся в порядок с небольшими конечными ветвями, сразу после друг друга в указанном ниже порядке.
  
- Версия: WORD (2 bytes), формат определений полей в структуре потока PropertyDefinition. В следующей таблице представлены возможные значения.
    
    |**Значение**|**Описание**|
    |:-----|:-----|
    |0x0102  <br/> |Формат: PropDefV1.  <br/> |
    |0x0103  <br/> |Формат: PropDefV2.  <br/> |
   
- FieldDefinitionCount: DWORD (4 bytes), количество определений полей в этом потоке. Это количество элементов массива в элементе данных FieldDefinitions.
    
- FieldDefinitions: массив структур потока FieldDefinition. Количество массивов равно элементу данных FieldDefinitionCount.
    
## <a name="see-also"></a>См. также

- [Элементы и поля Outlook](outlook-items-and-fields.md)
- [Добавление определения для нового поля User-Defined](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [Пример потока PropertyDefinition](propertydefinition-stream-sample.md)
- [Структуры потоков](stream-structures.md)

