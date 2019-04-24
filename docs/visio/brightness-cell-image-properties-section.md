---
title: Brightness Cell (Image Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251608
localization_priority: Normal
ms.assetid: 5bb1cc81-f3fd-a835-1449-233dbd1a62b6
description: НаСтраивает яркость растрового изображения. Чтобы уменьшить яркость изображения, введите значение от 0 до 49% или увеличьте яркость, указав значение от 51% до 100%. Значение по умолчанию — 50%.
ms.openlocfilehash: ae1390d2db3adad86a8afcbeaff88172a841d030
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338026"
---
# <a name="brightness-cell-image-properties-section"></a><span data-ttu-id="56a13-105">Brightness Cell (Image Properties Section)</span><span class="sxs-lookup"><span data-stu-id="56a13-105">Brightness Cell (Image Properties Section)</span></span>

<span data-ttu-id="56a13-106">НаСтраивает яркость растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="56a13-106">Adjusts the brightness of a bitmap image.</span></span> <span data-ttu-id="56a13-107">Чтобы уменьшить яркость изображения, введите значение от 0 до 49% или увеличьте яркость, указав значение от 51% до 100%.</span><span class="sxs-lookup"><span data-stu-id="56a13-107">Decrease brightness of an image by entering a value between 0% and 49%, or increase brightness by entering a value between 51% and 100%.</span></span> <span data-ttu-id="56a13-108">Значение по умолчанию — 50%.</span><span class="sxs-lookup"><span data-stu-id="56a13-108">The default value is 50%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="56a13-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56a13-109">Remarks</span></span>

<span data-ttu-id="56a13-110">Чтобы получить ссылку на ячейку яркости по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="56a13-110">To get a reference to the Brightness cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56a13-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="56a13-111">Cell name:</span></span>  <br/> | <span data-ttu-id="56a13-112">Яркость</span><span class="sxs-lookup"><span data-stu-id="56a13-112">Brightness</span></span>  <br/> |
   
<span data-ttu-id="56a13-113">Чтобы получить ссылку на ячейку "яркость" по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="56a13-113">To get a reference to the Brightness cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56a13-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="56a13-114">Section index:</span></span>  <br/> |<span data-ttu-id="56a13-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="56a13-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="56a13-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="56a13-116">Row index:</span></span>  <br/> |<span data-ttu-id="56a13-117">**Висровимаже**</span><span class="sxs-lookup"><span data-stu-id="56a13-117">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="56a13-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="56a13-118">Cell index:</span></span>  <br/> |<span data-ttu-id="56a13-119">**Висимажебригхтнесс**</span><span class="sxs-lookup"><span data-stu-id="56a13-119">**visImageBrightness**</span></span> <br/> |
   

