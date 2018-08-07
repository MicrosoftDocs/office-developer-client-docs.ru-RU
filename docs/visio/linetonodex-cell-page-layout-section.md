---
title: Ячейка LineToNodeX (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm575
localization_priority: Normal
ms.assetid: 9d58e23e-b411-c5c1-b785-5014488d42c8
description: Определяет горизонтальную свободное пространство между все соединители и фигур на странице документа.
ms.openlocfilehash: 75f7e8150711421138a01175be34003d124e88ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814095"
---
# <a name="linetonodex-cell-page-layout-section"></a>Ячейка LineToNodeX (раздел "Макет страницы")

Определяет горизонтальную свободное пространство между все соединители и фигур на странице документа.
  
## <a name="remarks"></a>Замечания

Также можно задать значение данной ячейки в диалоговом окне **Макет и интервал по маршрутизации** . (На вкладке **Конструктор** щелкните стрелку **Параметры страницы** , нажмите кнопку **Макет и маршрутизации**и нажмите кнопку **интервалы**.)
  
Чтобы получить ссылку на ячейку LineToNodeY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |LineToNodeX  <br/> |
   
Для получения ссылки на ячейки LineToNodeX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowPageLayout** <br/> |
|Индекс ячейки:  <br/> |**visPLOLineToNodeX** <br/> |
   

