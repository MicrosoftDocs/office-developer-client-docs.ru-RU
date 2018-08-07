---
title: Ячейка KeepTextFlat (раздел "Свойства поворота объемной фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Указывает, будет ли текстом фигуры будет игнорировать Поворот фигуры в объемных. Не применяется к плоских вращение.
ms.openlocfilehash: cf8b964360e602b81a2a7b7ca79961921eeeb8b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814021"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>Ячейка KeepTextFlat (раздел "Свойства поворота объемной фигуры")

Указывает, будет ли текстом фигуры будет игнорировать Поворот фигуры в объемных. Не применяется к плоских вращение. 
  
****

|**Значение**|**Описание**|
|:-----|:-----|
|TRUE  <br/> |Не поворачивайте текст фигуры с геометрией фигуры.  <br/> |
|FALSE  <br/> |Фигура текст преобразован в поворот с геометрией фигуры.  <br/> |
   
## <a name="remarks"></a>Замечания

Для получения ссылки на ячейки **KeepTextFlat** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте: 
  
|||
|:-----|:-----|
|Имя ячейки.  <br/> |KeepTextFlat  <br/> |
   
Для получения ссылки на ячейки **KeepTextFlat** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы: 
  
|||
|:-----|:-----|
|Индекс раздела:  <br/> |**visSectionObject** <br/> |
|Индекс строки:  <br/> |**visRow3DRotationProperties** <br/> |
|Индекс ячейки:  <br/> |**visKeepTextFlat** <br/> |
   

