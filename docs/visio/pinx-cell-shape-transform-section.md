---
title: Ячейка PinX (раздел "Преобразование фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm790
localization_priority: Normal
ms.assetid: dd88fb8d-3ec3-476a-870d-6642b191496f
description: Представляет x-координата ПИН-код фигуры (центр вращения) относительно начала родительского элемента.
ms.openlocfilehash: 74e98732f1e0c44fa20c159070198ed4f98cee92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19814360"
---
# <a name="pinx-cell-shape-transform-section"></a>Ячейка PinX (раздел "Преобразование фигуры")

Представляет *x* -координата ПИН-код фигуры (центр вращения) относительно начала родительского элемента. 
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку PinX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | PinX  <br/> |
   
Для получения ссылки на ячейки PinX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowXFormOut** <br/> |
| Индекс ячейки:  <br/> |**visXFormPinX** <br/> |
   

