---
title: Brightness Cell (Image Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251608
localization_priority: Normal
ms.assetid: 5bb1cc81-f3fd-a835-1449-233dbd1a62b6
description: Настраивает яркость толщины толщины изображения. Уменьшите яркость изображения, введите значение от 0% до 49 % или увеличив яркость, введите значение от 51% до 100 %. Значение по умолчанию — 50%.
ms.openlocfilehash: ae1390d2db3adad86a8afcbeaff88172a841d030
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424793"
---
# <a name="brightness-cell-image-properties-section"></a>Brightness Cell (Image Properties Section)

Настраивает яркость толщины толщины изображения. Уменьшите яркость изображения, введите значение от 0% до 49 % или увеличив яркость, введите значение от 51% до 100 %. Значение по умолчанию — 50%.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Brightness по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Яркость  <br/> |
   
Чтобы получить ссылку на ячейку Brightness по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowImage** <br/> |
| Индекс ячейки:  <br/> |**visImageBrightness** <br/> |
   

