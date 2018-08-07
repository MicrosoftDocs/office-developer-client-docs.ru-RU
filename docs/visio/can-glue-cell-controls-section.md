---
title: Ячейка Can Glue (раздел "Элементы управления")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
localization_priority: Normal
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: Определяет, может ли быть связан дескриптор элемента управления на другие фигуры.
ms.openlocfilehash: c7b6764e25deab3345b7b3cecd6cf12dde74a84c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813307"
---
# <a name="can-glue-cell-controls-section"></a>Ячейка Can Glue (раздел "Элементы управления")

Определяет, может ли быть связан дескриптор элемента управления на другие фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Может быть связан дескриптора элемента управления.  <br/> |
| FALSE  <br/> | Не может быть связан дескриптора элемента управления.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку можно связывающих по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | Элементы управления.  *имя* . Элементы управления CanGluewhere.  *имя* — это имя строки элементов управления.  <br/> |
   
Для получения ссылки на ячейки можно связывающих по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionControls** <br/> |
| Индекс строки:  <br/> |**visRowControl** +  *i* где *i* = 0, 1, 2,...  <br/> |
| Индекс ячейки:  <br/> |**visCtlGlue** <br/> |
   

