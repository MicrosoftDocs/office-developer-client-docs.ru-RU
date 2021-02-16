---
title: RightMargin Cell (Text Block Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
localization_priority: Normal
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: Определяет расстояние между правой границей текстового блока и текстом, который он содержит. Значение по умолчанию — 0,1 дюйма.
ms.openlocfilehash: 7a9d2406792e9e57c6acd0e4291b624633e70dcb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433523"
---
# <a name="rightmargin-cell-text-block-format-section"></a>RightMargin Cell (Text Block Format Section)

Определяет расстояние между правой границей текстового блока и текстом, который он содержит. Значение по умолчанию — 0,1 дюйма.
  
## <a name="remarks"></a>Примечания

Это значение не зависит от масштаба рисования. Если рисунок масштабировать, правое поле остается тем же.
  
Чтобы получить ссылку на ячейку RightMargin по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | RightMargin  <br/> |
   
Чтобы получить ссылку на ячейку RightMargin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowText** <br/> |
| Индекс ячейки:  <br/> |**visTxtBlkRightMargin** <br/> |
   

