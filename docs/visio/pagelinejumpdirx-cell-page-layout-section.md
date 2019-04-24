---
title: PageLineJumpDirX Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
localization_priority: Normal
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: Определяет направление пересечения линий на горизонтальных динамических соединительных линиях на странице документа, для которых вы не применили локальное направление перехода.
ms.openlocfilehash: 4e1213990877e1260cc8cecd5a55beda4592a844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283739"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a>PageLineJumpDirX Cell (Page Layout Section)

Определяет направление пересечения линий на горизонтальных динамических соединительных линиях на странице документа, для которых вы не применили локальное направление перехода.
  
|**Значение**|**Направление пересечения линий**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | Умолчани слева или параметры страницы для фигур  <br/> |**Висложумпдирксдефаулт** <br/> |
| 1,1  <br/> | Настройка  <br/> |**Висложумпдирксуп** <br/> |
| 2  <br/> | Понижен  <br/> |**Висложумпдирксдовн** <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку PageLineJumpDirX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PageLineJumpDirX  <br/> |
   
Чтобы получить ссылку на ячейку PageLineJumpDirX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровпажелайаут** <br/> |
| Индекс ячейки:  <br/> |**Виспложумпдиркс** <br/> |
   

