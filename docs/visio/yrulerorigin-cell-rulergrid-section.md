---
title: Ячейка YRulerOrigin (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1220
localization_priority: Normal
ms.assetid: 5d21b64f-a559-76ef-06df-d24c048cc6ef
description: Указывает точку начала координат на линейке по оси y для страницы.
ms.openlocfilehash: ead9ca453bfeb86f32a943950b297b9b629de95d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284967"
---
# <a name="yrulerorigin-cell-ruler-amp-grid-section"></a>Ячейка YRulerOrigin (раздел "Линейка и сетка")

Указывает точку начала координат на линейке по оси y для страницы.
  
## <a name="remarks"></a>Замечания

Эта ячейка соответствует параметру **Ноль на вертикальной линейке** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**). 
  
Чтобы получить ссылку на ячейку YRulerOrigin по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |YRulerOrigin  <br/> |
   
Чтобы получить ссылку на ячейку YRulerOrigin по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visYRulerOrigin** <br/> |
   

