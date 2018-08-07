---
title: Ячейка EnableFillProps (раздел "Свойства стиля")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm300
localization_priority: Normal
ms.assetid: 2b3334de-588c-6cf3-bc88-be03ae71b1a6
description: Определяет, включены ли в стиль свойства заливки.
ms.openlocfilehash: 399af4b9d1a2245ea7a9b91ebbf036eb122f15bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813689"
---
# <a name="enablefillprops-cell-style-properties-section"></a>Ячейка EnableFillProps (раздел "Свойства стиля")

Определяет, включены ли в стиль свойства заливки.
  
|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Включайте свойства заливки.  <br/> |
|FALSE  <br/> |Исключение свойства заливки.  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить ссылку на ячейку EnableFillProps по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |EnableFillProps  <br/> |
   
Для получения ссылки на ячейки EnableFillProps по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRowStyle** <br/> |
|Индекс ячейки:  <br/> |**visStyleIncludesFill** <br/> |
   

