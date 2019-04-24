---
title: Can Glue Cell (Controls Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
localization_priority: Normal
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: Определяет, можно ли приклеить управляющий маркер к другим фигурам.
ms.openlocfilehash: 2f5e65ab72c584f88b56e273b0d73abf969a6588
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337256"
---
# <a name="can-glue-cell-controls-section"></a>Can Glue Cell (Controls Section)

Определяет, можно ли приклеить управляющий маркер к другим фигурам.
  
|**Value**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Управляющий маркер можно приклеить.  <br/> |
| FALSE  <br/> | Управляющий маркер невозможно приклеить.  <br/> |
   
## <a name="remarks"></a>Комментарии

Чтобы получить ссылку на ячейку можно склеить по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Controls.  *Name (имя* ). Элементы управления Канглуевхере.  *имя* — название строки элементов управления.  <br/> |
   
Чтобы получить ссылку на ячейку можно склеить по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionControls** <br/> |
| Индекс строки:  <br/> |**висровконтрол** +  *i* , где *i* = 0, 1, 2,...  <br/> |
| Индекс ячейки:  <br/> |**Висктлглуе** <br/> |
   

