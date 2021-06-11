---
title: BulletString Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
localization_priority: Normal
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: Позволяет создать настраиваемый стиль пули.
ms.openlocfilehash: b7a1d7f845c7b9945670240361a4ac66efa80786
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409750"
---
# <a name="bulletstring-cell-paragraph-section"></a>BulletString Cell (Paragraph Section)

Позволяет создать настраиваемый стиль пули. 
  
## <a name="remarks"></a>Примечания

Введите стиль в качестве строки (в кавычках). Например, можно ввести строку "ooo".
  
Вы также можете установить значение этой ячейки, щелкнув правой кнопкой мыши фигуру, указав на **формат,** щелкнув **текст,** а затем щелкнув вкладку **Bullets.** 
  
Чтобы получить ссылку на ячейку BulletString по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Para.BulletStr[ *i*  ] где  *i*  = <1>, 2, 3, ...  <br/> |
   
Чтобы получить ссылку на ячейку BulletString по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
|Индекс строки:  <br/> |**visRowParagraph**  +   *i,* *где i* = 0, 1, 2, ...  <br/> |
|Индекс ячейки:  <br/> |**visBulletString** <br/> |
   

