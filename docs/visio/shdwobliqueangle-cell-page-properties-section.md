---
title: ShdwObliqueAngle Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
localization_priority: Normal
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: Содержит число, определяющее угол наклона при применении типа тени страницы по умолчанию.
ms.openlocfilehash: 2eca29bbc735c7101ca82a2f26db30b2e344b8e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349065"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a><span data-ttu-id="2c216-103">ShdwObliqueAngle Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="2c216-103">ShdwObliqueAngle Cell (Page Properties Section)</span></span>

<span data-ttu-id="2c216-104">Содержит число, определяющее угол наклона при применении типа тени страницы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c216-104">Contains a number specifying the angle of oblique direction when applying the default page shadow type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2c216-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="2c216-105">Remarks</span></span>

<span data-ttu-id="2c216-106">Значение ноль (0) в этой ячейке указывает на то, что направление угла является прямолинейным и измеряется при перемещении по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="2c216-106">A value of zero (0) in this cell indicates that the angle direction is straight up and is measured moving clockwise.</span></span>
  
 <span data-ttu-id="2c216-107">Угол, описанный в этой ячейке, используется всякий раз, когда ячейка ShapeShdwType (тип тени для фигуры на странице) имеет значение Default страницы (**висфстпажедефаулт** ), а тип тени — наклонный.</span><span class="sxs-lookup"><span data-stu-id="2c216-107">The angle described in this cell is used whenever the ShapeShdwType Cell (the shadow type for a shape on the page) is set to Page Default (**visFSTPageDefault** ), and the shadow type is oblique.</span></span> <span data-ttu-id="2c216-108">Тип тени страницы по умолчанию определяется в ячейке ShdwType.</span><span class="sxs-lookup"><span data-stu-id="2c216-108">The default page shadow type is defined in the ShdwType cell.</span></span> 
  
<span data-ttu-id="2c216-109">Чтобы задать такое поведение для отдельной фигуры, используйте ячейку ShapeShdwObliqueAngle в разделе Формат заливки.</span><span class="sxs-lookup"><span data-stu-id="2c216-109">To set this behavior for an individual shape, use the ShapeShdwObliqueAngle cell in the Fill Format section.</span></span>
  
<span data-ttu-id="2c216-110">Чтобы получить ссылку на ячейку ShdwObliqueAngle по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="2c216-110">To get a reference to the ShdwObliqueAngle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2c216-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="2c216-111">Cell name:</span></span>  <br/> | <span data-ttu-id="2c216-112">ShdwObliqueAngle</span><span class="sxs-lookup"><span data-stu-id="2c216-112">ShdwObliqueAngle</span></span>  <br/> |
   
<span data-ttu-id="2c216-113">Чтобы получить ссылку на ячейку ShdwObliqueAngle по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="2c216-113">To get a reference to the ShdwObliqueAngle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2c216-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2c216-114">Section index:</span></span>  <br/> |<span data-ttu-id="2c216-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2c216-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2c216-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2c216-116">Row index:</span></span>  <br/> |<span data-ttu-id="2c216-117">**Висровпаже**</span><span class="sxs-lookup"><span data-stu-id="2c216-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="2c216-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2c216-118">Cell index:</span></span>  <br/> |<span data-ttu-id="2c216-119">**Виспажешдвобликуеангле**</span><span class="sxs-lookup"><span data-stu-id="2c216-119">**visPageShdwObliqueAngle**</span></span> <br/> |
   

