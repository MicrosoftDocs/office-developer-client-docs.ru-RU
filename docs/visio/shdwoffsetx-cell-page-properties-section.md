---
title: Ячейка ShdwOffsetX (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
localization_priority: Normal
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: Определяет расстояние смещения тени фигуры по горизонтали относительно фигуры в единицах страницы.
ms.openlocfilehash: 9aec108146e329d7a8161acc4ca7cdcb19424eff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814833"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a>Ячейка ShdwOffsetX (раздел "Свойства страницы")

Определяет расстояние смещения тени фигуры по горизонтали относительно фигуры в единицах страницы.
  
## <a name="remarks"></a>Замечания

Это значение в диалоговом окне " **Параметры страницы** " (на вкладке " **Конструктор** ", щелкните стрелку **Параметры страницы** ). Это значение не зависит от масштаба документа. Если документа изменяется, смещение тени остается неизменным. 
  
Чтобы получить ссылку на ячейку ShdwOffsetX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | ShdwOffsetX  <br/> |
   
Для получения ссылки на ячейки ShdwOffsetX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPage** <br/> |
| Индекс ячейки:  <br/> |**visPageShdwOffsetX** <br/> |
   

