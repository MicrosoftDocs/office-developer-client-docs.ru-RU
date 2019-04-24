---
title: CompoundType Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Определяет составной тип линии фигуры.
ms.openlocfilehash: 120975e419656234266cb8151b2fa37ef19602e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359374"
---
# <a name="compoundtype-cell-line-format-section"></a>CompoundType Cell (Line Format Section)

Определяет составной тип линии фигуры. 
  
|**Value**|**Описание**|
|:-----|:-----|
|нуль  <br/> |Simple (Простая)  <br/> |
|1,1  <br/> |Двойное с плавающей точкой  <br/> |
|2  <br/> |Толстая тонкая  <br/> |
|4  <br/> |Тонкие плотности  <br/> |
|SP4  <br/> |Triple  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **CompoundType** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | CompoundType  <br/> |
   
Чтобы получить ссылку на ячейку **CompoundType** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровлине** <br/> |
| Индекс ячейки:  <br/> |**Вискомпаундтипе** <br/> |
   

