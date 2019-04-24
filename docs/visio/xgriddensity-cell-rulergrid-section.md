---
title: Ячейка XGridDensity (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Указывает тип горизонтальной сетки для использования.
ms.openlocfilehash: 5ebd172e56a66bfb39bd9bfa20967bb6b52c5aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328990"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>Ячейка XGridDensity (раздел "Линейка и сетка")

Указывает тип горизонтальной сетки для использования.
  
|**Value**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|нуль  <br/> |Фиксация  <br/> |**visGridFixed** <br/> |
|2  <br/> |С большими интервалами  <br/> |**visGridCoarse** <br/> |
|SP4  <br/> |С обычными интервалами (по умолчанию)  <br/> |**visGridNormal** <br/> |
|8,5  <br/> |С небольшими интервалами  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Замечания

Эта ячейка соответствует параметру **Интервал между линиями сетки по горизонтали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**). 
  
Чтобы получить ссылку на ячейку XGridDensity по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |XGridDensity  <br/> |
   
Чтобы получить ссылку на ячейку XGridDensity по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visXGridDensity** <br/> |
   

