---
title: Denoise Cell (Image Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm225
localization_priority: Normal
ms.assetid: e305585f-f0d8-0494-91d4-0c76929dc170
description: Удаляет шум (пиксели с случайно распределенными уровнями цвета) из точеченого изображения. Значение по умолчанию — 0%.
ms.openlocfilehash: f970fde22e864239ea3f3f9bcb704e7f4692e9cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415806"
---
# <a name="denoise-cell-image-properties-section"></a><span data-ttu-id="c10d7-104">Denoise Cell (Image Properties Section)</span><span class="sxs-lookup"><span data-stu-id="c10d7-104">Denoise Cell (Image Properties Section)</span></span>

<span data-ttu-id="c10d7-105">Удаляет шум (пиксели с случайно распределенными уровнями цвета) из точеченого изображения.</span><span class="sxs-lookup"><span data-stu-id="c10d7-105">Removes noise (pixels with randomly distributed color levels) from a bitmap image.</span></span> <span data-ttu-id="c10d7-106">Значение по умолчанию — 0%.</span><span class="sxs-lookup"><span data-stu-id="c10d7-106">The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c10d7-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="c10d7-107">Remarks</span></span>

<span data-ttu-id="c10d7-108">Чтобы получить ссылку на ячейку Denoise по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="c10d7-108">To get a reference to the Denoise cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c10d7-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c10d7-109">Cell name:</span></span>  <br/> | <span data-ttu-id="c10d7-110">Denoise</span><span class="sxs-lookup"><span data-stu-id="c10d7-110">Denoise</span></span>  <br/> |
   
<span data-ttu-id="c10d7-111">Чтобы получить ссылку на ячейку Denoise по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c10d7-111">To get a reference to the Denoise cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c10d7-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c10d7-112">Section index:</span></span>  <br/> |<span data-ttu-id="c10d7-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c10d7-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c10d7-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c10d7-114">Row index:</span></span>  <br/> |<span data-ttu-id="c10d7-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="c10d7-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="c10d7-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c10d7-116">Cell index:</span></span>  <br/> |<span data-ttu-id="c10d7-117">**visImageDenoise**</span><span class="sxs-lookup"><span data-stu-id="c10d7-117">**visImageDenoise**</span></span> <br/> |
   

