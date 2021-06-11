---
title: NewWindow Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
localization_priority: Normal
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: Указывает, следует ли открывать гиперссылку в новом окне.
ms.openlocfilehash: 0f9d1e4b1294dea3f211c8d0d69ffc49b6180066
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342233"
---
# <a name="newwindow-cell-hyperlinks-section"></a>NewWindow Cell (Hyperlinks Section)

Указывает, следует ли открывать гиперссылку в новом окне.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Откройте связанную страницу, документ или веб-сайт в новом окне.  <br/> |
| FALSE  <br/> | Значение, используемое по умолчанию. Не открывай новое окно для гиперссылки.  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку NewWindow по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Гиперссылка.  *Имя*  . NewWindow, где гиперссылка.  *Имя*  — это имя строки  <br/> |
   
Чтобы получить ссылку на ячейку NewWindow по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionHyperlink** <br/> |
| Индекс строки:  <br/> |**visRow1stHyperlink**  +   *i,* *где i* = 0, 1, 2, ...  <br/> |
| Индекс ячейки:  <br/> |**visHLinkNewWin** <br/> |
   

