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
description: Определяет направление прыжков строки на вертикальных динамических соединителях на странице рисования, для которой не применено локальное направление прыжка.
ms.openlocfilehash: 21ad1d95fd83780f31778dbc8bb70f9bdb4b922d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414678"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a>PageLineJumpDirY Cell (Page Layout Section)

Определяет направление прыжков строки на вертикальных динамических соединителях на странице рисования, для которой не применено локальное направление прыжка.
  
|**Значение**|**Направление перехода строки**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | По умолчанию; вверх или параметр страницы для фигур  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Left  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | Right  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку PageLineJumpDirY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | PageLineJumpDirY  <br/> |
   
Чтобы получить ссылку на ячейку PageLineJumpDirY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPageLayout** <br/> |
| Индекс ячейки:  <br/> |**visPLOJumpDirY** <br/> |
   

