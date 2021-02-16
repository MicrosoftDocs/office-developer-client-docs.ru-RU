---
title: IndFirst Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251254
localization_priority: Normal
ms.assetid: 0f2e362a-3ace-787d-6326-b5bf707f0727
description: Представляет расстояние от левого отступа абзаца от первой строки каждого абзаца в текстовом блоке фигуры. Это значение не зависит от масштаба рисунка. При масштабе рисования отступ первой строки остается тем же.
ms.openlocfilehash: aa6d9fd14a40f4fe6b269d9750f603d8faf1d550
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410324"
---
# <a name="indfirst-cell-paragraph-section"></a>IndFirst Cell (Paragraph Section)

Представляет расстояние от левого отступа абзаца от первой строки каждого абзаца в текстовом блоке фигуры. Это значение не зависит от масштаба рисунка. При масштабе рисования отступ первой строки остается тем же.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку IndFirst по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Para.IndFirst[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку IndFirst по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph**  +   *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visIndentFirst** <br/> |
   

