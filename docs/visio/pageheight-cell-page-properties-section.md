---
title: PageHeight Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm760
localization_priority: Normal
ms.assetid: 0184814c-2d67-6ad4-e336-5694612e518d
description: Содержит высоту напечатанной страницы в единицах рисования.
ms.openlocfilehash: ac24bee517f29da333a445f276447c1aa682f01c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427082"
---
# <a name="pageheight-cell-page-properties-section"></a>PageHeight Cell (Page Properties Section)

Содержит высоту напечатанной страницы в единицах рисования.
  
## <a name="remarks"></a>Примечания

Вы также можете установить высоту страницы на  вкладке **Размер** страницы  диалогового окна установки страницы (на вкладке Дизайн, нажмите стрелку **Установки** страницы) или вручную переостановив размер страницы с помощью мыши. 
  
Чтобы получить ссылку на ячейку PageHeight по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |PageHeight  <br/> |
   
Чтобы получить ссылку на ячейку PageHeight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPage** <br/> |
|Индекс ячейки:  <br/> |**visPageHeight** <br/> |
   

