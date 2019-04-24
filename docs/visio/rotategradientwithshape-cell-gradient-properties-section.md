---
title: RotateGradientWithShape Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Определяет, вращается ли Градиентная заливка с фигурой в двухмерном повороте в виде логического значения.
ms.openlocfilehash: 76a76a4a97128c81710269f75e9e17db90827377
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315661"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a>RotateGradientWithShape Cell (Gradient Properties Section)

Определяет, вращается ли Градиентная заливка с фигурой в двухмерном повороте в виде логического значения.
  
|**Value**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Градиент поворачивается вместе с фигурой, когда фигура поворачивается вокруг ПИН-кода вращения. "Top" градиента параллельно с маркером вращения.  <br/> |
|FALSE  <br/> |Градиент не поворачивается вместе с фигурой, когда фигура вращается вокруг ПИН-кода вращения. "Top" градиента параллельно с полотном.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку **RotateGradientWithShape** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | RotateGradientWithShape  <br/> |
   
Чтобы получить ссылку на ячейку **RotateGradientWithShape** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровградиентпропертиес** <br/> |
| Индекс ячейки:  <br/> |**Висротатеградиентвисшапе** <br/> |
   

