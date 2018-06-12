---
title: Ячейка NoSnap (раздел геометрии)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: Определяет, привязываются ли другие элементы к пути.
ms.openlocfilehash: 111f3773cb1df9033ed5a7b0b146d40ce6b26df0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814310"
---
# <a name="nosnap-cell-geometry-section"></a><span data-ttu-id="dff0a-103">Ячейка NoSnap (раздел геометрии)</span><span class="sxs-lookup"><span data-stu-id="dff0a-103">NoSnap Cell (Geometry Section)</span></span>

<span data-ttu-id="dff0a-104">Определяет, привязываются ли другие элементы к пути.</span><span class="sxs-lookup"><span data-stu-id="dff0a-104">Determines whether other shapes snap to a path.</span></span>
  
|<span data-ttu-id="dff0a-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="dff0a-105">**Value**</span></span>|<span data-ttu-id="dff0a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dff0a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="dff0a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="dff0a-107">TRUE</span></span>  <br/> | <span data-ttu-id="dff0a-108">Не разрешать другие фигуры, чтобы привязать к этому пути.</span><span class="sxs-lookup"><span data-stu-id="dff0a-108">Do not allow other shapes to snap to this path.</span></span>  <br/> |
| <span data-ttu-id="dff0a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="dff0a-109">FALSE</span></span>  <br/> | <span data-ttu-id="dff0a-110">Разрешить другие фигуры, чтобы привязать к этому пути.</span><span class="sxs-lookup"><span data-stu-id="dff0a-110">Allow other shapes to snap to this path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dff0a-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="dff0a-111">Remarks</span></span>

<span data-ttu-id="dff0a-112">Чтобы получить ссылку на ячейку NoSnap по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="dff0a-112">To get a reference to the NoSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dff0a-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="dff0a-113">Cell name:</span></span>  <br/> | <span data-ttu-id="dff0a-114">Геометрия *i* . NoSnap где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="dff0a-114">Geometry  *i*  .NoSnap            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="dff0a-115">Для получения ссылки на ячейки NoSnap по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="dff0a-115">To get a reference to the NoSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dff0a-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="dff0a-116">Section index:</span></span>  <br/> |<span data-ttu-id="dff0a-117">**visSectionFirstComponent** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dff0a-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="dff0a-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="dff0a-118">Row index:</span></span>  <br/> |<span data-ttu-id="dff0a-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="dff0a-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="dff0a-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="dff0a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="dff0a-121">**visCompNoSnap**</span><span class="sxs-lookup"><span data-stu-id="dff0a-121">**visCompNoSnap**</span></span> <br/> |
   

