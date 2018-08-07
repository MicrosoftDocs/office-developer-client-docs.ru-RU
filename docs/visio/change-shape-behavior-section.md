---
title: Раздел "Изменение поведения фигуры"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Определяет свойства, которые были перенесены из старого фигуры фигуры замещения во время операции замены. Значения ячеек в разделе поведение фигуры изменить основной фигуры замены считываются во время операции замены фигуры.
ms.openlocfilehash: 3b4b3cac37b8415309a2433c19c2b420fd652df7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813361"
---
# <a name="change-shape-behavior-section"></a><span data-ttu-id="252e5-104">Раздел "Изменение поведения фигуры"</span><span class="sxs-lookup"><span data-stu-id="252e5-104">Change Shape Behavior Section</span></span>

<span data-ttu-id="252e5-105">Определяет свойства, которые были перенесены из старого фигуры фигуры замещения во время операции замены.</span><span class="sxs-lookup"><span data-stu-id="252e5-105">Determines the properties that are transferred from the old shape to the replacement shape during a replacement operation.</span></span> <span data-ttu-id="252e5-106">Значения ячеек в разделе **Поведение фигуры изменить** основной фигуры замены считываются во время операции замены фигуры.</span><span class="sxs-lookup"><span data-stu-id="252e5-106">The values of the cells in the **Change Shape Behavior** section of the Master shape of the replacement are read during the shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="252e5-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="252e5-107">Remarks</span></span>

<span data-ttu-id="252e5-108">Установив ячейки в разделе **Поведение формы изменений** , можно обеспечить определенных свойств фигуры замещения не изменяются во время операции замены.</span><span class="sxs-lookup"><span data-stu-id="252e5-108">By setting the cells in the **Change Shape Behavior** section, you can ensure that certain properties of the replacement shape remain unchanged during the replacement operation.</span></span> <span data-ttu-id="252e5-109">Свойства, которые не защищены обновляются значениями локальной фигуры из старой фигуры во время операции.</span><span class="sxs-lookup"><span data-stu-id="252e5-109">Properties that are not protected are updated with the local shape values from the old shape during the operation.</span></span> 
  
<span data-ttu-id="252e5-110">Замена можно изменить параметры режима образца фигуры путем редактирования основной фигуры (в окне **фигур** , щелкните правой кнопкой мыши фигуру, выберите команду **Изменить**шаблон и нажмите кнопку **Изменить основной фигуры**) и изменение значений [ ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)и [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) ячеек в основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="252e5-110">You can change the replacement behavior settings of a Master shape by editing the Master shape (in the **Shapes** window, right-click the shape, point to **Edit Master**, and then click **Edit Master Shape**) and changing the values of the [ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md), and [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) cells in the Master's ShapeSheet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="252e5-111">Не может изменить поведение замены фигуры фигур, входящих в состав встроенных наборы элементов в Microsoft Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="252e5-111">You cannot change the shape replacement behaviors of the shapes that are included with the built-in stencils in Microsoft Visio 2013.</span></span> <span data-ttu-id="252e5-112">Для изменения поведения замены фигуры встроенных фигур Visio, создайте новый набор элементов и добавить фигуру, который требуется внести изменения в новый набор элементов.</span><span class="sxs-lookup"><span data-stu-id="252e5-112">To modify the shape replacement behaviors of the built-in Visio shapes, create a new stencil and add the shape that you want to modify to the new stencil.</span></span> 
  

