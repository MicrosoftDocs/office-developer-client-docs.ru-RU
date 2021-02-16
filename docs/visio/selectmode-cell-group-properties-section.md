---
title: SelectMode Cell (Group Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
localization_priority: Normal
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: Определяет, как выбрать фигуру группы и ее члены.
ms.openlocfilehash: 82f9e2806d1131a0acfd064f585c681fef0f209f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435364"
---
# <a name="selectmode-cell-group-properties-section"></a>SelectMode Cell (Group Properties Section)

Определяет, как выбрать фигуру группы и ее члены.
  
|**Значение**|**Режим выделения**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Выберите только фигуру группы.  <br/> |**visGrpSelModeGroupOnly** <br/> |
|1   <br/> |Сначала выберите фигуру группы.  <br/> |**visGrpSelModeGroup1st** <br/> |
|2   <br/> |Сначала выберите участников группы.  <br/> |**visGrpSelModeMembers1st** <br/> |
   
## <a name="remarks"></a>Примечания

Вы также можете установить  это значение в диалоговом окне [](run-in-developer-mode-display-the-developer-tab.md) "Поведение" (выбрав фигуру группы, на вкладке "Разработчик" в группе "Проектирование фигур" щелкните "Поведение" и выберите режим в списке "Выбор" в группе **"Поведение").**   
  
Чтобы получить ссылку на ячейку SelectMode по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |SelectMode  <br/> |
   
Чтобы получить ссылку на ячейку SelectMode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowGroup** <br/> |
|Индекс ячейки:  <br/> |**visGroupSelectMode** <br/> |
   

