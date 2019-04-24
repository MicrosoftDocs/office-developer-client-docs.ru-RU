---
title: Структура потока SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5a3367a15374234658fd9d10f3c2a5f3a191c80e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282672"
---
# <a name="skipblock-stream-structure"></a>Структура потока SkipBlock

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Структура потока SkipBlock — это блок данных, начинающийся с целого числа, который указывает длину оставшейся части блока. Эта структура потоков существует в потоке [FieldDefinition](fielddefinition-stream-structure.md) , если определение поля находится в формате PropDefV2. 
  
Цель структуры потока SkipBlock зависит от относительного расположения в ряде похожих структур в элементе данных Скипблоккс потока FieldDefinition. Ряд Скипблоккс должен содержать по крайней мере одну структуру SkipBlock, которая завершает ряд и имеет элемент данных size, равный 0. Если первая структура не является завершающей (то есть элемент данных size больше 0), то предполагается, что первая структура указывает имя поля в Юникоде (UTF-16).
  
Элементы данных в этом потоке хранятся в порядке байтов с прямым порядком байтов, сразу после друг друга в порядке, указанном ниже.
  
- Size: DWORD (4 байта), размер элемента данных контента (в байтах).
    
- Контент: массив БАЙТОВ. Количество этого массива равно элементу данных size. Значение элемента данных контента зависит от расположения структуры SkipBlock в серии и версии Outlook. Если первая структура SkipBlock не является завершающей, в Outlook рассматривается первая структура SkipBlock в качестве структуры потока [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) , указывающей имя поля в Юникоде. 
    
## <a name="see-also"></a>См. также



[Элементы и поля Outlook](outlook-items-and-fields.md)
  
[Структуры потока](stream-structures.md)
  
[Структура потока FieldDefinition](fielddefinition-stream-structure.md)
  
[Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)

