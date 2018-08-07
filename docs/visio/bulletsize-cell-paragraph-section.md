---
title: Ячейка BulletSize (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
localization_priority: Normal
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: Указывает размер маркера.
ms.openlocfilehash: e1b6bd1b4535a70bf99b9cd90af3e0d52128da01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813299"
---
# <a name="bulletsize-cell-paragraph-section"></a>Ячейка BulletSize (раздел "Абзац")

Указывает размер маркера. 
  
## <a name="remarks"></a>Замечания

Это значение можно указать либо встроенные или настраиваемые элементы, как процент или определенного значения. 
  
Если значение равно нулю (0), маркер имеет тот же размер шрифта, как и для первого знака абзаца. Если значение равно процент, маркера изменяется в процентном соотношении от размер шрифта первого знака абзаца. Отрицательными числами обрабатывается как процентных значений.
  
Чтобы получить ссылку на ячейку BulletSize по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Para.BulletFontSize [ *i* ] где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки BulletSize по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visBulletFontSize** <br/> |
   

