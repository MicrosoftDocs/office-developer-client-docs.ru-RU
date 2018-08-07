---
title: Ячейка PlaceDepth (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1230
localization_priority: Normal
ms.assetid: 02c139db-fe67-f550-1d07-8c8a9a4fb427
description: Определяет способ, с помощью которого выполняется анализ перед созданием макет документа и определяет тип макета.
ms.openlocfilehash: ab2c83a94c3dd03c1fdbf0c3ee187076406b2e84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814362"
---
# <a name="placedepth-cell-page-layout-section"></a>Ячейка PlaceDepth (раздел "Макет страницы")

Определяет способ, с помощью которого выполняется анализ перед созданием макет документа и определяет тип макета.
  
|**Значение**|**Размещение глубины вертикальных и горизонтальных макетов страниц**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Страница по умолчанию  <br/> |**visPLOPlaceDepthDefault** <br/> |
| 1  <br/> | Средний  <br/> |**visPLOPlaceDepthMedium** <br/> |
| 2  <br/> | Глубокое  <br/> |**visPLOPlaceDepthDeep** <br/> |
| 3  <br/> | Неполная  <br/> |**visPLOPlaceDepthShallow** <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку PlaceDepth по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | PlaceDepth  <br/> |
   
Для получения ссылки на ячейки PlaceDepth по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPageLayout** <br/> |
| Индекс ячейки:  <br/> |**visPLOPlaceDepth** <br/> |
   

