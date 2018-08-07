---
title: Ячейка LocPinX (раздел "Преобразование фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
localization_priority: Normal
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: 'Представляет x-координата ПИН-код фигуры (центр вращения) относительно начала фигуры. Формула для расчета LocPinX — это:'
ms.openlocfilehash: 17f7b0fde9a54f6596f2f87f866d30b908e062b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814179"
---
# <a name="locpinx-cell-shape-transform-section"></a>Ячейка LocPinX (раздел "Преобразование фигуры")

Представляет *x* -координата ПИН-код фигуры (центр вращения) относительно начала фигуры. Формула для расчета LocPinX — это: 
  
= Ширина \* 0,5
  
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки LocPinX по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LocPinX  <br/> |
   
Для получения ссылки на ячейки LocPinX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowXFormOut** <br/> |
| Индекс ячейки:  <br/> |**visXFormLocPinX** <br/> |
   

