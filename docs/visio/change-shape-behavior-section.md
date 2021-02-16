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
# <a name="change-shape-behavior-section"></a><span data-ttu-id="f573f-104">Change Shape Behavior Section</span><span class="sxs-lookup"><span data-stu-id="f573f-104">Change Shape Behavior Section</span></span>

<span data-ttu-id="f573f-105">Определяет свойства, которые переносятся из старой фигуры в заменяемую форму во время операции замены.</span><span class="sxs-lookup"><span data-stu-id="f573f-105">Determines the properties that are transferred from the old shape to the replacement shape during a replacement operation.</span></span> <span data-ttu-id="f573f-106">Значения ячеек в разделе "Изменение **поведения фигуры"** в фигуре "Хозяин" замены считыются во время операции замены фигуры.</span><span class="sxs-lookup"><span data-stu-id="f573f-106">The values of the cells in the **Change Shape Behavior** section of the Master shape of the replacement are read during the shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f573f-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="f573f-107">Remarks</span></span>

<span data-ttu-id="f573f-108">Установив ячейки в разделе **"Изменение** поведения фигуры", вы можете убедиться, что некоторые свойства заменяемой фигуры остаются неизменными во время операции замены.</span><span class="sxs-lookup"><span data-stu-id="f573f-108">By setting the cells in the **Change Shape Behavior** section, you can ensure that certain properties of the replacement shape remain unchanged during the replacement operation.</span></span> <span data-ttu-id="f573f-109">Свойства, которые не защищены, обновляются с помощью локальных значений фигуры из старой фигуры во время операции.</span><span class="sxs-lookup"><span data-stu-id="f573f-109">Properties that are not protected are updated with the local shape values from the old shape during the operation.</span></span> 
  
<span data-ttu-id="f573f-110">Вы можете изменить параметры поведения замены для фигуры Master, изменив фигуру "Master" (в окне **"Фигуры",** щелкните ее правой кнопкой мыши, найдите пункт "Изменить хозяин" и выберите пункт "Изменить хозяин фигуры") и измените значения ячеек [ReplaceCopyCells,](replacecopycells-cell-change-shape-behavior-section.md) [ReplaceLockFormat,](replacelockformat-cell-change-shape-behavior-section.md) [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)и [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) в таблице Фигуры хозяина.  </span><span class="sxs-lookup"><span data-stu-id="f573f-110">You can change the replacement behavior settings of a Master shape by editing the Master shape (in the **Shapes** window, right-click the shape, point to **Edit Master**, and then click **Edit Master Shape**) and changing the values of the [ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md), and [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) cells in the Master's ShapeSheet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f573f-111">Вы не можете изменить поведение замены фигур, включенных во встроенные трафареты в Microsoft Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="f573f-111">You cannot change the shape replacement behaviors of the shapes that are included with the built-in stencils in Microsoft Visio 2013.</span></span> <span data-ttu-id="f573f-112">Чтобы изменить поведение замены фигур встроенных фигур Visio, создайте новый трафарет и добавьте фигуру, которую необходимо изменить, в новый трафарет.</span><span class="sxs-lookup"><span data-stu-id="f573f-112">To modify the shape replacement behaviors of the built-in Visio shapes, create a new stencil and add the shape that you want to modify to the new stencil.</span></span> 
  

