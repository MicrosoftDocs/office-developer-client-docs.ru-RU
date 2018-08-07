---
title: Ячейка DynamicsOff (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251641
localization_priority: Normal
ms.assetid: 055764aa-9681-ffb0-83ce-fdd612fe37af
description: Определяет, будет ли размещаемые фигуры и соединители перенаправление вокруг другие фигуры и соединители на странице документа.
ms.openlocfilehash: 72d65860d1a2ee37efd5287ae3f4baf54bd3addb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813665"
---
# <a name="dynamicsoff-cell-page-layout-section"></a>Ячейка DynamicsOff (раздел "Макет страницы")

Определяет, будет ли размещаемые фигуры и соединители перенаправление вокруг другие фигуры и соединители на странице документа.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Отключение dynamics.  <br/> |
| FALSE  <br/> | Включение dynamics.  <br/> |
   
## <a name="remarks"></a>Замечания

Можно отключить dynamics для повышения производительности решения. Например если решение добавляет размещаемые фигуры на рисунок и требуется приложение для перенаправления соединители и изменить положение фигур каждый раз при добавлении фигуры, можно отключить dynamics. После решения добавляет фигур, повторно включите dynamics.
  
Чтобы получить ссылку на ячейку DynamicsOff по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | DynamicsOff  <br/> |
   
Для получения ссылки на ячейки DynamicsOff по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowPageLayout** <br/> |
| Индекс ячейки:  <br/> |**visPLODynamicsOff** <br/> |
   

