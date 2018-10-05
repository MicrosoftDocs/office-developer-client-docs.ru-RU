---
title: Ячейка NewWindow (раздел "Гиперссылки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
localization_priority: Normal
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: Указывает, следует ли открывать гиперссылки в новом окне.
ms.openlocfilehash: 0f9d1e4b1294dea3f211c8d0d69ffc49b6180066
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396339"
---
# <a name="newwindow-cell-hyperlinks-section"></a>Ячейка NewWindow (раздел "Гиперссылки")

Указывает, следует ли открывать гиперссылки в новом окне.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Откройте связанную страницу, документа или веб-сайт в новом окне.  <br/> |
| FALSE  <br/> | Значение, используемое по умолчанию. Не открывать новое окно гиперссылки.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку NewWindow по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | Гиперссылки.  *Имя* . NewWindow где гиперссылки.  *Имя* — это имя строки  <br/> |
   
Для получения ссылки на ячейки NewWindow по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionHyperlink** <br/> |
| Индекс строки:  <br/> |**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2,...  <br/> |
| Индекс ячейки:  <br/> |**visHLinkNewWin** <br/> |
   

