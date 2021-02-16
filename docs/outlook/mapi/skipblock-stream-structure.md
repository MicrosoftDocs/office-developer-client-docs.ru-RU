---
title: Структура потока SkipBlock
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
# <a name="skipblock-stream-structure"></a>Структура потока SkipBlock

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Структура потока SkipBlock — это блок данных, который начинается с integer, которое указывает длину оставшейся части блока. Эта структура потока существует в [потоке FieldDefinition,](fielddefinition-stream-structure.md) если определение поля имеет формат PropDefV2. 
  
Назначение структуры потока SkipBlock зависит от его относительного расположения в ряду похожих структур в элементе данных SkipBlocks потока FieldDefinition. Серия SkipBlocks должна содержать по крайней мере одну структуру SkipBlock, которая завершает ряд и имеет элемент данных Size, равный 0. Если первая структура не является структурой прерывания (то есть элемент данных Size больше 0), Outlook предполагает, что первая структура указывает имя поля в Юникод (UTF-16).
  
Элементы данных в этом потоке хранятся в порядок с небольшими конечными ветвями, сразу после друг друга в указанном ниже порядке.
  
- Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.
    
- Содержимое: массив BYTE. Количество массивов равно элементу данных Size. Значение элемента "Данные содержимого" зависит от расположения структуры SkipBlock в ряду и версии Outlook. Если первая структура SkipBlock не является структурой прерывания, Outlook рассматривает первую структуру SkipBlock как структуру [потока FirstSkipBlockContent,](firstskipblockcontent-stream-structure.md) которая указывает имя поля в Юникоде. 
    
## <a name="see-also"></a>См. также



[Элементы и поля Outlook](outlook-items-and-fields.md)
  
[Структуры потоков](stream-structures.md)
  
[Структура потока FieldDefinition](fielddefinition-stream-structure.md)
  
[Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)

