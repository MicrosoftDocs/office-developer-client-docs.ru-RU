---
title: Invisible Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
localization_priority: Normal
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: Указывает, отображается ли гиперссылка в ярлыке для фигуры или страницы.
ms.openlocfilehash: b52da8244bf31e75bacbb6f24f73eba6ee8c6e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404633"
---
# <a name="invisible-cell-hyperlinks-section"></a>Invisible Cell (Hyperlinks Section)

Указывает, отображается ли гиперссылка в ярлыке для фигуры или страницы. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Гиперссылка не будет отображаться в качестве пункта меню в ярлыке.  <br/> |
|FALSE  <br/> |Гиперссылка появляется в качестве пункта меню в ярлыке (по умолчанию).  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку Invisible по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |Гиперссылка. *name*  . Невидимый, где  *.name гиперссылки*  — это имя строки  <br/> |
   
Чтобы получить ссылку на ячейку Invisible по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionHyperlink** <br/> |
|Индекс строки:  <br/> |**visRow1stHyperlink**  +   *i* где *i* = 0, 1, 2...  <br/> |
|Индекс ячейки:  <br/> |**visHLinkInvisible** <br/> |
   

