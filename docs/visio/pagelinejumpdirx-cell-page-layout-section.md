---
title: Ячейка PageLineJumpDirX (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
localization_priority: Normal
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: Определяет направление строки пересечения на горизонтальную динамических соединители на странице документа, для которого не применяются локальные направление.
ms.openlocfilehash: d414313e98107790f9236c0afabdc5747c6a2a10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814338"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a>Ячейка PageLineJumpDirX (раздел "Макет страницы")

Определяет направление строки пересечения на горизонтальную динамических соединители на странице документа, для которого не применяются локальные направление.
  
|**Значение**|**Направление**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | По умолчанию; слева или параметров страницы для фигур  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Вверх   <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | Вниз  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку PageLineJumpDirX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | PageLineJumpDirX  <br/> |
   
Для получения ссылки на ячейки PageLineJumpDirX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPageLayout** <br/> |
| Индекс ячейки:  <br/> |**visPLOJumpDirX** <br/> |
   

