---
title: Ячейка NoLine (раздел "Геометрия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm715
localization_priority: Normal
ms.assetid: f9624af2-c087-3dde-9140-339c438b3652
description: Определяет, будет ли линия вокруг границ пути.
ms.openlocfilehash: 1e43072363461e6b8fcd511c70512f3bfef4504f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814295"
---
# <a name="noline-cell-geometry-section"></a>Ячейка NoLine (раздел "Геометрия")

Определяет, будет ли линия вокруг границ пути.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Вокруг границ пути, который является границ заполненной области строки не отображается.  <br/> |
| FALSE  <br/> | Линия вокруг границы пути.  <br/> |
   
## <a name="remarks"></a>Замечания

При изменении цвета линии Технический строка по-прежнему существует, даже если вы не видите на белым фоном. При установке значения ячейки имеет значение TRUE, строка не отображается.
  
Чтобы получить ссылку на ячейку NoLine по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Геометрия *i* . NoLine где *i* = < 1 > 2, 3...  <br/> |
   
Для получения ссылки на ячейки NoLine по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...  <br/> |
| Индекс строки:  <br/> |**visRowComponent** <br/> |
| Индекс ячейки:  <br/> |**visCompNoLine** <br/> |
   

