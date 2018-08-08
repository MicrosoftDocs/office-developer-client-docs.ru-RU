---
title: Ячейка ConFixedCode (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm175
localization_priority: Normal
ms.assetid: 8e7c9080-7ef1-0696-a3d2-d8f57ea5ab9b
description: Определяет, когда перенаправляет соединитель.
ms.openlocfilehash: 448e721d8dd6e287c61488e28b875f76d0fa2977
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813460"
---
# <a name="confixedcode-cell-shape-layout-section"></a>Ячейка ConFixedCode (раздел "Макет фигуры")

Определяет, когда перенаправляет соединитель.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Изменять направление автоматически  <br/> |**visSLOConFixedRerouteFreely** <br/> |
|1  <br/> |Изменение маршрута как необходимые (вручную перенаправить)  <br/> |**visSLOConFixedRerouteAsNeeded** <br/> |
|2  <br/> |Не изменять направление  <br/> |**visSLOConFixedRerouteNever** <br/> |
|3  <br/> |Изменять направление при пересечении  <br/> |**visSLOConFixedRerouteOnCrossover** <br/> |
|4  <br/> |Только для внутреннего использования  <br/> |**visSLOConFixedByAlgFrom** <br/> |
|5  <br/> |Только для внутреннего использования  <br/> |**visSLOConFixedByAlgTo** <br/> |
|6  <br/> |Только для внутреннего использования  <br/> |**visSLOConFixedByAlgFromTo** <br/> |
   
## <a name="remarks"></a>Замечания

Можно также значение ячейки с выбор динамического соединителя, нажав кнопку **поведение** группы **Разработки фигуры** на вкладки " [Разработчик](run-in-developer-mode-display-the-developer-tab.md) " и затем выбрав вкладку **соединителя** . 
  
Чтобы получить ссылку на ячейку ConFixedCode по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |ConFixedCode  <br/> |
   
Для получения ссылки на ячейки ConFixedCode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOConFixedCode** <br/> |
   

