---
title: Action Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
localization_priority: Normal
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: Содержит формулу, которая будет выполняться, когда пользователь выбирает команду в меню ярлыка или тега действий.
ms.openlocfilehash: e6bc576982cad871804cbcbc5f3d9c6bceb558c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407615"
---
# <a name="action-cell-actions-section"></a>Action Cell (Actions Section)

Содержит формулу, которая будет выполняться, когда пользователь выбирает команду в меню ярлыка или тега действий.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
## <a name="remarks"></a>Замечания

Ячейка Action оценивается только при действии, а не при вступив в формулу.
  
Чтобы получить ссылку на ячейку Action по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Действия.  *имя*  . Действие, в котором действия. *имя*  — это имя строки действий  <br/> |
   
Чтобы получить ссылку на ячейку Action по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionAction** <br/> |
| Индекс строки:  <br/> |**visRowAction**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> |**visActionAction** <br/> |
   

