---
title: SpBefore Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm965
localization_priority: Normal
ms.assetid: a7d5b0a1-3657-8211-f0e0-eaed588fa0bc
description: Определяет количество пространства, вставленного перед каждым абзацем в текстовом блоке фигуры, в дополнение к любому пространству из ячейки SpLine, если это первый абзац в текстовом блоке, ячейка TopMargin.
ms.openlocfilehash: 9890910a11990bb5be7fe3ee4af95e578c8d9799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425759"
---
# <a name="spbefore-cell-paragraph-section"></a>SpBefore Cell (Paragraph Section)

Определяет количество пространства, вставленного перед каждым абзацем в текстовом блоке фигуры, в дополнение к любому пространству из ячейки SpLine, если это первый абзац в текстовом блоке, ячейка TopMargin.
  
## <a name="remarks"></a>Примечания

Это значение не зависит от масштаба рисунка. Если рисунок масштабировать, параметр Space Before остается тем же.
  
Чтобы получить ссылку на ячейку SpBefore по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Para.SpBefore[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку SpBefore по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> |**visSpaceBefore** <br/> |
   

