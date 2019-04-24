---
title: Ячейка XGridSpacing (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: Определяет расстояние между горизонтальными линиями в фиксированной сетке (XGridDensity = 0).
ms.openlocfilehash: 05b68a9721dbfc9c03402d384d976c42ef05b134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327323"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a>Ячейка XGridSpacing (раздел "Линейка и сетка")

Определяет расстояние между горизонтальными линиями в фиксированной сетке (XGridDensity = 0).
  
## <a name="remarks"></a>Замечания

Эта ячейка соответствует параметру **Минимальный интервал** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**). 
  
Чтобы получить ссылку на ячейку XGridSpacing по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |XGridSpacing  <br/> |
   
Чтобы получить ссылку на ячейку XGridSpacing по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visXGridSpacing** <br/> |
   

