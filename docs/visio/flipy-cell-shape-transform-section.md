---
title: Ячейка FlipY (раздел "Преобразование фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251198
localization_priority: Normal
ms.assetid: 062022ff-e243-2540-becd-d9b969ce83ce
description: Указывает, является ли фигура отразилось по вертикали.
ms.openlocfilehash: 42ee740a13c3f447f5cd4a6caa9959189320a8af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813775"
---
# <a name="flipy-cell-shape-transform-section"></a>Ячейка FlipY (раздел "Преобразование фигуры")

Указывает, является ли фигура отразилось по вертикали.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Фигура отразилось по вертикали.  <br/> |
| FALSE  <br/> | Фигура не отразилось по вертикали.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку FlipY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | FlipY  <br/> |
   
Для получения ссылки на ячейки FlipY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowXFormOut** <br/> |
| Индекс ячейки:  <br/> |**visXFormFlipY** <br/> |
   

