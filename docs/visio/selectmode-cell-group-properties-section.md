---
title: Ячейка SelectMode (раздел "Свойства группы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm875
localization_priority: Normal
ms.assetid: 5ba68e05-f394-d7b7-390d-f0a9fdad011e
description: Определяет способ выбора групповой фигуры и ее компонентов.
ms.openlocfilehash: 426b4a18bbd54887e4f60b92860a6c3846386671
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814740"
---
# <a name="selectmode-cell-group-properties-section"></a>Ячейка SelectMode (раздел "Свойства группы")

Определяет способ выбора групповой фигуры и ее компонентов.
  
|**Значение**|**Выбор режима**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Выберите только групповой фигуры.  <br/> |**visGrpSelModeGroupOnly** <br/> |
|1  <br/> |Сначала выберите групповой фигуры.  <br/> |**visGrpSelModeGroup1st** <br/> |
|2  <br/> |Выберите членов группы.  <br/> |**visGrpSelModeMembers1st** <br/> |
   
## <a name="remarks"></a>Замечания

В диалоговом окне " **поведение** " можно задать это значение (с групповой фигуры, выбранные на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) в группе **Создать фигуру** щелкните **поведение**и нажмите кнопку режим в **списке в разделе **группы Поведение**** ). 
  
Чтобы получить ссылку на ячейку SelectMode по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |SelectMode  <br/> |
   
Для получения ссылки на ячейки SelectMode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowGroup** <br/> |
|Индекс ячейки:  <br/> |**visGroupSelectMode** <br/> |
   

