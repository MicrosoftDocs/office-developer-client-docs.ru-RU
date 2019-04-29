---
title: DynamicsOff Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251641
localization_priority: Normal
ms.assetid: 055764aa-9681-ffb0-83ce-fdd612fe37af
description: Определяет, перемещаются ли размещаемые фигуры, а соединители перенаправляются по другим фигурам и соединительным линиям на странице документа.
ms.openlocfilehash: d1075ab1b0512d5db1c7b7a5f2895305318dae7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437478"
---
# <a name="dynamicsoff-cell-page-layout-section"></a>DynamicsOff Cell (Page Layout Section)

Определяет, перемещаются ли размещаемые фигуры, а соединители перенаправляются по другим фигурам и соединительным линиям на странице документа.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Отключить Dynamics.  <br/> |
| FALSE  <br/> | Включение Dynamics.  <br/> |
   
## <a name="remarks"></a>Примечания

Вы можете отключить Dynamics, чтобы увеличить производительность решения. Например, если ваше решение добавляет размещаемые фигуры в документ и вы не хотите, чтобы приложение перенаправляло соединители и изменить положение фигур каждый раз при добавлении фигуры, можно отключить Dynamics. После того как решение добавит фигуры, повторно включите Dynamics.
  
Чтобы получить ссылку на ячейку DynamicsOff по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | DynamicsOff  <br/> |
   
Чтобы получить ссылку на ячейку DynamicsOff по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровпажелайаут** <br/> |
| Индекс ячейки:  <br/> |**Висплодинамиксофф** <br/> |
   

