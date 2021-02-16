---
title: NoAlignBox Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm700
localization_priority: Normal
ms.assetid: b2d51f4b-d64e-fd14-4ff1-ed67c69213bc
description: Включает и выключает отображение прямоугольника выбора для выбранной фигуры.
ms.openlocfilehash: 2ff9f051df54f4d424589332b9fbaea973552edc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435882"
---
# <a name="noalignbox-cell-miscellaneous-section"></a>NoAlignBox Cell (Miscellaneous Section)

Включает и выключает отображение прямоугольника выбора для выбранной фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Прямоугольник выделения не отображается при выборе фигуры.  <br/> |
| FALSE  <br/> | Прямоугольник выделения отображается при выборе фигуры.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку NoAlignBox по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | NoAlignBox  <br/> |
   
Чтобы получить ссылку на ячейку NoAlignBox по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visNoAlignBox** <br/> |
   

