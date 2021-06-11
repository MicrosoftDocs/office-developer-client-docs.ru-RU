---
title: LockRotate Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm655
localization_priority: Normal
ms.assetid: 2d97b31d-9008-307d-273a-1726007eeb34
description: Блокирует 2-D фигуры, которые вращаются с помощью ручки поворота или команды вращать левые 90° или вращать правой 90°.
ms.openlocfilehash: 36da1868e4f974bd19d00e86e31bea96eb8ad5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404675"
---
# <a name="lockrotate-cell-protection-section"></a><span data-ttu-id="ee112-103">LockRotate Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="ee112-103">LockRotate Cell (Protection Section)</span></span>

<span data-ttu-id="ee112-104">Блокирует 2-D фигуры, которые вращаются с помощью ручки поворота или команды вращать левые **90°** или вращать правой **90°.**</span><span class="sxs-lookup"><span data-stu-id="ee112-104">Locks 2-D shapes against being rotated with the rotation handle or the **Rotate Left 90°** or **Rotate Right 90°** command.</span></span> 
  
|<span data-ttu-id="ee112-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ee112-105">**Value**</span></span>|<span data-ttu-id="ee112-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ee112-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ee112-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ee112-107">TRUE</span></span>  <br/> | <span data-ttu-id="ee112-108">Фигура не может быть повернута.</span><span class="sxs-lookup"><span data-stu-id="ee112-108">Shape cannot be rotated.</span></span>  <br/> |
| <span data-ttu-id="ee112-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ee112-109">FALSE</span></span>  <br/> | <span data-ttu-id="ee112-110">Фигура может быть повернута (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="ee112-110">Shape can be rotated (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee112-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="ee112-111">Remarks</span></span>

<span data-ttu-id="ee112-112">Ячейка LockRotate не мешает вращать фигуру 1-D при перетаскивке конечной точки.</span><span class="sxs-lookup"><span data-stu-id="ee112-112">The LockRotate cell does not prevent a 1-D shape from being rotated when an endpoint is dragged.</span></span> <span data-ttu-id="ee112-113">Чтобы заблокировать 1-D-форму от вращения, установите ячейку LockWidth ненулевую величину (TRUE).</span><span class="sxs-lookup"><span data-stu-id="ee112-113">To lock a 1-D shape against rotation, set the LockWidth cell to a non-zero value (TRUE).</span></span>
  
<span data-ttu-id="ee112-114">Чтобы получить ссылку на ячейку LockRotate по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="ee112-114">To get a reference to the LockRotate cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ee112-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ee112-115">Cell name:</span></span>  <br/> | <span data-ttu-id="ee112-116">LockRotate</span><span class="sxs-lookup"><span data-stu-id="ee112-116">LockRotate</span></span>  <br/> |
   
<span data-ttu-id="ee112-117">Чтобы получить ссылку на ячейку LockRotate по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ee112-117">To get a reference to the LockRotate cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ee112-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ee112-118">Section index:</span></span>  <br/> |<span data-ttu-id="ee112-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ee112-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ee112-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ee112-120">Row index:</span></span>  <br/> |<span data-ttu-id="ee112-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="ee112-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="ee112-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ee112-122">Cell index:</span></span>  <br/> |<span data-ttu-id="ee112-123">**visLockRotate**</span><span class="sxs-lookup"><span data-stu-id="ee112-123">**visLockRotate**</span></span> <br/> |
   

