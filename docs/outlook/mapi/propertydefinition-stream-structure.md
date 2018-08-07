---
title: Определение свойства потока структуры
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 289227ee171c2325cad0ed321dab4f635a0ca724
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812090"
---
# <a name="propertydefinition-stream-structure"></a>Определение свойства потока структуры

**Относится к**: Outlook 
  
Структура потока определение свойства — массив структур [FieldDefinition](fielddefinition-stream-structure.md) потока, которые содержат определения для всех пользовательских полей в элемент Microsoft Outlook и параметры привязки данных для некоторых встроенных полей. 
  
Можно программно работать структура потока определение свойства. Тем не менее можно получить такой же результат с помощью конструктора форм Outlook, и, в частности, поле диалоговое окно **свойств** элемента управления с привязкой к данным. 
  
Определения полей в структуре потока определение свойства может иметь одно из следующих форматов: PropDefV1 и PropDefV2. Outlook поддерживает PropDefV1 и PropDefV2. Все определения полей в структуре одного потока определение свойства должен иметь тот же формат. Дополнительные сведения о отличия между PropDefV1 и PropDefV2 Просмотр [Структуры FieldDefinition потока](fielddefinition-stream-structure.md).
  
Элементы данных в этот поток хранятся в прямом байтовом, сразу после друг с другом в указанном порядке.
  
- Версия: WORD (2 байта), формат определения полей в определение свойства передать в потоковом режиме структуры. В следующей таблице показаны возможные значения.
    
    |**Значение**|**Описание**|
    |:-----|:-----|
    |0x0102  <br/> |Формат — PropDefV1.  <br/> |
    |0x0103  <br/> |Формат — PropDefV2.  <br/> |
   
- FieldDefinitionCount: Значение DWORD (4 байта), количество определения полей в этот поток. Это число элементов массива в элементе data FieldDefinitions.
    
- FieldDefinitions: Массив структур FieldDefinition потока. Число этого массива равно FieldDefinitionCount элемента данных.
    
## <a name="see-also"></a>См. также

- [Поля и элементы Outlook](outlook-items-and-fields.md)
- [Добавление определения для нового пользовательского поля](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [Пример потока PropertyDefinition](propertydefinition-stream-sample.md)
- [Структуры потоков](stream-structures.md)

