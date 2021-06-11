---
title: TextPosAfterBullet Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
localization_priority: Normal
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: Представляет расстояние между первой строкой абзаца и пулей.
ms.openlocfilehash: a98967cb5f9541434745c3b3d6afafde0878074a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422154"
---
# <a name="textposafterbullet-cell-paragraph-section"></a>TextPosAfterBullet Cell (Paragraph Section)

Представляет расстояние между первой строкой абзаца и пулей. 
  
## <a name="remarks"></a>Примечания

Это расстояние добавляется к расстоянию, содержамуся в ячейке IndFirst, которая является левой отступной по умолчанию. Это значение не зависит от масштаба рисунка. 
  
Чтобы получить ссылку на ячейку TextPosAfterBullet по имени из другой формулы или из программы с использованием свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Para.TextPosAfterBullet[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку TextPosAfterBullet по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> |**visTextPosAfterBullet** <br/> |
   

