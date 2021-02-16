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
description: Регулировка или исправление интенсивности изображения для конкретного устройства вывода, например монитора или сканера. Значение по умолчанию — 1 (без исправления).
ms.openlocfilehash: d00eb11ff1feffacf0d758bb25cdd56281e91327
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409015"
---
# <a name="gamma-cell-image-properties-section"></a><span data-ttu-id="2e4d4-104">Gamma Cell (Image Properties Section)</span><span class="sxs-lookup"><span data-stu-id="2e4d4-104">Gamma Cell (Image Properties Section)</span></span>

<span data-ttu-id="2e4d4-105">Регулировка или исправление интенсивности изображения для конкретного устройства вывода, например монитора или сканера.</span><span class="sxs-lookup"><span data-stu-id="2e4d4-105">Adjusts or corrects the intensity of an image for a particular output device, such as a monitor or scanner.</span></span> <span data-ttu-id="2e4d4-106">Значение по умолчанию — 1 (без исправления).</span><span class="sxs-lookup"><span data-stu-id="2e4d4-106">The default value is 1 (no correction).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e4d4-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="2e4d4-107">Remarks</span></span>

<span data-ttu-id="2e4d4-108">Чтобы получить ссылку на ячейку Gamma по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="2e4d4-108">To get a reference to the Gamma cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e4d4-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="2e4d4-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2e4d4-110">ГАММА</span><span class="sxs-lookup"><span data-stu-id="2e4d4-110">Gamma</span></span>  <br/> |
   
<span data-ttu-id="2e4d4-111">Чтобы получить ссылку на ячейку Gamma по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="2e4d4-111">To get a reference to the Gamma cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e4d4-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2e4d4-112">Section index:</span></span>  <br/> |<span data-ttu-id="2e4d4-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2e4d4-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2e4d4-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2e4d4-114">Row index:</span></span>  <br/> |<span data-ttu-id="2e4d4-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="2e4d4-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="2e4d4-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2e4d4-116">Cell index:</span></span>  <br/> |<span data-ttu-id="2e4d4-117">**visImageGaвяз**</span><span class="sxs-lookup"><span data-stu-id="2e4d4-117">**visImageGamma**</span></span> <br/> |
   

