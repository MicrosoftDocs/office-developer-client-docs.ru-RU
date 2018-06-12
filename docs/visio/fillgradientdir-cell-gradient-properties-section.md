---
title: Ячейка FillGradientDir (градиента Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Определяет направление градиентной заливки. Градиент линейно, Радиальное, прямоугольный, или выполните путь.
ms.openlocfilehash: 9b4226892e70fcffe7a78d109bd852e6d4f93838
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813753"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a>Ячейка FillGradientDir (градиента Properties Section)

Определяет направление градиентной заливки. Градиент линейно, Радиальное, прямоугольный, или выполните путь. 
  
> [!NOTE]
> Линейный градиент — это единственный градиент, который принимает значения дополнительных угол (в зависимости от **FillGradientDir** ячейки). Все другие градиента инструкции по панелям предварительно перечисления. 
  
****

|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Линейный градиент. Ячейка **FillGradientAngle** определяет направление градиента.  <br/> |
|1-7  <br/> |Радиальное градиентом. Градиента расширяет возможности outwards в круг из центральной точки.  <br/> |
|8-12  <br/> |Прямоугольный градиентом. Расширяет возможности градиента направления строке с происхождения с появления прямоугольной формы.  <br/> |
|13  <br/> |Градиентные путь.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **FillGradientDir** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | FillGradientDir  <br/> |
   
Для получения ссылки на ячейки **FillGradientDir** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowGradientProperties** <br/> |
| Индекс ячейки:  <br/> |**visFillGradientDir** <br/> |
   

