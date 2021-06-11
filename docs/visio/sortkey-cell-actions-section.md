---
title: SortKey Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027286
localization_priority: Normal
ms.assetid: c0c4b668-f31b-336f-4434-e94a4804ff7c
description: Номер, определяя порядок действий, которые отображаются в меню ярлыков или тегов действий.
ms.openlocfilehash: d4eb98055f199f603003b068dca9fa7b4e377e52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419662"
---
# <a name="sortkey-cell-actions-section"></a>SortKey Cell (Actions Section)

Номер, определяя порядок действий, которые отображаются в меню ярлыков или тегов действий.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
## <a name="remarks"></a>Замечания

Действия в теге действия или меню ярлыка отображаются в меню, отсортировали от самого низкого до самого высокого, а в верхней части меню отображаются более низкие числа. Если два ряда действий имеют одно и то же значение ячейки SortKey, порядок определяется физическим порядком строки. По умолчанию значение 0 (ноль).
  
Чтобы получить ссылку на ячейку SortKey по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Действия. *имя*  . SortKeywhere Actions.  *имя*  — это имя строки Действия  <br/> |
   
Чтобы получить ссылку на ячейку SortKey по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionAction** <br/> |
|Индекс строки:  <br/> |**visRowAction**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
|Индекс ячейки:  <br/> |**visActionSortKey** <br/> |
   

