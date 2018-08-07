---
title: Ячейка HideText (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
localization_priority: Normal
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: Скрывает текст фигуры. Можно просматривать текст, измените свойства и применить стили для текста в блоке текста, несмотря на то, что изменения не будут отображаться, пока не будет сброшен HideText значение FALSE (0).
ms.openlocfilehash: e2d220e9d7874382f2aaeade5488bd4809f3a9dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813913"
---
# <a name="hidetext-cell-miscellaneous-section"></a>Ячейка HideText (раздел "Прочее")

Скрывает текст фигуры. Можно просматривать текст, измените свойства и применить стили для текста в блоке текста, несмотря на то, что изменения не будут отображаться, пока не будет сброшен HideText значение FALSE (0).
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Текст скрыто и не печатается.  <br/> |
| FALSE  <br/> | Текст не скрывается.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки HideText по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | HideText  <br/> |
   
Для получения ссылки на ячейки HideText по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visHideText** <br/> |
   

