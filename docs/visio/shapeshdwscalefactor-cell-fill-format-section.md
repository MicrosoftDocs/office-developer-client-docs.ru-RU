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
description: Указывает процентное значение, на которое можно увеличить или уменьшить тень фигуры.
ms.openlocfilehash: 5862b61ca1f5df25ca97bf8742b9e20bf45091a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349163"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a><span data-ttu-id="5fca2-103">ShapeShdwScaleFactor Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="5fca2-103">ShapeShdwScaleFactor Cell (Fill Format Section)</span></span>

<span data-ttu-id="5fca2-104">Указывает процентное значение, на которое можно увеличить или уменьшить тень фигуры.</span><span class="sxs-lookup"><span data-stu-id="5fca2-104">Specifies the percentage by which the shadow of a shape can be enlarged or reduced.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5fca2-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="5fca2-105">Remarks</span></span>

<span data-ttu-id="5fca2-106">Каждая теневая копия имеет затененный ПИН-код, указывающий на тень, соответствующую ПИН-коду фигуры.</span><span class="sxs-lookup"><span data-stu-id="5fca2-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="5fca2-107">Например, если ПИН-код фигуры находится в центре фигуры, то затененное расположение ПИН-кода будет точкой в центре тени.</span><span class="sxs-lookup"><span data-stu-id="5fca2-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="5fca2-108">При применении масштаба к простым теням, увеличение выравнивается по центру в затененном расположении; При применении масштаба к теням теней наклон применяется при увеличении наклона.</span><span class="sxs-lookup"><span data-stu-id="5fca2-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
<span data-ttu-id="5fca2-109">Чтобы задать это значение для всех фигур на странице, используйте ячейку ShdwScaleFactor в разделе Свойства страницы.</span><span class="sxs-lookup"><span data-stu-id="5fca2-109">To set this value for all the shapes on a page, use the ShdwScaleFactor cell in the Page Properties section.</span></span>
  
<span data-ttu-id="5fca2-110">Это значение соответствует значению параметра " **масштаб** " в диалоговом окне " **тень** " (на вкладке **Главная** , в группе **фигур** выберите пункт **тень**и нажмите кнопку **параметры тени**).</span><span class="sxs-lookup"><span data-stu-id="5fca2-110">This value corresponds to the value of the **Magnification** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="5fca2-111">Чтобы получить ссылку на ячейку ShapeShdwScaleFactor по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="5fca2-111">To get a reference to the ShapeShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5fca2-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5fca2-112">Cell name:</span></span>  <br/> |<span data-ttu-id="5fca2-113">ShapeShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="5fca2-113">ShapeShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="5fca2-114">Чтобы получить ссылку на ячейку ShapeShdwScaleFactor по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5fca2-114">To get a reference to the ShapeShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5fca2-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5fca2-115">Section index:</span></span>  <br/> |<span data-ttu-id="5fca2-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5fca2-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5fca2-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5fca2-117">Row index:</span></span>  <br/> |<span data-ttu-id="5fca2-118">**Висровфилл**</span><span class="sxs-lookup"><span data-stu-id="5fca2-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="5fca2-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5fca2-119">Cell index:</span></span>  <br/> |<span data-ttu-id="5fca2-120">**Висфиллшдвскалефактор**</span><span class="sxs-lookup"><span data-stu-id="5fca2-120">**visFillShdwScaleFactor**</span></span> <br/> |
   

