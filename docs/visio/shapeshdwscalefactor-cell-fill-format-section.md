---
title: ShapeShdwScaleFactor Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033175
localization_priority: Normal
ms.assetid: 94ec06c5-8d2f-dd27-1eed-1abaf93daba8
description: Указывает процент, с помощью которого тень фигуры может быть увеличена или уменьшена.
ms.openlocfilehash: 5862b61ca1f5df25ca97bf8742b9e20bf45091a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436267"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a><span data-ttu-id="eed26-103">ShapeShdwScaleFactor Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="eed26-103">ShapeShdwScaleFactor Cell (Fill Format Section)</span></span>

<span data-ttu-id="eed26-104">Указывает процент, с помощью которого тень фигуры может быть увеличена или уменьшена.</span><span class="sxs-lookup"><span data-stu-id="eed26-104">Specifies the percentage by which the shadow of a shape can be enlarged or reduced.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eed26-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="eed26-105">Remarks</span></span>

<span data-ttu-id="eed26-106">Каждая тень имеет затеняемое расположение пина, которое является точкой на тени, соответствующей пин-коду фигуры.</span><span class="sxs-lookup"><span data-stu-id="eed26-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="eed26-107">Например, если пин-код фигуры находится в центре фигуры, то затеняемое расположение пина будет точкой в центре тени.</span><span class="sxs-lookup"><span data-stu-id="eed26-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="eed26-108">При применении масштабирования к простым теням увеличение расположено в затененом расположении пин-кода; При применении масштабирования к косой тени в косом направлении применяется увеличение.</span><span class="sxs-lookup"><span data-stu-id="eed26-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
<span data-ttu-id="eed26-109">Чтобы установить это значение для всех фигур на странице, используйте ячейку ShdwScaleFactor в разделе Свойства страниц.</span><span class="sxs-lookup"><span data-stu-id="eed26-109">To set this value for all the shapes on a page, use the ShdwScaleFactor cell in the Page Properties section.</span></span>
  
<span data-ttu-id="eed26-110">Это значение соответствует значению параметра **Magnification** в диалоговом окне **Shadow** (на вкладке **Главная** в группе **Shape** щелкните Тень **и** нажмите кнопку **Параметры тени).**</span><span class="sxs-lookup"><span data-stu-id="eed26-110">This value corresponds to the value of the **Magnification** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="eed26-111">Чтобы получить ссылку на ячейку ShapeShdwScaleFactor по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="eed26-111">To get a reference to the ShapeShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eed26-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="eed26-112">Cell name:</span></span>  <br/> |<span data-ttu-id="eed26-113">ShapeShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="eed26-113">ShapeShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="eed26-114">Чтобы получить ссылку на ячейку ShapeShdwScaleFactor по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="eed26-114">To get a reference to the ShapeShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eed26-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="eed26-115">Section index:</span></span>  <br/> |<span data-ttu-id="eed26-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eed26-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="eed26-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="eed26-117">Row index:</span></span>  <br/> |<span data-ttu-id="eed26-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="eed26-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="eed26-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="eed26-119">Cell index:</span></span>  <br/> |<span data-ttu-id="eed26-120">**visFillShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="eed26-120">**visFillShdwScaleFactor**</span></span> <br/> |
   

