---
title: LocPinX Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
localization_priority: Normal
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: 'Представляет x-координату пина фигуры (центр вращения) по отношению к происхождению фигуры. Формула определения LocPinX по умолчанию:'
ms.openlocfilehash: 2eb5c328eed3c97652173670c426b83b8c358833
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439242"
---
# <a name="locpinx-cell-shape-transform-section"></a><span data-ttu-id="00901-104">LocPinX Cell (Shape Transform Section)</span><span class="sxs-lookup"><span data-stu-id="00901-104">LocPinX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="00901-105">Представляет  x-координату пина фигуры (центр вращения) по отношению к происхождению фигуры.</span><span class="sxs-lookup"><span data-stu-id="00901-105">Represents the  *x*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="00901-106">Формула определения LocPinX по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="00901-106">The default formula for determining LocPinX is:</span></span> 
  
<span data-ttu-id="00901-107">= \* Ширина 0,5</span><span class="sxs-lookup"><span data-stu-id="00901-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00901-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="00901-108">Remarks</span></span>

<span data-ttu-id="00901-109">Чтобы получить ссылку на ячейку LocPinX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="00901-109">To get a reference to the LocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="00901-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="00901-110">Cell name:</span></span>  <br/> | <span data-ttu-id="00901-111">LocPinX</span><span class="sxs-lookup"><span data-stu-id="00901-111">LocPinX</span></span>  <br/> |
   
<span data-ttu-id="00901-112">Чтобы получить ссылку на ячейку LocPinX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="00901-112">To get a reference to the LocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="00901-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="00901-113">Section index:</span></span>  <br/> |<span data-ttu-id="00901-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="00901-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="00901-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="00901-115">Row index:</span></span>  <br/> |<span data-ttu-id="00901-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="00901-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="00901-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="00901-117">Cell index:</span></span>  <br/> |<span data-ttu-id="00901-118">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="00901-118">**visXFormLocPinX**</span></span> <br/> |
   

