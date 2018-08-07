---
title: Ячейка NonPrinting (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
localization_priority: Normal
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: Параметры печати и отключает для выбранной фигуры.
ms.openlocfilehash: ab00914a9c59cfe94b3f7273f89684f43328b4d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814299"
---
# <a name="nonprinting-cell-miscellaneous-section"></a>Ячейка NonPrinting (раздел "Прочее")

Параметры печати и отключает для выбранной фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Печать отключена, но фигуры отображаются в окне документа.  <br/> |
| FALSE  <br/> | Печать включена.  <br/> |
   
## <a name="remarks"></a>Замечания

Можно распечатать руководства, выбрав его, а затем устанавливает значение ячейки его непечатаемый значение FALSE.
  
Для получения ссылки на ячейки непечатаемый по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Непечатаемый  <br/> |
   
Для получения ссылки на ячейки непечатаемый по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visNonPrinting** <br/> |
   

