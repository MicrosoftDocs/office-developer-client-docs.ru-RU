---
title: Ячейка ResizeMode (раздел "Преобразование фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Отображает текущий изменения размера для фигуры.
ms.openlocfilehash: a32f5dbc935e85a49ab585073ca6a31215fd102a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814638"
---
# <a name="resizemode-cell-shape-transform-section"></a>Ячейка ResizeMode (раздел "Преобразование фигуры")

Отображает текущий изменения размера для фигуры.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Используйте значение группы.  <br/> |**visXFormResizeDontCare** <br/> |
|1  <br/> |Только перемещение.  <br/> |**visXFormResizeSpread** <br/> |
|2  <br/> |Масштабирование с группой.  <br/> |**visXFormResizeScale** <br/> |
   
## <a name="remarks"></a>Замечания

Это значение также можно настроить на вкладке **поведение** в диалоговом окне " **поведение** " (на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md)в группе **Разработки фигуры** выберите **поведение**). Чтобы получить ссылку на ячейку ResizeMode по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |ResizeMode  <br/> |
   
Для получения ссылки на ячейки ResizeMode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowXFormOut** <br/> |
|Индекс ячейки:  <br/> |**visXFormResizeMode** <br/> |
   

