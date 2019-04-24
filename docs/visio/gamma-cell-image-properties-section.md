---
title: Gamma Cell (Image Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm410
localization_priority: Normal
ms.assetid: 3dcaee26-391c-0494-4380-890ee825dc47
description: Корректирует или корректирует интенсивность изображения для определенного устройства вывода, например монитора или сканера. Значение по умолчанию — 1 (без коррекции).
ms.openlocfilehash: d00eb11ff1feffacf0d758bb25cdd56281e91327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315206"
---
# <a name="gamma-cell-image-properties-section"></a><span data-ttu-id="5dc43-104">Gamma Cell (Image Properties Section)</span><span class="sxs-lookup"><span data-stu-id="5dc43-104">Gamma Cell (Image Properties Section)</span></span>

<span data-ttu-id="5dc43-105">Корректирует или корректирует интенсивность изображения для определенного устройства вывода, например монитора или сканера.</span><span class="sxs-lookup"><span data-stu-id="5dc43-105">Adjusts or corrects the intensity of an image for a particular output device, such as a monitor or scanner.</span></span> <span data-ttu-id="5dc43-106">Значение по умолчанию — 1 (без коррекции).</span><span class="sxs-lookup"><span data-stu-id="5dc43-106">The default value is 1 (no correction).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5dc43-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="5dc43-107">Remarks</span></span>

<span data-ttu-id="5dc43-108">Чтобы получить ссылку на ячейку гаммы по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="5dc43-108">To get a reference to the Gamma cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5dc43-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5dc43-109">Cell name:</span></span>  <br/> | <span data-ttu-id="5dc43-110">ГАММА</span><span class="sxs-lookup"><span data-stu-id="5dc43-110">Gamma</span></span>  <br/> |
   
<span data-ttu-id="5dc43-111">Чтобы получить ссылку на ячейку гамма по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5dc43-111">To get a reference to the Gamma cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5dc43-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5dc43-112">Section index:</span></span>  <br/> |<span data-ttu-id="5dc43-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5dc43-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5dc43-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5dc43-114">Row index:</span></span>  <br/> |<span data-ttu-id="5dc43-115">**Висровимаже**</span><span class="sxs-lookup"><span data-stu-id="5dc43-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="5dc43-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5dc43-116">Cell index:</span></span>  <br/> |<span data-ttu-id="5dc43-117">**Висимажегамма**</span><span class="sxs-lookup"><span data-stu-id="5dc43-117">**visImageGamma**</span></span> <br/> |
   

