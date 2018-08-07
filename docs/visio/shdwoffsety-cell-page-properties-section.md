---
title: Ячейка ShdwOffsetY (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm930
localization_priority: Normal
ms.assetid: f3f53a7d-7450-b2b0-b508-6044a87450d9
description: Определяет расстояние смещения тени фигуры по вертикали относительно фигуры в единицах страницы.
ms.openlocfilehash: 0228fef00230dd1517d20067fda855225cef5533
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814850"
---
# <a name="shdwoffsety-cell-page-properties-section"></a>Ячейка ShdwOffsetY (раздел "Свойства страницы")

Определяет расстояние смещения тени фигуры по вертикали относительно фигуры в единицах страницы.
  
## <a name="remarks"></a>Замечания

Это значение в диалоговом окне " **Параметры страницы** " (на вкладке " **Конструктор** ", щелкните стрелку **Параметры страницы** ). Это значение не зависит от масштаба документа. Если документа изменяется, смещение тени остается неизменным. 
  
Чтобы получить ссылку на ячейку ShdwOffsetY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | ShdwOffsetY  <br/> |
   
Для получения ссылки на ячейки ShdwOffsetY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPage** <br/> |
| Индекс ячейки:  <br/> |**visPageShdwOffsetY** <br/> |
   

