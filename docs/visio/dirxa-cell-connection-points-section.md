---
title: DirX / A Cell (Connection Points Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
localization_priority: Normal
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: Определяет X-компонент для требуемого вектора выравнивания совпадающих точек подключения. Ячейка DirX /A также используется для ориентирования присоединенной ногой динамического соединителя. Эта ячейка принимает значение с плавающей за точкой.
ms.openlocfilehash: cb86ef1064537911ffd00a66f5c0b7942459f85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422399"
---
# <a name="dirx--a-cell-connection-points-section"></a>DirX / A Cell (Connection Points Section)

Определяет  *x-компонент*  для требуемого вектора выравнивания совпадающих точек подключения. Ячейка DirX /A также используется для ориентирования присоединенной ногой динамического соединителя. Эта ячейка принимает значение с плавающей за точкой. 
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку DirX или ячейку по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Connections.DirX[  *i*  ] где  *i*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на DirX / ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionConnectionPts** <br/> |
| Индекс строки:  <br/> |**visRowConnectionPts**  +   *i,* *где i* = 0, 1, 2  <br/> |
| Индекс ячейки:  <br/> |**visCnnctDirX** (неширимые строки)           **visCnnctA** (расширенные строки)  <br/> |
   
Сведения о невыбранных и расширенных строках см. в строке "Точки подключения".
  

