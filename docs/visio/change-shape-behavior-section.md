---
title: Change Shape Behavior Section
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Определяет свойства, которые передаются из старой фигуры в замещающую фигуру во время операции замены. Значения ячеек в разделе изменение поведения фигуры основной фигуры замены считываются во время операции замены фигуры.
ms.openlocfilehash: 74519b27ab5b2b5bafc7c00010a65769061bf691
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341925"
---
# <a name="change-shape-behavior-section"></a>Change Shape Behavior Section

Определяет свойства, которые передаются из старой фигуры в замещающую фигуру во время операции замены. Значения ячеек в разделе **изменение поведения фигуры** основной фигуры замены считываются во время операции замены фигуры. 
  
## <a name="remarks"></a>Комментарии

Настраивая ячейки в разделе **изменение поведения фигуры** , можно гарантировать, что определенные свойства замещающей фигуры остаются неизменными во время операции замены. Свойства без защиты обновляются с использованием значений локальных фигур из старой фигуры во время выполнения операции. 
  
Вы можете изменить параметры поведения замены образца фигуры, изменив основную фигуру (в окне **фигуры** щелкните фигуру правой кнопкой мыши, наведите указатель на пункт **изменить образец**, а затем выберите команду **изменить образец фигуры**) и измените значения [Свойства Ячейки ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)и [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) в таблице свойств фигуры. 
  
> [!NOTE]
> Изменение поведения фигур, включенных вместе со встроенными трафаретами в Microsoft Visio 2013, невозможно. Чтобы изменить поведение замены фигур встроенных фигур Visio, создайте новый набор элементов и добавьте фигуру, которую нужно изменить, в новый набор элементов. 
  

