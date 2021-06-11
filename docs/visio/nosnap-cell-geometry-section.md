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
description: Определяет, могут ли другие фигуры привязаться к пути.
ms.openlocfilehash: 60a6532aee0f391eb38609f6ed87577e5558d5c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408546"
---
# <a name="nosnap-cell-geometry-section"></a><span data-ttu-id="97935-103">NoSnap Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="97935-103">NoSnap Cell (Geometry Section)</span></span>

<span data-ttu-id="97935-104">Определяет, могут ли другие фигуры привязаться к пути.</span><span class="sxs-lookup"><span data-stu-id="97935-104">Determines whether other shapes snap to a path.</span></span>
  
|<span data-ttu-id="97935-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="97935-105">**Value**</span></span>|<span data-ttu-id="97935-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="97935-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="97935-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="97935-107">TRUE</span></span>  <br/> | <span data-ttu-id="97935-108">Не позволяйте другим фигурам щелкнуть этот путь.</span><span class="sxs-lookup"><span data-stu-id="97935-108">Do not allow other shapes to snap to this path.</span></span>  <br/> |
| <span data-ttu-id="97935-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="97935-109">FALSE</span></span>  <br/> | <span data-ttu-id="97935-110">Разрешить другим фигурам щелкнуть этот путь.</span><span class="sxs-lookup"><span data-stu-id="97935-110">Allow other shapes to snap to this path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97935-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="97935-111">Remarks</span></span>

<span data-ttu-id="97935-112">Чтобы получить ссылку на ячейку NoSnap по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="97935-112">To get a reference to the NoSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97935-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="97935-113">Cell name:</span></span>  <br/> | <span data-ttu-id="97935-114">Геометрия  *i*  . NoSnap, где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="97935-114">Geometry  *i*  .NoSnap            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="97935-115">Чтобы получить ссылку на ячейку NoSnap по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="97935-115">To get a reference to the NoSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97935-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="97935-116">Section index:</span></span>  <br/> |<span data-ttu-id="97935-117">**visSectionFirstComponent** +  *i*, где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="97935-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="97935-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="97935-118">Row index:</span></span>  <br/> |<span data-ttu-id="97935-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="97935-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="97935-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="97935-120">Cell index:</span></span>  <br/> |<span data-ttu-id="97935-121">**visCompNoSnap**</span><span class="sxs-lookup"><span data-stu-id="97935-121">**visCompNoSnap**</span></span> <br/> |
   

