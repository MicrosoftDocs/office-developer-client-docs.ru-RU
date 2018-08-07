---
title: Ячейка Sharpen (раздел "Свойства изображения")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm910
localization_priority: Normal
ms.assetid: aa2bebfc-a6bb-a6b3-3ae9-8553f96b5738
description: 'Повышает резкость точечного рисунка. Значение по умолчанию: 0%. Резкость изображения достигается путем увеличения контрастности смежных пикселов.'
ms.openlocfilehash: fbc66f8c88cde67ad1f259f8392f6d3bd0457be7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814822"
---
# <a name="sharpen-cell-image-properties-section"></a><span data-ttu-id="93d27-105">Ячейка Sharpen (раздел "Свойства изображения")</span><span class="sxs-lookup"><span data-stu-id="93d27-105">Sharpen Cell (Image Properties Section)</span></span>

<span data-ttu-id="93d27-106">Повышает резкость точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="93d27-106">Sharpens a bitmap image.</span></span> <span data-ttu-id="93d27-107">Значение по умолчанию: 0%.</span><span class="sxs-lookup"><span data-stu-id="93d27-107">The default value is 0%.</span></span> <span data-ttu-id="93d27-108">Резкость изображения достигается путем увеличения контрастности смежных пикселов.</span><span class="sxs-lookup"><span data-stu-id="93d27-108">Sharpening an image focuses it by increasing the contrast of adjacent pixels.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="93d27-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="93d27-109">Remarks</span></span>

<span data-ttu-id="93d27-110">Для получения ссылки на ячейки резкость по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="93d27-110">To get a reference to the Sharpen cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="93d27-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="93d27-111">Cell name:</span></span>  <br/> | <span data-ttu-id="93d27-112">Резкость</span><span class="sxs-lookup"><span data-stu-id="93d27-112">Sharpen</span></span>  <br/> |
   
<span data-ttu-id="93d27-113">Для получения ссылки на ячейки резкость по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="93d27-113">To get a reference to the Sharpen cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="93d27-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="93d27-114">Section index:</span></span>  <br/> |<span data-ttu-id="93d27-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="93d27-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="93d27-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="93d27-116">Row index:</span></span>  <br/> |<span data-ttu-id="93d27-117">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="93d27-117">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="93d27-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="93d27-118">Cell index:</span></span>  <br/> |<span data-ttu-id="93d27-119">**visImageSharpen**</span><span class="sxs-lookup"><span data-stu-id="93d27-119">**visImageSharpen**</span></span> <br/> |
   

