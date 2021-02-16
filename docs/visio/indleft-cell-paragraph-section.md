---
title: IndLeft Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251255
localization_priority: Normal
ms.assetid: 31a7d0d4-4666-ddef-c5eb-4d13803e6a2f
description: Представляет расстояние, на которое все строки текста в абзаце отступят от левого поля текстового блока. Это значение не зависит от масштаба рисунка. Если рисунок масштабировать, отступ слева остается тем же.
ms.openlocfilehash: 2a942ef3d874b8d1ce2ef85f423c93bc0db33230
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405165"
---
# <a name="indleft-cell-paragraph-section"></a>IndLeft Cell (Paragraph Section)

Представляет расстояние, на которое все строки текста в абзаце отступят от левого поля текстового блока. Это значение не зависит от масштаба рисования. Если рисунок масштабировать, отступ слева остается тем же.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку IndLeft по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Para.IndLeft[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку IndLeft по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph**  +   *i* где *i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visIndentLeft** <br/> |
   

