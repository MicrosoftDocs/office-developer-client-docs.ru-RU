---
title: Ячейка XRulerDensity (линейки &amp; сетка)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Задает горизонтальную деления на линейке для страницы.
ms.openlocfilehash: 633b2e54ca77216fd20ead00f047283c54f8164d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815190"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a>Ячейка XRulerDensity (линейки &amp; сетка)

Задает горизонтальную деления на линейке для страницы.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Предопределенная  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |Крупной  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Обычный (по умолчанию)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Оптимизация  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Замечания

В этой ячейке соответствует параметру горизонтальной **подразделами** в **линейки &amp; сетки** диалоговое окно "" (на вкладке **Вид** щелкните стрелку **Показать** ). 
  
Чтобы получить ссылку на ячейку XRulerDensity по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |XRulerDensity  <br/> |
   
Для получения ссылки на ячейки XRulerDensity по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visXRulerDensity** <br/> |
   

