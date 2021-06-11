---
title: Структура skipBlock Stream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5a3367a15374234658fd9d10f3c2a5f3a191c80e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435546"
---
# <a name="skipblock-stream-structure"></a>Структура skipBlock Stream

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Структура потока SkipBlock — это блок данных, который начинается с integer, который указывает длину оставшейся части блока. Эта структура потока существует в [потоке FieldDefinition,](fielddefinition-stream-structure.md) если определение поля находится в формате PropDefV2. 
  
Назначение структуры потока SkipBlock зависит от его относительного расположения в серии похожих структур в элементе данных SkipBlocks потока FieldDefinition. Серия SkipBlocks должна содержать по крайней мере одну структуру SkipBlock, которая завершает серию и имеет элемент данных Size, равный 0. Если первая структура не является структурой прекращения (то есть элемент данных Size больше 0), Outlook предполагает, что первая структура указывает имя поля в Unicode (UTF-16).
  
Элементы данных в этом потоке хранятся в порядке маленького byte, немедленно следуя друг за другом в порядке, указанном ниже.
  
- Размер: DWORD (4 bytes), размер, в количестве bytes, элемента данных контента.
    
- Содержимое. Массив BYTE. Количество этого массива равно элементу Данных Size. Значение элемента данных контента зависит от расположения структуры SkipBlock в серии и версии Outlook. Если первая структура SkipBlock не является структурой прекращения, Outlook первой структурой SkipBlock является структура [потока FirstSkipBlockContent,](firstskipblockcontent-stream-structure.md) которая указывает имя поля в Unicode. 
    
## <a name="see-also"></a>См. также



[Outlook Элементы и поля](outlook-items-and-fields.md)
  
[Структуры потока](stream-structures.md)
  
[Структура потока FieldDefinition](fielddefinition-stream-structure.md)
  
[Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)

