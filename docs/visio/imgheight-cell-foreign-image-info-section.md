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
description: 'Определяет высоту изображения объекта в пределах его границ. По умолчанию используется следующая формула:'
ms.openlocfilehash: 956bc478604fd19d8dfdbb7079e092e9e8a16e7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344935"
---
# <a name="imgheight-cell-foreign-image-info-section"></a><span data-ttu-id="b3d02-104">ImgHeight Cell (Foreign Image Info Section)</span><span class="sxs-lookup"><span data-stu-id="b3d02-104">ImgHeight Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="b3d02-105">Определяет высоту изображения объекта в пределах его границ.</span><span class="sxs-lookup"><span data-stu-id="b3d02-105">Determines the height of the object's image within its border.</span></span> <span data-ttu-id="b3d02-106">По умолчанию используется следующая формула:</span><span class="sxs-lookup"><span data-stu-id="b3d02-106">The default formula is:</span></span>
  
<span data-ttu-id="b3d02-107">= Высота \* 1</span><span class="sxs-lookup"><span data-stu-id="b3d02-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b3d02-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3d02-108">Remarks</span></span>

<span data-ttu-id="b3d02-109">Чтобы получить ссылку на ячейку ImgHeight по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="b3d02-109">To get a reference to the ImgHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3d02-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b3d02-110">Cell name:</span></span>  <br/> | <span data-ttu-id="b3d02-111">ImgHeight</span><span class="sxs-lookup"><span data-stu-id="b3d02-111">ImgHeight</span></span>  <br/> |
   
<span data-ttu-id="b3d02-112">Чтобы получить ссылку на ячейку ImgHeight по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b3d02-112">To get a reference to the ImgHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3d02-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b3d02-113">Section index:</span></span>  <br/> |<span data-ttu-id="b3d02-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b3d02-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b3d02-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b3d02-115">Row index:</span></span>  <br/> |<span data-ttu-id="b3d02-116">**Висровфореигн**</span><span class="sxs-lookup"><span data-stu-id="b3d02-116">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="b3d02-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b3d02-117">Cell index:</span></span>  <br/> |<span data-ttu-id="b3d02-118">**Висфргнимгхеигхт**</span><span class="sxs-lookup"><span data-stu-id="b3d02-118">**visFrgnImgHeight**</span></span> <br/> |
   

