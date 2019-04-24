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
description: Определяет внешний вид по умолчанию для всех соединителей на странице документа.
ms.openlocfilehash: 6daed2e06f7673e5a4ec97ec83dc31bad2766301
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358984"
---
# <a name="linerouteext-cell-page-layout-section"></a>LineRouteExt Cell (Page Layout Section)

Определяет внешний вид по умолчанию для всех соединителей на странице документа.
  
|**Value**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | По умолчанию (прямолинейный)  <br/> |**Вислораутикстдефаулт** <br/> |
| 1,1  <br/> | Располагает  <br/> |**Вислораутикстстраигхт** <br/> |
| 2  <br/> | Прямолинейны  <br/> |**Вислораутикстнурбс** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LineRouteExt по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LineRouteExt  <br/> |
   
Чтобы получить ссылку на ячейку LineRouteExt по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровпажелайаут** <br/> |
| Индекс ячейки:  <br/> |**Висплолинераутикст** <br/> |
   

