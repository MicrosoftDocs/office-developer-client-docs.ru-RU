---
title: Ячейка BeginArrowSize (раздел "Формат линий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251629
localization_priority: Normal
ms.assetid: bfddb829-6e13-7d74-b9b9-2cb5c0937bae
description: Определяет размер стрелки в начале строки.
ms.openlocfilehash: b38e4a0685fce6d7f4aea2192ed123665eacf40a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813173"
---
# <a name="beginarrowsize-cell-line-format-section"></a>Ячейка BeginArrowSize (раздел "Формат линий")

Определяет размер стрелки в начале строки.
  
|**Значение**|**Size**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Очень маленькие  <br/> |**visArrowSizeVerySmall** <br/> |
| 1  <br/> | Малый  <br/> |**visArrowSizeSmall** <br/> |
| 2  <br/> | Средний  <br/> |**visArrowSizeMedium** <br/> |
| 3  <br/> | Большая  <br/> |**visArrowSizeLarge** <br/> |
| 4  <br/> | Очень большие  <br/> |**visArrowSizeVeryLarge** <br/> |
| 5  <br/> | Большие  <br/> |**visArrowSizeJumbo** <br/> |
| 6  <br/> | Колоссальных  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Замечания

Также можно задать размер стрелки в диалоговом окне **строки** . 
  
Чтобы получить ссылку на ячейку BeginArrowSize по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | BeginArrowSize  <br/> |
   
Для получения ссылки на ячейки BeginArrowSize по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLine** <br/> |
| Индекс ячейки:  <br/> |**visLineBeginArrowSize** <br/> |
   

