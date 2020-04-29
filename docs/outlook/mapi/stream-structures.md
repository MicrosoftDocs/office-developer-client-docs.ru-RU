---
title: Структуры потока
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7f1f1e028797edaa0afb45df4f39aca15ff6d425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407825"
---
# <a name="stream-structures"></a>Структуры потока

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определения определяемых пользователем полей элемента Microsoft Outlook хранятся в свойстве [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) . Значение этого свойства — это двоичный поток, который содержит определения пользовательских полей и параметры привязки к данным для встроенных полей элемента Outlook. В этом разделе представлены сведения о структуре двоичного потока, разбитых в следующих структурах потока. 
  
> [!NOTE]
> Имена этих структур потоков (например, PropertyDefinition, FieldDefinition и SkipBlock) и их элементы данных технически не являются частью программного интерфейса API обмена сообщениями (MAPI) и предоставляются здесь только в целях документирования фактических структур потоков. Разработчики могут помечать эти структуры потоков и элементы данных в своих приложениях по мере их выбора. 
  
- [Структура потока PropertyDefinition](propertydefinition-stream-structure.md)
    
- [Структура потока FieldDefinition](fielddefinition-stream-structure.md)
    
- [Структура потока SkipBlock](skipblock-stream-structure.md)
    
- [Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
    
- [Структура потока PackedAnsiString](packedansistring-stream-structure.md)
    
- [Структура потока PackedUnicodeString](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>См. также



[Элементы и поля Outlook](outlook-items-and-fields.md)
  
[Добавление определения для нового пользовательского поля](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Пример потока PropertyDefinition](propertydefinition-stream-sample.md)

