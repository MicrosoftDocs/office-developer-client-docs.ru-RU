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
description: Определяет способ выбора групповой фигуры и ее членов.
ms.openlocfilehash: 82f9e2806d1131a0acfd064f585c681fef0f209f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326014"
---
# <a name="selectmode-cell-group-properties-section"></a>SelectMode Cell (Group Properties Section)

Определяет способ выбора групповой фигуры и ее членов.
  
|**Значение**|**Режим выбора**|**Константа автоматизации**|
|:-----|:-----|:-----|
|нуль  <br/> |Выберите только фигуру группы.  <br/> |**Висгрпселмодеграупонли** <br/> |
|1,1  <br/> |Сначала выберите фигуру Group (группа).  <br/> |**visGrpSelModeGroup1st** <br/> |
|2  <br/> |Сначала выберите участников группы.  <br/> |**visGrpSelModeMembers1st** <br/> |
   
## <a name="remarks"></a>Замечания

Вы также можете задать это значение в диалоговом окне **поведение** (если выбрана фигура группы, на вкладке [разработчик](run-in-developer-mode-display-the-developer-tab.md) в группе **Макет фигуры** щелкните **поведение**, а затем выберите режим в списке **Выбор** раздела **Группа Поведение** ). 
  
Чтобы получить ссылку на ячейку SelectMode по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее: 
  
|||
|:-----|:-----|
|Имя ячейки:  <br/> |SelectMode  <br/> |
   
Чтобы получить ссылку на ячейку SelectMode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**Висровграуп** <br/> |
|Индекс ячейки:  <br/> |**Висграупселектмоде** <br/> |
   

