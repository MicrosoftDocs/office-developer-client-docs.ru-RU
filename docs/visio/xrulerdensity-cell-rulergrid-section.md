---
title: Ячейка XRulerDensity (раздел "Линейка и сетка")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Определяет горизонтальные промежуточные деления линейки для страницы.
ms.openlocfilehash: f459e5d1d19580201f1404ac2d1ae53c824293f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411472"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a>Ячейка XRulerDensity (раздел "Линейка и сетка")

Определяет горизонтальные промежуточные деления линейки для страницы.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|нуль  <br/> |Фиксация  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |С большими интервалами  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |С обычными интервалами (по умолчанию)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |С небольшими интервалами  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Замечания

Эта ячейка соответствует параметру **Промежуточные деления по горизонтали** в диалоговом окне **Линейка и сетка** (на вкладке **Вид** нужно выбрать стрелку **Показать**). 
  
Чтобы получить ссылку на ячейку XRulerDensity по имени из другой формулы или из программы с помощью свойства **CellsU**, укажите следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |XRulerDensity  <br/> |
   
Чтобы получить ссылку на ячейку XRulerDensity по индексу из программы, укажите свойство **CellsSRC** с такими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visXRulerDensity** <br/> |
   

