---
title: ImgOffsetY Cell (Foreign Image Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm455
localization_priority: Normal
ms.assetid: 3b2991aa-4722-fe3b-39c5-02d38c4c7efc
description: Определяет расстояние, на которое объект смещен вертикально от начала границы объекта. По умолчанию используется значение 0. Панорамирование объекта с помощью средства Crop изменяет это значение.
ms.openlocfilehash: 908972216a24370bc48990ddc99a36da9274d648
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406740"
---
# <a name="imgoffsety-cell-foreign-image-info-section"></a><span data-ttu-id="b0a1c-105">ImgOffsetY Cell (Foreign Image Info Section)</span><span class="sxs-lookup"><span data-stu-id="b0a1c-105">ImgOffsetY Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="b0a1c-106">Определяет расстояние, на которое объект смещен вертикально от начала границы объекта.</span><span class="sxs-lookup"><span data-stu-id="b0a1c-106">Determines the distance the object is offset vertically from the origin of the object's border.</span></span> <span data-ttu-id="b0a1c-107">По умолчанию используется значение 0.</span><span class="sxs-lookup"><span data-stu-id="b0a1c-107">The default is 0.</span></span> <span data-ttu-id="b0a1c-108">Панорамирование объекта с помощью средства **Crop** изменяет это значение.</span><span class="sxs-lookup"><span data-stu-id="b0a1c-108">Panning the object with the **Crop** tool changes this value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b0a1c-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0a1c-109">Remarks</span></span>

<span data-ttu-id="b0a1c-110">Чтобы получить ссылку на ячейку ImgOffsetY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="b0a1c-110">To get a reference to the ImgOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b0a1c-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b0a1c-111">Cell name:</span></span>  <br/> | <span data-ttu-id="b0a1c-112">ImgOffsetY</span><span class="sxs-lookup"><span data-stu-id="b0a1c-112">ImgOffsetY</span></span>  <br/> |
   
<span data-ttu-id="b0a1c-113">Чтобы получить ссылку на ячейку ImgOffsetY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b0a1c-113">To get a reference to the ImgOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b0a1c-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b0a1c-114">Section index:</span></span>  <br/> |<span data-ttu-id="b0a1c-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b0a1c-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b0a1c-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b0a1c-116">Row index:</span></span>  <br/> |<span data-ttu-id="b0a1c-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="b0a1c-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="b0a1c-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b0a1c-118">Cell index:</span></span>  <br/> |<span data-ttu-id="b0a1c-119">**visFrgnImgOffsetY**</span><span class="sxs-lookup"><span data-stu-id="b0a1c-119">**visFrgnImgOffsetY**</span></span> <br/> |
   

