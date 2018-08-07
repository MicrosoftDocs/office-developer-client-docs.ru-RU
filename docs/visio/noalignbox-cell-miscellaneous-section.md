---
title: Ячейка NoAlignBox (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm700
localization_priority: Normal
ms.assetid: b2d51f4b-d64e-fd14-4ff1-ed67c69213bc
description: Включает или отключает отображение прямоугольник выделения и отключает для выбранной фигуры.
ms.openlocfilehash: c8e5fe28197a72b4cdb5306732dd155dc8f4f810
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814293"
---
# <a name="noalignbox-cell-miscellaneous-section"></a>Ячейка NoAlignBox (раздел "Прочее")

Включает или отключает отображение прямоугольник выделения и отключает для выбранной фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Прямоугольник выделения не отображаются при выборе фигуры.  <br/> |
| FALSE  <br/> | Прямоугольник выделения отображается при выборе фигуры.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку NoAlignBox по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | NoAlignBox  <br/> |
   
Для получения ссылки на ячейки NoAlignBox по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visNoAlignBox** <br/> |
   

