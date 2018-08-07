---
title: Ячейка NoObjHandles (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm730
localization_priority: Normal
ms.assetid: 8e1c8c8f-4ed0-0f53-f93f-3a264edc02bd
description: Включает или отключает отображение маркеров выделения и отключает для выбранной фигуры.
ms.openlocfilehash: 8f812c2087870529cb65aa2e7d705171a5d4ca32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814324"
---
# <a name="noobjhandles-cell-miscellaneous-section"></a>Ячейка NoObjHandles (раздел "Прочее")

Включает или отключает отображение маркеров выделения и отключает для выбранной фигуры.
  
|**Значение**|**Описание**|
|:-----|:-----|
| TRUE  <br/> | Маркеры выделения, не отображаются при выборе фигуры.  <br/> |
| FALSE  <br/> | Маркеры выделения, отображаются при выборе фигуры.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку NoObjHandles по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
| Имя ячейки.  <br/> | NoObjHandles  <br/> |
   
Для получения ссылки на ячейки NoObjHandles по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
| Индекс раздела:  <br/> |**visSectionObject** <br/> |
| Индекс строки:  <br/> |**visRowMisc** <br/> |
| Индекс ячейки:  <br/> |**visNoObjHandles** <br/> |
   

