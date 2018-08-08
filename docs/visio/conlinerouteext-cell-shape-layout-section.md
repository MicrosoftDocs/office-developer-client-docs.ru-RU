---
title: Ячейка ConLineRouteExt (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
localization_priority: Normal
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: Определяет внешний соединитель.
ms.openlocfilehash: 7724466b6ad225fcf39243bc80ba2e440f3b700b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813464"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a>Ячейка ConLineRouteExt (раздел "Макет фигуры")

Определяет внешний соединитель.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | По умолчанию; Использование параметров страницы  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Прямой  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Круглая  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку ConLineRouteExt по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | ConLineRouteExt  <br/> |
   
Для получения ссылки на ячейки ConLineRouteExt по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
| Индекс ячейки:  <br/> |**visSLOLineRouteExt** <br/> |
   

