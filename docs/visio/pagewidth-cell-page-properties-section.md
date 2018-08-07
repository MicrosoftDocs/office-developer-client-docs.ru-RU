---
title: Ячейка PageWidth (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
localization_priority: Normal
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: Определяет ширину печатной страницы в единицах документа.
ms.openlocfilehash: e03696c8f1c921c930d3563e9c73ef4ae613a7c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814356"
---
# <a name="pagewidth-cell-page-properties-section"></a>Ячейка PageWidth (раздел "Свойства страницы")

Определяет ширину печатной страницы в единицах документа.
  
## <a name="remarks"></a>Замечания

Можно также задать ширину страницы на вкладке **Размер страницы** диалогового окна **Параметры страницы** (на вкладки " **Конструктор** ", нажмите стрелку **Параметры страницы** ) или вручную изменения размеров страницы с помощью мыши. Для этого перетащите края страницы, удерживая нажатой клавишу CTRL. 
  
Для получения ссылки на ячейки PageWidth по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |PageWidth  <br/> |
   
Для получения ссылки на ячейки PageWidth по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPage** <br/> |
|Индекс ячейки:  <br/> |**visPageWidth** <br/> |
   

