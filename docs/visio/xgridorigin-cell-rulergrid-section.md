---
title: Ячейка XGridOrigin (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1155
localization_priority: Normal
ms.assetid: 2b1a8902-b1d4-c3d9-8c9f-1a28fddacc59
description: Указывает горизонтальную координату начала сетки.
ms.openlocfilehash: ee58ea7d950dd7e422f8a60a13bac8aa4ed353a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428622"
---
# <a name="xgridorigin-cell-ruler-amp-grid-section"></a>Ячейка XGridOrigin (раздел "Линейка и сетка")

Указывает горизонтальную координату начала сетки.
  
## <a name="remarks"></a>Замечания

Эта ячейка соответствует параметру **Начало сетки** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**). 
  
Чтобы получить ссылку на ячейку XGridOrigin по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |XGridOrigin  <br/> |
   
Чтобы получить ссылку на ячейку XGridOrigin по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visXGridOrigin** <br/> |
   

