---
title: Ячейка YGridDensity (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Указывает тип вертикальной сетки для использования.
ms.openlocfilehash: 793fa40316edd591c8b4873d8919507c2393b5d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307709"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a>Ячейка YGridDensity (раздел "Линейка и сетка")

Указывает тип вертикальной сетки для использования.
  
|**Value**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|нуль  <br/> |Фиксация  <br/> |**visGridFixed** <br/> |
|2  <br/> |С большими интервалами  <br/> |**visGridCoarse** <br/> |
|SP4  <br/> |С обычными интервалами (по умолчанию)  <br/> |**visGridNormal** <br/> |
|8,5  <br/> |С небольшими интервалами  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Замечания

Эта ячейка соответствует параметру **Интервал между линиями сетки по вертикали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**). 
  
Чтобы получить ссылку на ячейку YGridDensity по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |YGridDensity  <br/> |
   
Чтобы получить ссылку на ячейку YGridDensity по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visYGridDensity** <br/> |
   

