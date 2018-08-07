---
title: Ячейка NoCtlHandles (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251319
localization_priority: Normal
ms.assetid: 4345b3e5-f522-e300-307c-4f8992a3ddce
description: Включает или отключает отображение управляющих маркеров и отключает для выбранной фигуры.
ms.openlocfilehash: 897e4cd97eeab8797f2652285ba395603c41a8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814292"
---
# <a name="noctlhandles-cell-miscellaneous-section"></a>Ячейка NoCtlHandles (раздел "Прочее")

Включает или отключает отображение управляющих маркеров и отключает для выбранной фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Управляющие маркеры не отображаются при выборе фигуры.  <br/> |
| FALSE  <br/> | Управляющие маркеры отображаются при выборе фигуры.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку NoCtlHandles по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | NoCtlHandles  <br/> |
   
Для получения ссылки на ячейки NoCtlHandles по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visNoCtlHandles** <br/> |
   

