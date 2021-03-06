---
title: Color Cell (Reviewer Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60032
localization_priority: Normal
ms.assetid: c1e3d7bf-e6b6-65f1-ae40-80c8ba4821cd
description: Значение RGB, которое представляет цвет, присвоенный разметке рецензента документов.
ms.openlocfilehash: d9df6605ca6c8a22353978b9483989ecfc08130d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430541"
---
# <a name="color-cell-reviewer-section"></a>Color Cell (Reviewer Section)

Значение RGB, которое представляет цвет, присвоенный разметке рецензента документов. 
  
## <a name="remarks"></a>Примечания

Цвета назначены рецензентам в следующей последовательности: красный, синий, зеленый, фиолетовый, оранжевый, бирюзовый, серый. Эти цвета снова циклика для остальных рецензентов. 
  
Комментарии, вступив на исходной странице рисования, всегда окрашены в желтый цвет независимо от цвета, назначенного рецензенту в ячейке Color. 
  
Чтобы получить ссылку на ячейку Color по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Reviewer.Color  *[i]*  где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку Color по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionReviewer** <br/> |
| Индекс строки:  <br/> |**visRowReviewer**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> |**visReviewerColor** <br/> |
   

