---
title: Ячейка IsSnapTarget (раздел "Свойства группы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251626
localization_priority: Normal
ms.assetid: b58131f6-a566-d9ca-bad4-4f4b66e03aaf
description: Определяет, выполняется ли привязка к группе или к фигурам в группе.
ms.openlocfilehash: 89536923617f80768d7c14658cb07c97595824ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814003"
---
# <a name="issnaptarget-cell-group-properties-section"></a>Ячейка IsSnapTarget (раздел "Свойства группы")

Определяет, выполняется ли привязка к группе или к фигурам в группе.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Включение привязки к фигурам в группе.  <br/> |
|FALSE  <br/> |Привязка только для группы.  <br/> |
   
## <a name="remarks"></a>Замечания

Также можно задать это значение, выбрав в группу, щелкая вкладки " [Разработчик](run-in-developer-mode-display-the-developer-tab.md) " **поведение** и затем установите флажок **Привязка к фигурам** . 
  
Чтобы получить ссылку на ячейку IsSnapTarget по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |IsSnapTarget  <br/> |
   
Для получения ссылки на ячейки IsSnapTarget по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowGroup** <br/> |
|Индекс ячейки:  <br/> |**visGroupIsSnapTarget** <br/> |
   

