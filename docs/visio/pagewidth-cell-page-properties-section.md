---
title: PageWidth Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
localization_priority: Normal
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: Определяет ширину печатных страниц в единицах рисования.
ms.openlocfilehash: 6d887cb4335d2725101db54ba2b1483ccf01cff4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434272"
---
# <a name="pagewidth-cell-page-properties-section"></a>PageWidth Cell (Page Properties Section)

Определяет ширину печатных страниц в единицах рисования.
  
## <a name="remarks"></a>Примечания

Вы также можете установить ширину страницы на  вкладке "Размер страницы" диалогового  окна "Настройка страницы" (на вкладке "Конструктор", щелкните стрелку "Настройка страницы") или вручную измерив размер страницы мышью.   Для этого перетащите край страницы, удерживая клавишу CTRL. 
  
Чтобы получить ссылку на ячейку PageWidth по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |PageWidth  <br/> |
   
Чтобы получить ссылку на ячейку PageWidth по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPage** <br/> |
|Индекс ячейки:  <br/> |**visPageWidth** <br/> |
   

