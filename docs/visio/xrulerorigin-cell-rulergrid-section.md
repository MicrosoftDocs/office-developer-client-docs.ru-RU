---
title: Ячейка XRulerOrigin (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1170
localization_priority: Normal
ms.assetid: 328f8ab5-217f-0336-0d56-611eff509fe8
description: Указывает точку начала координат на линейке по оси X для страницы.
ms.openlocfilehash: d66fd324718ec46b1209c4726eeb2d27c21db8b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346454"
---
# <a name="xrulerorigin-cell-ruler-amp-grid-section"></a>Ячейка XRulerOrigin (раздел "Линейка и сетка")

Указывает точку начала координат на линейке по оси X для страницы.
  
## <a name="remarks"></a>Замечания

Эта ячейка соответствует параметру **Ноль на горизонтальной линейке** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**). 
  
Чтобы получить ссылку на ячейку XRulerOrigin по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |XRulerOrigin  <br/> |
   
Чтобы получить ссылку на ячейку XRulerOrigin по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visXRulerOrigin** <br/> |
   

