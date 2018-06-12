---
title: Ячейка LineGradientDir (градиента Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Определяет направление градиента строки. Градиент линейно, Радиальное, прямоугольный, или выполните путь.
ms.openlocfilehash: 6243d7a6b470db0915ba6fc462f05b72a9814f66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814089"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a>Ячейка LineGradientDir (градиента Properties Section)

Определяет направление градиента строки. Градиент линейно, Радиальное, прямоугольный, или выполните путь. 
  
> [!NOTE]
> Линейный градиент — это единственный градиент, который принимает значения дополнительных угол (в зависимости от **LineGradientDir** ячейки). Все другие градиента инструкции по панелям предварительно перечисления. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Линейный градиент. Ячейка **LineGradientAngle** определяет направление градиента.  <br/> |
|1-7  <br/> |Радиальное градиентом. Градиента расширяет возможности outwards в круг из центральной точки.  <br/> |
|8-12  <br/> |Прямоугольный градиентом. Расширяет возможности градиента направления строке с происхождения с появления прямоугольной формы.  <br/> |
|13  <br/> |Градиентные путь.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **LineGradientDir** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LineGradientDir  <br/> |
   
Для получения ссылки на ячейки **LineGradientDir** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowGradientProperties** <br/> |
| Индекс ячейки:  <br/> |**visLineGradientDir** <br/> |
   

