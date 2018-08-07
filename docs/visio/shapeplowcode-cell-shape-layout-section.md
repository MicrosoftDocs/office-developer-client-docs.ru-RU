---
title: Ячейка ShapePlowCode (раздел "Макет фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
localization_priority: Normal
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: Определяет, будет ли этот размещаемой фигуры перемещает нет на месте при перетаскивании другой фигуры к ним рядом с этой фигуры на странице документа.
ms.openlocfilehash: 5917abad653e7aaf40da05eafa3f9f1a90a2cf9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814792"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a>Ячейка ShapePlowCode (раздел "Макет фигуры")

Определяет, будет ли этот размещаемой фигуры перемещает нет на месте при перетаскивании другой фигуры к ним рядом с этой фигуры на странице документа.
  
|**Значение**|**Описание**|**Константа автоматизации**|
|:-----|:-----|:-----|
|0  <br/> |Сдвигать, как указано для страницы.  <br/> |**visSLOPlowDefault** <br/> |
|1  <br/> |Не сдвигать фигуры.  <br/> |**visSLOPlowNever** <br/> |
|2  <br/> |Сдвигать все фигуры.  <br/> |**visSLOPlowAlways** <br/> |
   
## <a name="remarks"></a>Замечания

Также можно настроить значение ячейки для определенного фигуры на вкладку **Размещение** в диалоговом окне **поведение** (с фигурой выбрано, на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) в группе **Разработки фигуры** выберите **поведение**и нажмите кнопку Вкладка **Размещение** ). 
  
Чтобы задать это поведение для *всех* фигур на странице документа, используйте ячейку PlowCode в разделе макет страницы. 
  
Чтобы получить ссылку на ячейку ShapePlowCode по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |ShapePlowCode  <br/> |
   
Для получения ссылки на ячейки ShapePlowCode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowShapeLayout** <br/> |
|Индекс ячейки:  <br/> |**visSLOPlowCode** <br/> |
   

