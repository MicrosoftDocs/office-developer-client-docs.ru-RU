---
title: PinX Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm790
localization_priority: Normal
ms.assetid: dd88fb8d-3ec3-476a-870d-6642b191496f
description: Представляет x-координату пин-кода фигуры (центр вращения) по отношению к происхождению ее родителя.
ms.openlocfilehash: de12b379d5f345209a468298174634ff4f9cd639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404822"
---
# <a name="pinx-cell-shape-transform-section"></a>PinX Cell (Shape Transform Section)

Представляет  *x-координату*  пин-кода фигуры (центр вращения) по отношению к происхождению ее родителя. 
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку PinX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PinX  <br/> |
   
Чтобы получить ссылку на ячейку PinX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowXFormOut** <br/> |
| Индекс ячейки:  <br/> |**visXFormPinX** <br/> |
   

