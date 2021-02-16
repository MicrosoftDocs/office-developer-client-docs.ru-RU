---
title: RotateGradientWithShape Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Определяет, вращается ли градиент заливки фигурой в 2D-повороте в виде boolean.
ms.openlocfilehash: 76a76a4a97128c81710269f75e9e17db90827377
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412221"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a>RotateGradientWithShape Cell (Gradient Properties Section)

Определяет, вращается ли градиент заливки фигурой в 2D-повороте в виде boolean.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Градиент поворачивается вместе с фигурой при повороте фигуры вокруг закрепления поворота. "Верхняя" часть градиента является параллельной вращаемой ладе.  <br/> |
|FALSE  <br/> |Градиент не поворачивается вместе с фигурой при повороте фигуры вокруг закрепления поворота. "Верхняя" часть градиента является параллельно полотну.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку **RotateGradientWithShape** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | RotateGradientWithShape  <br/> |
   
Чтобы получить ссылку на ячейку **RotateGradientWithShape** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowGradientProperties** <br/> |
| Индекс ячейки:  <br/> |**visRotateGradientWithShape** <br/> |
   

