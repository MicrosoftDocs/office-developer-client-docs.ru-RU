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
ms.openlocfilehash: b4d927e1970e994047df3cb89afa7799a825511d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814296"
---
# <a name="newwindow-cell-hyperlinks-section"></a>Ячейка NewWindow (раздел "Гиперссылки")

Указывает, следует ли открывать гиперссылки в новом окне.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Откройте связанную страницу, документа или веб-сайта в новом окне.  <br/> |
| FALSE  <br/> | Значение, используемое по умолчанию. Не открывать новое окно гиперссылки.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку NewWindow по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Гиперссылки.  *Имя* . NewWindow где гиперссылки.  *Имя* — это имя строки  <br/> |
   
Для получения ссылки на ячейки NewWindow по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionHyperlink** <br/> |
| Индекс строки:  <br/> |**visRow1stHyperlink** +  *i* где *i* = 0, 1, 2,...  <br/> |
| Индекс ячейки:  <br/> |**visHLinkNewWin** <br/> |
   

