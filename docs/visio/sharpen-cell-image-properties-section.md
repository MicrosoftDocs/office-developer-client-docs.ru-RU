---
title: Sharpen Cell (Image Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm910
localization_priority: Normal
ms.assetid: aa2bebfc-a6bb-a6b3-3ae9-8553f96b5738
description: Заостряет изображение bitmap. Значение по умолчанию — 0%. Заострение изображения фокусирует его, увеличивая контраст соседних пикселей.
ms.openlocfilehash: e519cf6e5a168b64b4bc8aa083843163a47525ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415924"
---
# <a name="sharpen-cell-image-properties-section"></a><span data-ttu-id="19dbf-105">Sharpen Cell (Image Properties Section)</span><span class="sxs-lookup"><span data-stu-id="19dbf-105">Sharpen Cell (Image Properties Section)</span></span>

<span data-ttu-id="19dbf-106">Заостряет изображение bitmap.</span><span class="sxs-lookup"><span data-stu-id="19dbf-106">Sharpens a bitmap image.</span></span> <span data-ttu-id="19dbf-107">Значение по умолчанию — 0%.</span><span class="sxs-lookup"><span data-stu-id="19dbf-107">The default value is 0%.</span></span> <span data-ttu-id="19dbf-108">Заострение изображения фокусирует его, увеличивая контраст соседних пикселей.</span><span class="sxs-lookup"><span data-stu-id="19dbf-108">Sharpening an image focuses it by increasing the contrast of adjacent pixels.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19dbf-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="19dbf-109">Remarks</span></span>

<span data-ttu-id="19dbf-110">Чтобы получить ссылку на ячейку Sharpen по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="19dbf-110">To get a reference to the Sharpen cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="19dbf-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="19dbf-111">Cell name:</span></span>  <br/> | <span data-ttu-id="19dbf-112">Sharpen</span><span class="sxs-lookup"><span data-stu-id="19dbf-112">Sharpen</span></span>  <br/> |
   
<span data-ttu-id="19dbf-113">Чтобы получить ссылку на ячейку Sharpen по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="19dbf-113">To get a reference to the Sharpen cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="19dbf-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="19dbf-114">Section index:</span></span>  <br/> |<span data-ttu-id="19dbf-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="19dbf-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="19dbf-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="19dbf-116">Row index:</span></span>  <br/> |<span data-ttu-id="19dbf-117">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="19dbf-117">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="19dbf-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="19dbf-118">Cell index:</span></span>  <br/> |<span data-ttu-id="19dbf-119">**visImageSharpen**</span><span class="sxs-lookup"><span data-stu-id="19dbf-119">**visImageSharpen**</span></span> <br/> |
   

