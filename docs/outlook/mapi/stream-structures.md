---
title: Структуры потоков
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
# <a name="stream-structures"></a>Структуры потоков

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определения пользовательских полей элемента Microsoft Outlook хранятся в свойстве [PidLidPropertyDefinitionStream.](pidlidpropertydefinitionstream-canonical-property.md) Значение этого свойства — это двоичный поток, содержащий определения пользовательских полей и параметры привязки данных для встроенных полей для элемента Outlook. В этом разделе содержится информация о структуре двоичного потока, разбитой на следующие структуры потока. 
  
> [!NOTE]
> Имена этих структур потока (например, PropertyDefinition, FieldDefinition и SkipBlock) и их элементы данных технически не являются частью программного интерфейса API обмена сообщениями (MAPI) и предоставляются здесь только для документации по фактическим структурам потоков. Разработчики могут пометить эти структуры потоков и элементы данных в своих приложениях по своему выбору. 
  
- [Структура потока PropertyDefinition](propertydefinition-stream-structure.md)
    
- [Структура потока FieldDefinition](fielddefinition-stream-structure.md)
    
- [Структура потока SkipBlock](skipblock-stream-structure.md)
    
- [Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
    
- [Структура потока PackedAnsiString](packedansistring-stream-structure.md)
    
- [Структура потока PackedUnicodeString](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>См. также



[Элементы и поля Outlook](outlook-items-and-fields.md)
  
[Добавление определения для нового поля User-Defined](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Пример потока PropertyDefinition](propertydefinition-stream-sample.md)

