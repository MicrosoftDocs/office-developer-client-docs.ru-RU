---
title: ConLineRouteExt Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
localization_priority: Normal
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: Определяет внешний вид соединитетеля.
ms.openlocfilehash: 19fe948daf7aa3d67db858849ecb2b15f40ba02d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434615"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a>ConLineRouteExt Cell (Shape Layout Section)

Определяет внешний вид соединитетеля.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | По умолчанию; использование параметра страницы  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Прямая  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Изогнутый  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку ConLineRouteExt по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ConLineRouteExt  <br/> |
   
Чтобы получить ссылку на ячейку ConLineRouteExt по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
| Индекс ячейки:  <br/> |**visSLOLineRouteExt** <br/> |
   

