---
title: LineRouteExt Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
localization_priority: Normal
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: Определяет внешний вид по умолчанию для всех соединители на странице рисования.
ms.openlocfilehash: 6daed2e06f7673e5a4ec97ec83dc31bad2766301
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410625"
---
# <a name="linerouteext-cell-page-layout-section"></a>LineRouteExt Cell (Page Layout Section)

Определяет внешний вид по умолчанию для всех соединители на странице рисования.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | По умолчанию (прямо)  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Прямая  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Изогнутый  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LineRouteExt по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LineRouteExt  <br/> |
   
Чтобы получить ссылку на ячейку LineRouteExt по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPageLayout** <br/> |
| Индекс ячейки:  <br/> |**visPLOLineRouteExt** <br/> |
   

