---
title: BulletSize Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
localization_priority: Normal
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: Указывает размер маркера.
ms.openlocfilehash: 8671bc6f5ec40814b13727bc458f74eb2893f839
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405424"
---
# <a name="bulletsize-cell-paragraph-section"></a>BulletSize Cell (Paragraph Section)

Указывает размер маркера. 
  
## <a name="remarks"></a>Примечания

Это значение может быть задано для предварительно определенных или настраиваемого маркеров в виде процента или определенного значения. 
  
Если значение — ноль (0), маркер имеет тот же размер шрифта, что и размер первого символа в абзаце. Если значение составляет процентное значение, размер маркера составляет процент от размера шрифта первого символа в абзаце. Отрицательные числа обрабатываются в процентах.
  
Чтобы получить ссылку на ячейку BulletSize по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Para.BulletFontSize[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку BulletSize по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph**  +   *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visBulletFontSize** <br/> |
   

