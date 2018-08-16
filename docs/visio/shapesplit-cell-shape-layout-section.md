---
title: Ячейка ShapeSplit (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60080
localization_priority: Normal
ms.assetid: 96b8c503-67b3-8623-d99b-0dad7b15c224
description: Указывает, будет ли эта фигура разделять фигуры, которые можно разбить таблицу.
ms.openlocfilehash: b782977bd5b7e828223675eb16f4e7e48f4ca55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814805"
---
# <a name="shapesplit-cell-shape-layout-section"></a>Ячейка ShapeSplit (раздел "Макет фигуры")

Указывает, будет ли эта фигура разделять фигуры, которые можно разбить таблицу.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
| 0  <br/> | Не разрешать этой фигуры для разделения другие фигуры.  <br/> |**visSLOSplitNone** <br/> |
| 1  <br/> | Разрешить этой фигуры для разделения другие фигуры.  <br/> |**visSLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Замечания

Фигура, который можно разделить другие фигуры должен быть плоских фигур или 1 D размещаемой фигуры. 
  
Автоматическое разделение фигур включена и отключена три уровня: приложения, страницы и фигуры. По умолчанию разделение включена на приложения и уровне страницы; для фигур он изменяется в соответствии с тип графического. 
  
Чтобы включить или отключить разделение на уровне приложения, используйте параметр **включить разделение соединительной линии** на вкладке **Дополнительно** диалогового окна **Параметры Visio** (перейдите на вкладку **файл** , выберите пункт **Параметры**и нажмите кнопку ** Расширенный**). 
  
Чтобы включить или отключить разбиение на страницы, обратитесь к разделу PageShapeSplit ячейки. 
  
Чтобы вызвать одномерной фигуры иметь возможность разделения, обратитесь к разделу ячейки ShapeSplittable.
  
Чтобы получить ссылку на ячейку ShapeSplit по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | ShapeSplit  <br/> |
   
Для получения ссылки на ячейки ShapeSplit по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
| Индекс ячейки:  <br/> |**visSLOSplit** <br/> |
   
