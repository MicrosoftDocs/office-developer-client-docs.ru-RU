---
title: DirY / B Cell (Connection Points Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
localization_priority: Normal
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Определяет y-компонент для необходимого вектора выравнивания точки подключения. Он также используется для сориентировать присоединенную ногу динамического соединителя. Эта ячейка принимает значение плавающей точки.
ms.openlocfilehash: b0dc3c9f7e1a9e87b2ecdace21c8fa1658b1388d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417093"
---
# <a name="diry--b-cell-connection-points-section"></a>DirY / B Cell (Connection Points Section)

Определяет  *y-компонент*  для необходимого вектора выравнивания точки подключения. Он также используется для сориентировать присоединенную ногу динамического соединителя. Эта ячейка принимает значение плавающей точки. 
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку DirY /B по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Connections.DirY[i] где *i* = <1>, 2, 3...   <br/> |
   
Чтобы получить ссылку на ячейку DirY/B по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionConnectionPts** <br/> |
|Индекс строки:  <br/> |**visRowConnectionPts** +  *i*, где *i* = 0, 1, 2…  <br/> |
|Индекс ячейки:  <br/> |**visCnnctDirY** (не расширенные строки)           **visCnnctB** (расширенные строки)  <br/> |
   
Сведения о расширенных и расширенных строках см. в строке Точки подключения.
  

