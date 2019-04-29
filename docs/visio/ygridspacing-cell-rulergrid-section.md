---
title: Ячейка YGridSpacing (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1210
localization_priority: Normal
ms.assetid: 30766e13-c90d-62fc-9c98-35ad7b0b4056
description: Определяет расстояние между вертикальными линиями в фиксированной сетке (YGridDensity = 0).
ms.openlocfilehash: fc355b4e509494e9e7570122a8a3a7a3ce2e0588
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417464"
---
# <a name="ygridspacing-cell-ruler-amp-grid-section"></a>Ячейка YGridSpacing (раздел "Линейка и сетка")

Определяет расстояние между вертикальными линиями в фиксированной сетке (YGridDensity = 0).
  
## <a name="remarks"></a>Замечания

Соответствует параметру **Минимальный интервал по вертикали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**). 
  
Чтобы получить ссылку на ячейку YGridSpacing по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |YGridSpacing  <br/> |
   
Чтобы получить ссылку на ячейку YGridSpacing по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visYGridSpacing** <br/> |
   

