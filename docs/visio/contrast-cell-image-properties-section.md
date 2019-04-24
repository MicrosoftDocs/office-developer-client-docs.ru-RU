---
title: Contrast Cell (Image Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm200
localization_priority: Normal
ms.assetid: f0e4c644-c646-9649-c697-82feb02f5e29
description: НаСтраивает контрастность растрового изображения. Чтобы уменьшить контрастность изображения, введите значение от 0 до 49% или увеличьте контраст, указав значение между 51% и 100%. Значение по умолчанию — 50%.
ms.openlocfilehash: f0a27090ea1ec96bf11726ae641ff918dd581e2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319022"
---
# <a name="contrast-cell-image-properties-section"></a><span data-ttu-id="65443-105">Contrast Cell (Image Properties Section)</span><span class="sxs-lookup"><span data-stu-id="65443-105">Contrast Cell (Image Properties Section)</span></span>

<span data-ttu-id="65443-106">НаСтраивает контрастность растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="65443-106">Adjusts the contrast of a bitmap image.</span></span> <span data-ttu-id="65443-107">Чтобы уменьшить контрастность изображения, введите значение от 0 до 49% или увеличьте контраст, указав значение между 51% и 100%.</span><span class="sxs-lookup"><span data-stu-id="65443-107">Decrease the contrast of an image by entering a value between 0% and 49%, or increase the contrast by entering a value between 51% and 100%.</span></span> <span data-ttu-id="65443-108">Значение по умолчанию — 50%.</span><span class="sxs-lookup"><span data-stu-id="65443-108">The default value is 50%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="65443-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="65443-109">Remarks</span></span>

<span data-ttu-id="65443-110">Чтобы получить ссылку на ячейку контрастности по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="65443-110">To get a reference to the Contrast cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="65443-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="65443-111">Cell name:</span></span>  <br/> | <span data-ttu-id="65443-112">Контраст</span><span class="sxs-lookup"><span data-stu-id="65443-112">Contrast</span></span>  <br/> |
   
<span data-ttu-id="65443-113">Чтобы получить ссылку на ячейку контрастности по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="65443-113">To get a reference to the Contrast cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="65443-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="65443-114">Section index:</span></span>  <br/> |<span data-ttu-id="65443-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="65443-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="65443-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="65443-116">Row index:</span></span>  <br/> |<span data-ttu-id="65443-117">**Висровимаже**</span><span class="sxs-lookup"><span data-stu-id="65443-117">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="65443-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="65443-118">Cell index:</span></span>  <br/> |<span data-ttu-id="65443-119">**Висимажеконтраст**</span><span class="sxs-lookup"><span data-stu-id="65443-119">**visImageContrast**</span></span> <br/> |
   

