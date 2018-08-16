---
title: Ячейка ShapePermeablePlace (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
localization_priority: Normal
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: Определяет, можно было включить размещаемые фигуры поверх фигуры при размещении фигур в диалоговом окне "Настройка макета" (на вкладке конструктор в группе макет нажмите кнопку Изменить расположение и нажмите кнопку Дополнительные параметры расположения).
ms.openlocfilehash: 1873575eb4322d31f81c0dd34557c6167750ce82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814772"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a>Ячейка ShapePermeablePlace (раздел "Макет фигуры")

Определяет, можно было включить размещаемые фигуры поверх фигуры при размещении фигур в диалоговом окне " **Настройка макета** " (на вкладке **Конструктор** в группе **Макет** нажмите кнопку **Изменить расположение**и нажмите кнопку **Дополнительные параметры расположения **).
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Включение фигуры, чтобы поместить поверх фигуры.  <br/> |
|FALSE  <br/> |Не следует включать фигуры, чтобы поместить поверх фигуры.  <br/> |
   
## <a name="remarks"></a>Замечания

Значение ячейки также можно настроить на вкладке **Размещение** в диалоговом окне **поведение** (с фигуры, выбранные на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) в группе **Создать фигуру** нажмите кнопку **поведение**и затем перейдите на вкладку **Размещение** ). 
  
Более ранних чем Visio 2000 в версиях задайте это поведение, с помощью ObjInteract ячеек в разделе Разное.
  
Чтобы получить ссылку на ячейку ShapePermeablePlace по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |ShapePermeablePlace  <br/> |
   
Для получения ссылки на ячейки ShapePermeablePlace по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOPermeablePlace** <br/> |
   
