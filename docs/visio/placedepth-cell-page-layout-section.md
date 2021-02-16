---
title: PlaceDepth Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1230
localization_priority: Normal
ms.assetid: 02c139db-fe67-f550-1d07-8c8a9a4fb427
description: Определяет метод, с помощью которого анализировался рисунок перед созданием макета, и определяет тип макета.
ms.openlocfilehash: 463c7dad39955161538aa89d1482685189bf7fdc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432039"
---
# <a name="placedepth-cell-page-layout-section"></a>PlaceDepth Cell (Page Layout Section)

Определяет метод, с помощью которого анализировался рисунок перед созданием макета, и определяет тип макета.
  
|**Значение**|**Глубина размещения для вертикальных и горизонтальных макетов**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Страница по умолчанию  <br/> |**visPLOPlaceDepthDefault** <br/> |
| 1   <br/> | Средняя  <br/> |**visPLOPlaceDepthMedium** <br/> |
| 2   <br/> | Deep  <br/> |**visPLOPlaceDepthDeep** <br/> |
| 3   <br/> | Поверхностное  <br/> |**visPLOPlaceDepthShallow** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку PlaceDepth по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PlaceDepth  <br/> |
   
Чтобы получить ссылку на ячейку PlaceDepth по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPageLayout** <br/> |
| Индекс ячейки:  <br/> |**visPLOPlaceDepth** <br/> |
   

