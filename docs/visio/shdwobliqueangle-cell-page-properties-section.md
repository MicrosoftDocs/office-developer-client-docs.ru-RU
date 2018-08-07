---
title: Ячейка ShdwObliqueAngle (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
localization_priority: Normal
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: Содержит номер, определяющий угол наклона при использовании типа тени по умолчанию.
ms.openlocfilehash: 4549ce7b5202b4649a925b04ea54c0d5df569599
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814851"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a>Ячейка ShdwObliqueAngle (раздел "Свойства страницы")

Содержит номер, определяющий угол наклона при использовании типа тени по умолчанию.
  
## <a name="remarks"></a>Замечания

Значение нуль (0) в этой ячейке указывает, что направление угол — вверх и измеряется стрелке.
  
 Угол, описанных в этой ячейке используется всякий раз, когда ShapeShdwType ячейки (тип тени для фигуры на странице) задано значение по умолчанию для страницы (**visFSTPageDefault** ), тип теневой наклон. Тип тени страницы по умолчанию определяется в ячейке ShdwType. 
  
Чтобы задать это поведение для отдельных фигуры, используйте ShapeShdwObliqueAngle ячейки в разделе формат заполните поля.
  
Чтобы получить ссылку на ячейку ShdwObliqueAngle по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | ShdwObliqueAngle  <br/> |
   
Для получения ссылки на ячейки ShdwObliqueAngle по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPage** <br/> |
| Индекс ячейки:  <br/> |**visPageShdwObliqueAngle** <br/> |
   

