---
title: FillGradientEnabled Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: Определяет, включен ли градиент заливки для этой фигуры.
ms.openlocfilehash: 17f617c13b632318be22b86a3354a194f0f835f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431213"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a>FillGradientEnabled Cell (Gradient Properties Section)

Определяет, включен ли градиент заливки для этой фигуры. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Заливка градиента отображается на фигуре.  <br/> |
|FALSE  <br/> |Заливки градиента не отображаются на фигуре.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **FillGradientEnabled** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | FillGradientEnabled  <br/> |
   
Чтобы получить ссылку на ячейку **FillGradientEnabled** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowGradientProperties** <br/> |
| Индекс ячейки:  <br/> |**visFillGradientEnabled ** <br/> |
   

