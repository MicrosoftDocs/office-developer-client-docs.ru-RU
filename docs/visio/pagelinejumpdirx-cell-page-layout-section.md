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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431010"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a>PageLineJumpDirX Cell (Page Layout Section)

Определяет направление пересечения линий на горизонтальных динамических соединительных линиях на странице документа, для которых вы не применили локальное направление перехода.
  
|**Значение**|**Направление пересечения линий**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | Умолчани слева или параметры страницы для фигур  <br/> |**висложумпдирксдефаулт** <br/> |
| 1,1  <br/> | Настройка  <br/> |**висложумпдирксуп** <br/> |
| 2  <br/> | Понижен  <br/> |**висложумпдирксдовн** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку PageLineJumpDirX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PageLineJumpDirX  <br/> |
   
Чтобы получить ссылку на ячейку PageLineJumpDirX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**висровпажелайаут** <br/> |
| Индекс ячейки:  <br/> |**виспложумпдиркс** <br/> |
   

