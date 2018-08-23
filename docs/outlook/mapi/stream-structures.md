---
title: Структуры потоков
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5f372e93457f2b7ef8830ae6bd0363f6b3a7bd60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581582"
---
# <a name="stream-structures"></a>Структуры потоков

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Определения пользовательских полей элемента Microsoft Outlook сохраняются в свойстве [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) . Значение этого свойства — это двоичный поток, который содержит определения пользовательских полей и параметров привязки данных для встроенных полей для элемента Outlook. В этом разделе представлены сведения о структуре двоичный поток, разбитым в следующих структур потока. 
  
> [!NOTE]
> Имена эти структуры потока (например, определение свойства, FieldDefinition и SkipBlock) и их элементов данных не технически частью API-интерфейс системы обмена сообщениями API (MAPI) и содержащиеся в этой статье только для документации в целях структур фактический потока. Разработчики можно пометить эти элементы структуры и данные потока в своих приложениях по своему выбору. 
  
- [Структура потока PropertyDefinition](propertydefinition-stream-structure.md)
    
- [Структура потока FieldDefinition](fielddefinition-stream-structure.md)
    
- [Структура потока SkipBlock](skipblock-stream-structure.md)
    
- [Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
    
- [Структура потока PackedAnsiString](packedansistring-stream-structure.md)
    
- [Структура потока PackedUnicodeString](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a>См. также



[Поля и элементы Outlook](outlook-items-and-fields.md)
  
[Добавление определения для нового пользовательского поля](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Пример потока PropertyDefinition](propertydefinition-stream-sample.md)

