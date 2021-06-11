---
title: BulletFont Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60023
localization_priority: Normal
ms.assetid: a75ff1f3-2f4d-89e3-108b-e16a34f5184f
description: Представляет число шрифта, используемого для формата текста при указании настраиваемой строки пули, а значение в ячейке Bullet не нулевое.
ms.openlocfilehash: 1cf04917bb7dfa68ee9395abb66ffe9e150f0273
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438465"
---
# <a name="bulletfont-cell-paragraph-section"></a>BulletFont Cell (Paragraph Section)

Представляет число шрифта, используемого для формата текста при указании настраиваемой строки пули, а значение в ячейке Bullet не нулевое. 
  
## <a name="remarks"></a>Примечания

Номера шрифтов различаются в зависимости от шрифтов, установленных в системе. Если значение 0 и есть настраиваемая строка пули, используемый шрифт является таким же, как шрифт первого символа абзаца.
  
Чтобы получить ссылку на ячейку BulletFont по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Para.BulletFont[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку BulletFont по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionParagraph** <br/> |
| Индекс строки:  <br/> |**visRowParagraph**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> |**visBulletFont** <br/> |
   

