---
title: Ячейка ShdwObliqueAngle (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
localization_priority: Normal
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: Содержит номер, определяющий угол наклона при использовании типа тени по умолчанию.
ms.openlocfilehash: 4549ce7b5202b4649a925b04ea54c0d5df569599
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814851"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a><span data-ttu-id="448fe-103">Ячейка ShdwObliqueAngle (раздел "Свойства страницы")</span><span class="sxs-lookup"><span data-stu-id="448fe-103">ShdwObliqueAngle Cell (Page Properties Section)</span></span>

<span data-ttu-id="448fe-104">Содержит номер, определяющий угол наклона при использовании типа тени по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="448fe-104">Contains a number specifying the angle of oblique direction when applying the default page shadow type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="448fe-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="448fe-105">Remarks</span></span>

<span data-ttu-id="448fe-106">Значение нуль (0) в этой ячейке указывает, что направление угол — вверх и измеряется стрелке.</span><span class="sxs-lookup"><span data-stu-id="448fe-106">A value of zero (0) in this cell indicates that the angle direction is straight up and is measured moving clockwise.</span></span>
  
 <span data-ttu-id="448fe-107">Угол, описанных в этой ячейке используется всякий раз, когда ShapeShdwType ячейки (тип тени для фигуры на странице) задано значение по умолчанию для страницы (**visFSTPageDefault** ), тип теневой наклон.</span><span class="sxs-lookup"><span data-stu-id="448fe-107">The angle described in this cell is used whenever the ShapeShdwType Cell (the shadow type for a shape on the page) is set to Page Default (**visFSTPageDefault** ), and the shadow type is oblique.</span></span> <span data-ttu-id="448fe-108">Тип тени страницы по умолчанию определяется в ячейке ShdwType.</span><span class="sxs-lookup"><span data-stu-id="448fe-108">The default page shadow type is defined in the ShdwType cell.</span></span> 
  
<span data-ttu-id="448fe-109">Чтобы задать это поведение для отдельных фигуры, используйте ShapeShdwObliqueAngle ячейки в разделе формат заполните поля.</span><span class="sxs-lookup"><span data-stu-id="448fe-109">To set this behavior for an individual shape, use the ShapeShdwObliqueAngle cell in the Fill Format section.</span></span>
  
<span data-ttu-id="448fe-110">Чтобы получить ссылку на ячейку ShdwObliqueAngle по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="448fe-110">To get a reference to the ShdwObliqueAngle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="448fe-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="448fe-111">Cell name:</span></span>  <br/> | <span data-ttu-id="448fe-112">ShdwObliqueAngle</span><span class="sxs-lookup"><span data-stu-id="448fe-112">ShdwObliqueAngle</span></span>  <br/> |
   
<span data-ttu-id="448fe-113">Для получения ссылки на ячейки ShdwObliqueAngle по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="448fe-113">To get a reference to the ShdwObliqueAngle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="448fe-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="448fe-114">Section index:</span></span>  <br/> |<span data-ttu-id="448fe-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="448fe-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="448fe-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="448fe-116">Row index:</span></span>  <br/> |<span data-ttu-id="448fe-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="448fe-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="448fe-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="448fe-118">Cell index:</span></span>  <br/> |<span data-ttu-id="448fe-119">**visPageShdwObliqueAngle**</span><span class="sxs-lookup"><span data-stu-id="448fe-119">**visPageShdwObliqueAngle**</span></span> <br/> |
   

