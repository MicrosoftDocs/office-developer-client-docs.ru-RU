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
ms.openlocfilehash: 633b2e54ca77216fd20ead00f047283c54f8164d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815190"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a>Ячейка XRulerDensity (раздел "Линейка и сетка")

Определяет горизонтальные промежуточные деления линейки для страницы.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Фиксация  <br/> |**visRulerFixed** <br/> |
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
   

