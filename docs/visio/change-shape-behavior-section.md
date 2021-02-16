---
title: Change Shape Behavior Section
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Определяет свойства, которые переносятся из старой фигуры в заменяемую форму во время операции замены. Значения ячеек в разделе "Изменение поведения фигуры" в фигуре "Хозяин" замены считыются во время операции замены фигуры.
ms.openlocfilehash: 74519b27ab5b2b5bafc7c00010a65769061bf691
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418668"
---
# <a name="change-shape-behavior-section"></a>Change Shape Behavior Section

Определяет свойства, которые переносятся из старой фигуры в заменяемую форму во время операции замены. Значения ячеек в разделе "Изменение **поведения фигуры"** в фигуре "Хозяин" замены считыются во время операции замены фигуры. 
  
## <a name="remarks"></a>Примечания

Установив ячейки в разделе **"Изменение** поведения фигуры", вы можете убедиться, что некоторые свойства заменяемой фигуры остаются неизменными во время операции замены. Свойства, которые не защищены, обновляются с помощью локальных значений фигуры из старой фигуры во время операции. 
  
Вы можете изменить параметры поведения замены для фигуры Master, изменив фигуру "Master" (в окне **"Фигуры",** щелкните ее правой кнопкой мыши, найдите пункт "Изменить хозяин" и выберите пункт "Изменить хозяин фигуры") и измените значения ячеек [ReplaceCopyCells,](replacecopycells-cell-change-shape-behavior-section.md) [ReplaceLockFormat,](replacelockformat-cell-change-shape-behavior-section.md) [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)и [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) в таблице Фигуры хозяина.   
  
> [!NOTE]
> Вы не можете изменить поведение замены фигур, включенных во встроенные трафареты в Microsoft Visio 2013. Чтобы изменить поведение замены фигур встроенных фигур Visio, создайте новый трафарет и добавьте фигуру, которую необходимо изменить, в новый трафарет. 
  

