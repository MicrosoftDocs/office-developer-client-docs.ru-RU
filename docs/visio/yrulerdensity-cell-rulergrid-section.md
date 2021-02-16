---
title: Ячейка YRulerDensity (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Определяет вертикальные промежуточные деления линейки для страницы.
ms.openlocfilehash: c92c48f6c86fc794cf6f53a87fdb99e67a73b9f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406803"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a>Ячейка YRulerDensity (раздел "Линейка и сетка")

Определяет вертикальные промежуточные деления линейки для страницы.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Фиксация  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |С большими интервалами  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |С обычными интервалами (по умолчанию)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |С небольшими интервалами  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Замечания

Эта ячейка соответствует параметру **Промежуточные деления по вертикали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**). 
  
Чтобы получить ссылку на ячейку YRulerDensity по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |YRulerDensity  <br/> |
   
Чтобы получить ссылку на ячейку YRulerDensity по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visYRulerDensity** <br/> |
   

