---
title: PageLineJumpDirY Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm770
localization_priority: Normal
ms.assetid: f73cc157-b332-279b-f7cf-d5a090bc09a4
description: Определяет направление значков пересечения линий на вертикальных динамических соединителях на странице документа, для которых вы не применили локальное направление перехода.
ms.openlocfilehash: 21ad1d95fd83780f31778dbc8bb70f9bdb4b922d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329899"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a>PageLineJumpDirY Cell (Page Layout Section)

Определяет направление значков пересечения линий на вертикальных динамических соединителях на странице документа, для которых вы не применили локальное направление перехода.
  
|**Значение**|**Направление пересечения линий**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | Умолчани или параметры страницы для фигур  <br/> |**Висложумпдиридефаулт** <br/> |
| 1,1  <br/> | Left  <br/> |**Висложумпдирилефт** <br/> |
| 2  <br/> | Right  <br/> |**Висложумпдириригхт** <br/> |
   
## <a name="remarks"></a>Комментарии

Чтобы получить ссылку на ячейку PageLineJumpDirY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PageLineJumpDirY  <br/> |
   
Чтобы получить ссылку на ячейку PageLineJumpDirY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровпажелайаут** <br/> |
| Индекс ячейки:  <br/> |**Виспложумпдири** <br/> |
   

