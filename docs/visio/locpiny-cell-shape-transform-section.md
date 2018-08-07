---
title: Ячейка LocPinY (раздел "Преобразование фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
localization_priority: Normal
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 'Представляет y-координата ПИН-код фигуры (центр вращения) относительно начала фигуры. Формула для расчета LocPinX — это:'
ms.openlocfilehash: 8d98906e8082af0fc54bc01fe3a8537b66ac56b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814166"
---
# <a name="locpiny-cell-shape-transform-section"></a>Ячейка LocPinY (раздел "Преобразование фигуры")

Представляет *y* -координата ПИН-код фигуры (центр вращения) относительно начала фигуры. Формула для расчета LocPinX — это: 
  
= Высота \* 0,5
  
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку LocPinY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | LocPinY  <br/> |
   
Для получения ссылки на ячейки LocPinY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowXFormOut** <br/> |
| Индекс ячейки:  <br/> |**visXFormLocPinY** <br/> |
   

