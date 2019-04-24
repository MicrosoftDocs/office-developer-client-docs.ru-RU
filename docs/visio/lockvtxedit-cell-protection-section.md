---
title: LockVtxEdit Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
localization_priority: Normal
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: Блокирует вершины фигуры, чтобы их нельзя было редактировать.
ms.openlocfilehash: 1703769fe54171a14f7052f0f6686e1eb5ec92fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358060"
---
# <a name="lockvtxedit-cell-protection-section"></a>LockVtxEdit Cell (Protection Section)

Блокирует вершины фигуры, чтобы их нельзя было редактировать.
  
|**Value**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Вершины нельзя редактировать.  <br/> |
|FALSE  <br/> |Вершины можно редактировать.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LockVtxEdit по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |LockVtxEdit  <br/> |
   
Чтобы получить ссылку на ячейку LockVtxEdit по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровлокк** <br/> |
|Индекс ячейки:  <br/> |**Вислокквткседит** <br/> |
   

