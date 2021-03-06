---
title: Actions Row (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60017
localization_priority: Normal
ms.assetid: 29a7464a-b9d4-a8ea-161b-3044de32ed23
description: Содержит ячейки, которые указывают действия, связанные с настраиваемой командой в меню ярлыков или тегов действий. Раздел Действия содержит одну строку Действия для каждого действия.
ms.openlocfilehash: 37464e98b3e4f7d07b2ae4bd391b31ec009b6726
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408007"
---
# <a name="actions-row-actions-section"></a>Actions Row (Actions Section)

Содержит ячейки, которые указывают действия, связанные с настраиваемой командой в меню ярлыков или тегов действий. Раздел Действия содержит одну строку Действия для каждого действия.
  
> [!NOTE]
> В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами. 
  
Строки действий называются Действиями. *имя*  и содержать следующие ячейки. Дополнительные сведения см. в конкретных разделах ячейки. 
  
|**Cell**|**Описание**|
|:-----|:-----|
|[Действие](action-cell-actions-section.md) <br/> |Содержит формулу, которая будет выполнена, когда пользователь выбирает элемент в меню ярлыка или тега действий.  <br/> |
|[Меню](menu-cell-actions-section.md) <br/> |Определяет имя элемента меню, который отображается в теге действия или меню ярлыка.  <br/> |
|[TagName](tagname-cell-actions-section.md) <br/> |Логическое имя тега действия, в котором должно отображаться это действие.  <br/> |
|[ButtonFace](buttonface-cell-actions-section.md) <br/> |Определяет значок, который отображается рядом с элементом в меню ярлыка или тега действий.  <br/> |
|[SortKey](sortkey-cell-actions-section.md) <br/> |Номер, определяя порядок элементов меню в теге действия или меню ярлыка.  <br/> |
|[Checked](checked-cell-actions-section.md) <br/> |Указывает, проверяется ли элемент меню в теге действия или в меню ярлыка.  <br/> |
|[Disabled](disabled-cell-actions-section.md) <br/> |Указывает, отключен ли элемент меню в меню ярлыка или тега действий.  <br/> |
|[ReadOnly](readonly-cell-actions-section.md) <br/> |Указывает, является ли элемент меню только для чтения (не может быть щелкнуть).  <br/> |
|[Невидимый](invisible-cell-actions-section.md) <br/> |Указывает, виден ли элемент меню в теге действия или в меню ярлыка.  <br/> |
|[BeginGroup](begingroup-cell-actions-section.md) <br/> |Указывает, следует ли вставлять сепаратор в меню над элементом меню.  <br/> |
   
## <a name="remarks"></a>Примечания

 Можно добавить как можно больше действий.  *Строки*  имен по мере необходимости назначьте значимые имена строкам и установите значения ячейки. Чтобы добавить настраиваемую команду в существующий раздел Действия, щелкните правой кнопкой мыши строку и нажмите **строку Вставить** строку в меню ярлыка. 
  
Вы можете ссылаться на эти ячейки по имени строки, которое отображается в окне ShapeSheet в красном тексте. Назначение значимого имени действий. *Строка*  имен, щелкните строку, а затем введите имя, например  *Custom,*  чтобы создать имя строки Actions.Custom. Затем вы можете ссылаться на ячейку Меню с помощью Actions.Custom.Menu. 
  
Имя строки, которое вы вводите, должно быть уникальным в разделе.
  

