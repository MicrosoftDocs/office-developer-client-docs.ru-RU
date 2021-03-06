---
title: Smart Tags Row (Action Tags Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026926
localization_priority: Normal
ms.assetid: 065c6977-c737-a4f4-effa-0fd2c98e8bbf
description: Содержит сведения для одного тега действий, связанного с фигурой или страницей. Фигура или страница содержит одну строку Smart Tags для каждого тега действий.
ms.openlocfilehash: 1c1591fd2d2cacfbfb350a542e6601cb2f6fbfd6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404710"
---
# <a name="smart-tags-row-action-tags-section"></a>Smart Tags Row (Action Tags Section)

Содержит сведения для одного тега действий, связанного с фигурой или страницей. Фигура или страница содержит одну строку Smart Tags для каждого тега действий.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
Строки Smart Tags называются SmartTags. *имя*  и содержать следующие ячейки. Дополнительные сведения см. в конкретных разделах ячейки. 
  
|**Cell**|**Описание**|
|:-----|:-----|
|[X](x-cell-action-tags-section.md) <br/> |Расположение  *точки*  в локальных координатах фигуры, вокруг которой расположена кнопка тега действия.  <br/> |
|[Да](y-cell-action-tags-section.md) <br/> |Расположение  *y-координаты*  точки в локальных координатах фигуры, вокруг которой расположена кнопка тега действия.  <br/> |
|[TagName](tagname-cell-action-tags-section.md) <br/> |Логическое имя тега действия.  <br/> |
|[X Justify](x-justify-cell-action-tags-section.md) <br/> |Смещение по оси *x* для кнопки тега действия, связанной с точкой, которая определена ячейками X и Y.  <br/> |
|[Y Justify](y-justify-cell-action-tags-section.md) <br/> |Смещение по оси *y* для кнопки тега действия, связанной с точкой, которая определена ячейками X и Y.  <br/> |
|[DisplayMode](displaymode-cell-action-tags-section.md) <br/> |Определяет, когда появится тег действия.  <br/> |
|[ButtonFace](buttonface-cell-action-tags-section.md) <br/> |ID изображения, которое отображается на лицевом лице кнопки тег действий.  <br/> |
|[Описание](description-cell-action-tags-section.md) <br/> |Описательная строка для тега действия.  <br/> |
|[Disabled](disabled-cell-action-tags-section.md) <br/> |Указывает, отключен ли тег действия.  <br/> |
   
## <a name="remarks"></a>Примечания

 Вы можете добавить как можно больше SmartTags.  *Строки*  имен по мере необходимости назначьте значимые имена строкам и установите значения ячейки. Чтобы добавить тег действий в существующий раздел Smart Tags, щелкните правой кнопкой мыши строку и нажмите кнопку **Вставить** строку в меню ярлыка. 
  
Вы можете ссылаться на эти ячейки по имени строки, которое отображается в окне ShapeSheet в красном тексте. Назначение значимых имен смарт-тегам. *строки*  имен, щелкните строку, а затем введите имя, например  *Размер,*  чтобы создать имя строки Smart Tags.Size. Затем можно ссылаться на ячейку Description с помощью Smart Tags.Size.Description. 
  
Имя строки, которое вы вводите, должно быть уникальным в разделе.
  

