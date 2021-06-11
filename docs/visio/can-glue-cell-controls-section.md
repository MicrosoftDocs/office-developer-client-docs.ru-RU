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
description: Определяет, можно ли приклеить ручку управления к другим фигурам.
ms.openlocfilehash: 2f5e65ab72c584f88b56e273b0d73abf969a6588
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423295"
---
# <a name="can-glue-cell-controls-section"></a>Can Glue Cell (Controls Section)

Определяет, можно ли приклеить ручку управления к другим фигурам.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Ручку управления можно приклеить.  <br/> |
| FALSE  <br/> | Ручка управления не может быть приклеена.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Can Glue по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Controls.  *имя*  . Элементы управления CanGluewhere.  *имя* — название строки элементов управления.  <br/> |
   
Чтобы получить ссылку на ячейку Can Glue по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionControls** <br/> |
| Индекс строки:  <br/> |**visRowControl**  +   *i,* *где i* = 0, 1, 2, ...  <br/> |
| Индекс ячейки:  <br/> |**visCtlGlue** <br/> |
   

