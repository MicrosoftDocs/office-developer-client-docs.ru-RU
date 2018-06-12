---
title: Ячейка YRulerDensity (линейки &amp; сетка)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Определяет вертикальные деления на линейке для страницы.
ms.openlocfilehash: 4b5dcba7a5cb1a588f742b1c2ea6b430cb2af12c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815222"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a>Ячейка YRulerDensity (линейки &amp; сетка)

Определяет вертикальные деления на линейке для страницы.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Предопределенная  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |Крупной  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Обычный (по умолчанию)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Оптимизация  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Замечания

В этой ячейке соответствует параметру вертикальной **подразделами** в **линейки &amp; сетки** диалоговое окно "" (на вкладке **Вид** щелкните стрелку **Показать** ). 
  
Чтобы получить ссылку на ячейку YRulerDensity по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |YRulerDensity  <br/> |
   
Для получения ссылки на ячейки YRulerDensity по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowRulerGrid** <br/> |
|Индекс ячейки:  <br/> |**visYRulerDensity** <br/> |
   

