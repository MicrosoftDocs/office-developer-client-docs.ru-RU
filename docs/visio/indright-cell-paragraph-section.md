---
title: IndRight Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251256
localization_priority: Normal
ms.assetid: f0891064-95d9-ae1b-28f3-3aef1406b636
description: Представляет расстояние, на которое все строки текста в абзаце отступят от правого поля текстового блока. Это значение не зависит от масштаба рисования. Если рисунок масштабировать, правый отступ остается тем же.
ms.openlocfilehash: e6529bf41cb8fdd40371d9a663291961626afb56
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408868"
---
# <a name="indright-cell-paragraph-section"></a>IndRight Cell (Paragraph Section)

Представляет расстояние, на которое все строки текста в абзаце отступят от правого поля текстового блока. Это значение не зависит от масштаба рисования. Если рисунок масштабировать, правый отступ остается тем же.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку IndRight по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Para.IndRight[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку IndRight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph**  +   *i,* *где i* = 0, 1, 2...  <br/> |
| Индекс ячейки:  <br/> |**visIndentRight** <br/> |
   

