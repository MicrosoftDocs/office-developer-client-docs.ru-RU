---
title: Ячейка SpBefore (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm965
localization_priority: Normal
ms.assetid: a7d5b0a1-3657-8211-f0e0-eaed588fa0bc
description: Определяет объем пространства, перед каждым абзацем в блоке текста фигуры пробелов из ячейки сплайн, если это первый абзац в блоке текста в ячейку TopMargin.
ms.openlocfilehash: d33a10220499020ba1a1acedf5782fdb78925c07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814927"
---
# <a name="spbefore-cell-paragraph-section"></a>Ячейка SpBefore (раздел "Абзац")

Определяет объем пространства, перед каждым абзацем в блоке текста фигуры пробелов из ячейки сплайн, если это первый абзац в блоке текста в ячейку TopMargin.
  
## <a name="remarks"></a>Замечания

Это значение не зависит от масштаба документа. Если документа изменяется, пространство перед параметр остается неизменным.
  
Чтобы получить ссылку на ячейку SpBefore по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Para.SpBefore [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки SpBefore по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visSpaceBefore** <br/> |
   

