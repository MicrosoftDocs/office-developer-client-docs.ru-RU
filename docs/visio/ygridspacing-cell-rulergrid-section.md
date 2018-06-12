---
title: Ячейка YGridSpacing (линейки &amp; сетка)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1210
localization_priority: Normal
ms.assetid: 30766e13-c90d-62fc-9c98-35ad7b0b4056
description: Указывает расстояние между вертикальными линиями фиксированной сетки (YGridDensity = 0).
ms.openlocfilehash: 638479719ee0649bf271403249e2cde2ddccf09c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815225"
---
# <a name="ygridspacing-cell-ruler-amp-grid-section"></a>Ячейка YGridSpacing (линейки &amp; сетка)

Указывает расстояние между вертикальными линиями фиксированной сетки (YGridDensity = 0).
  
## <a name="remarks"></a>Замечания

**Минимальный интервал** по вертикали, соответствует параметра в **линейки &amp; сетки** диалоговое окно "" (на вкладке **Вид** щелкните стрелку **Показать** ). 
  
Чтобы получить ссылку на ячейку YGridSpacing по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |YGridSpacing  <br/> |
   
Для получения ссылки на ячейки YGridSpacing по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visYGridSpacing** <br/> |
   

