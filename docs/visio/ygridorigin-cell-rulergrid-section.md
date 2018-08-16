---
title: Ячейка YGridOrigin (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1205
localization_priority: Normal
ms.assetid: eeec59f8-f301-5639-ffd6-8a36b2bf9c8f
description: Указывает начало сетки по вертикали.
ms.openlocfilehash: 2d914fc15df8a100066ad17a2e35001fe8a4d587
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815217"
---
# <a name="ygridorigin-cell-ruler-amp-grid-section"></a>Ячейка YGridOrigin (раздел "Линейка и сетка")

Указывает начало сетки по вертикали.
  
## <a name="remarks"></a>Замечания

Эта ячейка соответствует параметру **Начало сетки по вертикали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**). 
  
Чтобы получить ссылку на ячейку YGridOrigin по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |YGridOrigin  <br/> |
   
Чтобы получить ссылку на ячейку YGridOrigin по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visYGridOrigin** <br/> |
   

