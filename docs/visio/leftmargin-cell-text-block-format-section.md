---
title: LeftMargin Cell (Text Block Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251265
localization_priority: Normal
ms.assetid: 47d84d7d-08a0-1934-d156-702da848e01c
description: Определяет расстояние между левой границей текстового блока и текстом, который он содержит. По умолчанию — 0,1 дюйма. Это значение не зависит от масштаба рисунка. Если рисунок масштабировать, то левая маржа остается той же.
ms.openlocfilehash: fee8eca8b5730e40518babe0c76549e10bebd902
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411339"
---
# <a name="leftmargin-cell-text-block-format-section"></a>LeftMargin Cell (Text Block Format Section)

Определяет расстояние между левой границей текстового блока и текстом, который он содержит. По умолчанию — 0,1 дюйма. Это значение не зависит от масштаба рисунка. Если рисунок масштабировать, то левая маржа остается той же.
  
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку LeftMargin по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | LeftMargin  <br/> |
   
Чтобы получить ссылку на ячейку LeftMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowText** <br/> |
| Индекс ячейки:  <br/> |**visTxtBlkLeftMargin** <br/> |
   

