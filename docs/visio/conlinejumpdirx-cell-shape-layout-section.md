---
title: ConLineJumpDirX Cell (Shape Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Определяет направление пересечения линий при пересечении горизонтальной динамической соединительной линии для фигуры.
ms.openlocfilehash: 22b9366b750a85a76498b83880aac2b9b974e1ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415042"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a>ConLineJumpDirX Cell (Shape Layout Section)

Определяет направление пересечения линий при пересечении горизонтальной динамической соединительной линии для фигуры.
  
|**Значение**|**Направление пересечения линий**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | Страница по умолчанию  <br/> |**Висложумпдирксдефаулт** <br/> |
| 1,1  <br/> | Настройка  <br/> |**Висложумпдирксуп** <br/> |
| 2  <br/> | Понижен  <br/> |**Висложумпдирксдовн** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы задать горизонтальное направление по умолчанию для *всех* переходов между соединителями на странице, используйте ячейку PageLineJumpDirX в разделе Макет страницы. 
  
Чтобы получить ссылку на ячейку ConLineJumpDirX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | ConLineJumpDirX  <br/> |
   
Чтобы получить ссылку на ячейку ConLineJumpDirX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**Висровшапелайаут** <br/> |
| Индекс ячейки:  <br/> |**Виссложумпдиркс** <br/> |
   

