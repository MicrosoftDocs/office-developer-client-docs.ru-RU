---
title: DrawingScaleType Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
localization_priority: Normal
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: Определяет масштаб документа, выбранный в диалоговом окне "Параметры страницы" (щелкните стрелку настройки страницы на вкладке "Главная").
ms.openlocfilehash: d1c1c00ffe025c566646a1f8b9fe034732ad86a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428741"
---
# <a name="drawingscaletype-cell-page-properties-section"></a>DrawingScaleType Cell (Page Properties Section)

Определяет масштаб документа, выбранный в диалоговом окне " **Параметры страницы** " (щелкните стрелку **настройки страницы** на вкладке " **Главная** "). 
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| нуль  <br/> | Без масштаба  <br/> |**висноскале** <br/> |
| 1,1  <br/> | Архитектурный масштаб  <br/> |**висарчитектурал** <br/> |
| 2  <br/> | Масштабирование гражданского проектирования  <br/> |**висенгиниринг** <br/> |
| 4  <br/> | Настраиваемый масштаб  <br/> |**висскалекустом** <br/> |
| 4   <br/> | Метрика  <br/> |**висскалеметрик** <br/> |
| 5   <br/> | Механическая масштабируемость  <br/> |**висскалемечаникал** <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить ссылку на ячейку DrawingScaleType по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
| Имя ячейки:  <br/> | DrawingScaleType  <br/> |
   
Чтобы получить ссылку на ячейку DrawingScaleType по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**висровпаже** <br/> |
| Индекс ячейки:  <br/> |**виспажедравскалетипе** <br/> |
   

