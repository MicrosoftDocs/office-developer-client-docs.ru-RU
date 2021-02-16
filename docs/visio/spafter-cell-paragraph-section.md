---
title: SpAfter Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm960
localization_priority: Normal
ms.assetid: 2dd56ae5-300e-ba09-a73a-83c2b6c2a0ef
description: Определяет объем пространства, вставляемого после каждого абзаца в текстовом блоке фигуры, в дополнение к пространству из ячейки SpLine и, если это последний абзац в текстовом блоке, ячейка BottomMargin.
ms.openlocfilehash: 2b8fe7e2b0df09561d0db4367f917c8f4b71335d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439837"
---
# <a name="spafter-cell-paragraph-section"></a>SpAfter Cell (Paragraph Section)

Определяет объем пространства, вставляемого после каждого абзаца в текстовом блоке фигуры, в дополнение к пространству из ячейки SpLine и, если это последний абзац в текстовом блоке, ячейку BottomMargin.
  
## <a name="remarks"></a>Примечания

Это значение не зависит от масштаба рисунка. Если рисунок масштабировать, параметр "Пробел после" остается тем же.
  
Чтобы получить ссылку на ячейку SpAfter по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Para.SpAfter[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку SpAfter по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph**  +   *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visSpaceAfter** <br/> |
   

