---
title: Ячейка Width (раздел "Преобразование фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
localization_priority: Normal
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: 'Содержит ширину выбранной фигуры в единицах документа. Формула для определения ширины одномерной фигуры — это:'
ms.openlocfilehash: 55e77c5ccfca2425a8a2985564448e0f656aebbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815163"
---
# <a name="width-cell-shape-transform-section"></a>Ячейка Width (раздел "Преобразование фигуры")

Содержит ширину выбранной фигуры в единицах документа. Формула для определения ширины одномерной фигуры — это:
  
= КОРЕНЬ ((EndX-BeginX) ^ 2 + (КонецY - НачалоY) ^ 2)
  
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки ширины по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Width  <br/> |
   
Для получения ссылки на ячейки ширины по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowXFormOut** <br/> |
| Индекс ячейки:  <br/> |**visXFormWidth** <br/> |
   

