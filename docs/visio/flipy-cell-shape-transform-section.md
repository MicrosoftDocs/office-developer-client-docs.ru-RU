---
title: FlipY Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251198
localization_priority: Normal
ms.assetid: 062022ff-e243-2540-becd-d9b969ce83ce
description: Указывает, была ли фигура перевернута вертикально.
ms.openlocfilehash: 44ea0341cda3655e8acc69e82e89acddac69b80d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417450"
---
# <a name="flipy-cell-shape-transform-section"></a>FlipY Cell (Shape Transform Section)

Указывает, была ли фигура перевернута вертикально.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Фигура перевернута вертикально.  <br/> |
| FALSE  <br/> | Фигура не перевернута вертикально.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку FlipY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | FlipY  <br/> |
   
Чтобы получить ссылку на ячейку FlipY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowXFormOut** <br/> |
| Индекс ячейки:  <br/> |**visXFormFlipY** <br/> |
   

