---
title: NoSnap Cell (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: Определяет, привязываются ли другие фигуры к пути.
ms.openlocfilehash: 60a6532aee0f391eb38609f6ed87577e5558d5c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341134"
---
# <a name="nosnap-cell-geometry-section"></a><span data-ttu-id="f01f6-103">NoSnap Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="f01f6-103">NoSnap Cell (Geometry Section)</span></span>

<span data-ttu-id="f01f6-104">Определяет, привязываются ли другие фигуры к пути.</span><span class="sxs-lookup"><span data-stu-id="f01f6-104">Determines whether other shapes snap to a path.</span></span>
  
|<span data-ttu-id="f01f6-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="f01f6-105">**Value**</span></span>|<span data-ttu-id="f01f6-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f01f6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f01f6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f01f6-107">TRUE</span></span>  <br/> | <span data-ttu-id="f01f6-108">Не разрешать привязку других фигур к этому пути.</span><span class="sxs-lookup"><span data-stu-id="f01f6-108">Do not allow other shapes to snap to this path.</span></span>  <br/> |
| <span data-ttu-id="f01f6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f01f6-109">FALSE</span></span>  <br/> | <span data-ttu-id="f01f6-110">РазРешите другим фигурам привязку к этому пути.</span><span class="sxs-lookup"><span data-stu-id="f01f6-110">Allow other shapes to snap to this path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f01f6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f01f6-111">Remarks</span></span>

<span data-ttu-id="f01f6-112">Чтобы получить ссылку на ячейку с функцией Snapin по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="f01f6-112">To get a reference to the NoSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f01f6-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f01f6-113">Cell name:</span></span>  <br/> | <span data-ttu-id="f01f6-114">Геометрия *i* . Snapin, где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f01f6-114">Geometry  *i*  .NoSnap            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f01f6-115">Чтобы получить ссылку на ячейку с параметром Snapin по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f01f6-115">To get a reference to the NoSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f01f6-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f01f6-116">Section index:</span></span>  <br/> |<span data-ttu-id="f01f6-117">**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f01f6-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f01f6-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f01f6-118">Row index:</span></span>  <br/> |<span data-ttu-id="f01f6-119">**Висровкомпонент**</span><span class="sxs-lookup"><span data-stu-id="f01f6-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="f01f6-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f01f6-120">Cell index:</span></span>  <br/> |<span data-ttu-id="f01f6-121">**Вискомпноснап**</span><span class="sxs-lookup"><span data-stu-id="f01f6-121">**visCompNoSnap**</span></span> <br/> |
   

