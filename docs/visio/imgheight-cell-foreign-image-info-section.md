---
title: ImgHeight Cell (Foreign Image Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: 'Определяет высоту изображения объекта в пределах его границы. Формула по умолчанию:'
ms.openlocfilehash: 956bc478604fd19d8dfdbb7079e092e9e8a16e7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411199"
---
# <a name="imgheight-cell-foreign-image-info-section"></a><span data-ttu-id="94b5a-104">ImgHeight Cell (Foreign Image Info Section)</span><span class="sxs-lookup"><span data-stu-id="94b5a-104">ImgHeight Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="94b5a-105">Определяет высоту изображения объекта в пределах его границы.</span><span class="sxs-lookup"><span data-stu-id="94b5a-105">Determines the height of the object's image within its border.</span></span> <span data-ttu-id="94b5a-106">Формула по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="94b5a-106">The default formula is:</span></span>
  
<span data-ttu-id="94b5a-107">= Высота \* 1</span><span class="sxs-lookup"><span data-stu-id="94b5a-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94b5a-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="94b5a-108">Remarks</span></span>

<span data-ttu-id="94b5a-109">Чтобы получить ссылку на ячейку ImgHeight по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="94b5a-109">To get a reference to the ImgHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="94b5a-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="94b5a-110">Cell name:</span></span>  <br/> | <span data-ttu-id="94b5a-111">ImgHeight</span><span class="sxs-lookup"><span data-stu-id="94b5a-111">ImgHeight</span></span>  <br/> |
   
<span data-ttu-id="94b5a-112">Чтобы получить ссылку на ячейку ImgHeight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="94b5a-112">To get a reference to the ImgHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="94b5a-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="94b5a-113">Section index:</span></span>  <br/> |<span data-ttu-id="94b5a-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="94b5a-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="94b5a-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="94b5a-115">Row index:</span></span>  <br/> |<span data-ttu-id="94b5a-116">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="94b5a-116">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="94b5a-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="94b5a-117">Cell index:</span></span>  <br/> |<span data-ttu-id="94b5a-118">**visFrgnImgHeight**</span><span class="sxs-lookup"><span data-stu-id="94b5a-118">**visFrgnImgHeight**</span></span> <br/> |
   

