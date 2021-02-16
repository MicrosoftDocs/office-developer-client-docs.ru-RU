---
title: BeginArrowSize Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251629
localization_priority: Normal
ms.assetid: bfddb829-6e13-7d74-b9b9-2cb5c0937bae
description: Определяет размер наконечник в начале строки.
ms.openlocfilehash: 9c1288ced747c4e16090013cc043b040f1fbb59c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412284"
---
# <a name="beginarrowsize-cell-line-format-section"></a>BeginArrowSize Cell (Line Format Section)

Определяет размер наконечник в начале строки.
  
|**Значение**|**Размер**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Очень маленький  <br/> |**visArrowSizeVerySmall** <br/> |
| 1   <br/> | Малый  <br/> |**visArrowSizeSmall** <br/> |
| 2   <br/> | Средняя  <br/> |**visArrowSizeMedium** <br/> |
| 3   <br/> | Крупный  <br/> |**visArrowSizeLarge** <br/> |
| 4   <br/> | Очень большой  <br/> |**visArrowSizeVeryLarge** <br/> |
| 5   <br/> | Jumbo  <br/> |**visArrowSizeJumbo** <br/> |
| 6   <br/> | Colossal  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить размер наконечники в диалоговом окне **"Линия".** 
  
Чтобы получить ссылку на ячейку BeginArrowSize по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | BeginArrowSize  <br/> |
   
Чтобы получить ссылку на ячейку BeginArrowSize по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowLine** <br/> |
| Индекс ячейки:  <br/> |**visLineBeginArrowSize** <br/> |
   

