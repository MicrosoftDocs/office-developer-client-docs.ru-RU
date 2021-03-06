---
title: Position Cell (Tabs Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: Указывает положение остановки вкладки. Положение вкладки не зависит от масштаба рисунка. Если рисунок масштабировать, положение вкладки остается таким же.
ms.openlocfilehash: ef17b38d708103ca004594ba04ff5b8d1ada13bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409932"
---
# <a name="position-cell-tabs-section"></a>Position Cell (Tabs Section)

Указывает положение остановки вкладки. Положение вкладки не зависит от масштаба рисунка. Если рисунок масштабировать, положение вкладки остается таким же.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Position по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Вкладки.  *ij,*            *где i*  и  *j*  = <1>, 2, 3...  <br/> |
   
Чтобы получить ссылку на ячейку Position по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionTab** <br/> |
| Индекс строки:  <br/> |**visRowTab**  +   *i,* *где i* = 0, 1, 2 ...  <br/> |
| Индекс ячейки:  <br/> | (*j*  *3) + **visTabPos** <br/> |
   

