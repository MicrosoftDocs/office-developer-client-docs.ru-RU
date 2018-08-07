---
title: Структура потока SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d84704300602bada4cf93c9d3f6622feaf16f352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812316"
---
# <a name="skipblock-stream-structure"></a>Структура потока SkipBlock

  
  
**Относится к**: Outlook 
  
Структура потока SkipBlock — блок данных, который начинается с целое число, указывающее длину оставшихся часть блока. Эта структура потока существует в потоке [FieldDefinition](fielddefinition-stream-structure.md) Если определение поля в формате PropDefV2. 
  
Назначение структуру потока SkipBlock зависит от его относительно расположения в серии из как структуры в элементе data SkipBlocks FieldDefinition потока. Серии SkipBlocks должны содержать по крайней мере один SkipBlock структуры, который имеет элемент размер данных, равно 0 и завершает серии. Если первый структура не прерывающие структура (то есть элемент данных размером больше 0), Outlook предполагается, что первая структура указывает имя поля в кодировке Юникод (UTF-16).
  
Элементы данных в этот поток хранятся в прямом байтовом, сразу после друг с другом в указанном порядке.
  
- Размер: Значение DWORD (4 байта), размер, в байтах, элемента данных контента.
    
- Содержимое: Массив БАЙТОВ. Число этого массива равно размер элемента данных. Значение элемента контента данных зависит от расположения структура SkipBlock из серии и версии Outlook. Если первый структуры SkipBlock не прерывающие структуры, Outlook рассматривает первого структура SkipBlock структуры [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) потока, которая указывает имя поля в Юникод. 
    
## <a name="see-also"></a>См. также



[Поля и элементы Outlook](outlook-items-and-fields.md)
  
[Структуры потоков](stream-structures.md)
  
[Структура потока FieldDefinition](fielddefinition-stream-structure.md)
  
[Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)

