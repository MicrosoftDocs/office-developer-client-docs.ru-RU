---
title: Ячейка XGridSpacing (линейки &amp; сетка)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: Указывает расстояние между линиями фиксированной сетки (XGridDensity = 0).
ms.openlocfilehash: 5f461d02dae1574fe2b186b43166ef14d8251df2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815188"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a>Ячейка XGridSpacing (линейки &amp; сетка)

Указывает расстояние между линиями фиксированной сетки (XGridDensity = 0).
  
## <a name="remarks"></a>Замечания

В этой ячейке соответствует **минимальный интервал** по горизонтали параметра в **линейки &amp; сетки** диалоговое окно "" (на вкладке **Вид** щелкните стрелку **Показать** ). 
  
Чтобы получить ссылку на ячейку XGridSpacing по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |XGridSpacing  <br/> |
   
Для получения ссылки на ячейки XGridSpacing по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visXGridSpacing** <br/> |
   

