---
title: Ячейка LineGradientEnabled (раздел "Свойства градиента")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: Определяет, включена ли градиент строки для линии или границы фигуры.
ms.openlocfilehash: d78a94a25c0290bd5e58522c9a45955868f31b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814070"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a>Ячейка LineGradientEnabled (раздел "Свойства градиента")

Определяет, включена ли градиент строки для линии или границы фигуры. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Градиентные отображается в строке или границы фигуры.  <br/> |
|FALSE  <br/> |Градиентом, не отображаются в строке или границы фигуры.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **LineGradientEnabled** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LineGradientEnabled  <br/> |
   
Для получения ссылки на ячейки **LineGradientEnabled** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowGradientProperties** <br/> |
| Индекс ячейки:  <br/> |**visLineGradientEnabled** <br/> |
   

