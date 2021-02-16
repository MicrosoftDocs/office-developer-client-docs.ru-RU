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
description: Определяет, перемещаются ли перемещаемые фигуры, а соединители перенадвигаются вокруг других фигур и соединители на странице рисования.
ms.openlocfilehash: d1075ab1b0512d5db1c7b7a5f2895305318dae7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437478"
---
# <a name="dynamicsoff-cell-page-layout-section"></a>DynamicsOff Cell (Page Layout Section)

Определяет, перемещаются ли перемещаемые фигуры, а соединители перенадвигаются вокруг других фигур и соединители на странице рисования.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Отключать динамику.  <br/> |
| FALSE  <br/> | Включить динамику.  <br/> |
   
## <a name="remarks"></a>Примечания

Вы можете отключить динамику, чтобы повысить производительность решения. Например, если ваше решение добавляет в рисунок местоимяемые фигуры и вы не хотите, чтобы приложение перенанимал соединители и менял положение фигур при каждом добавлении фигуры, вы можете отключить динамику. После того как ваше решение добавит фигуры, повторно в включить динамику.
  
Чтобы получить ссылку на ячейку DynamicsOff по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | DynamicsOff  <br/> |
   
Чтобы получить ссылку на ячейку DynamicsOff по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPageLayout** <br/> |
| Индекс ячейки:  <br/> |**visPLODynamicsOff** <br/> |
   

