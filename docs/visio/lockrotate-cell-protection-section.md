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
description: Отменяет поворот плоских фигур с помощью маркера вращения или поворота влево на 90 ° или повернуть вправо 90 °.
ms.openlocfilehash: 36da1868e4f974bd19d00e86e31bea96eb8ad5bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348275"
---
# <a name="lockrotate-cell-protection-section"></a><span data-ttu-id="48b26-103">LockRotate Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="48b26-103">LockRotate Cell (Protection Section)</span></span>

<span data-ttu-id="48b26-104">Отменяет поворот плоских фигур с помощью маркера вращения или поворота **влево на 90 °** или **повернуть вправо 90 °** .</span><span class="sxs-lookup"><span data-stu-id="48b26-104">Locks 2-D shapes against being rotated with the rotation handle or the **Rotate Left 90°** or **Rotate Right 90°** command.</span></span> 
  
|<span data-ttu-id="48b26-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="48b26-105">**Value**</span></span>|<span data-ttu-id="48b26-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="48b26-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="48b26-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="48b26-107">TRUE</span></span>  <br/> | <span data-ttu-id="48b26-108">Поворот фигуры невозможен.</span><span class="sxs-lookup"><span data-stu-id="48b26-108">Shape cannot be rotated.</span></span>  <br/> |
| <span data-ttu-id="48b26-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="48b26-109">FALSE</span></span>  <br/> | <span data-ttu-id="48b26-110">Фигура может быть повернута (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="48b26-110">Shape can be rotated (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48b26-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="48b26-111">Remarks</span></span>

<span data-ttu-id="48b26-112">Ячейка LockRotate не предотвращает повернутую фигуру 1-D при перетаскивании конечной точки.</span><span class="sxs-lookup"><span data-stu-id="48b26-112">The LockRotate cell does not prevent a 1-D shape from being rotated when an endpoint is dragged.</span></span> <span data-ttu-id="48b26-113">Чтобы заблокировать одноМерное фигуру относительно вращения, установите для ячейки LockWidth значение, отличное от нуля (TRUE).</span><span class="sxs-lookup"><span data-stu-id="48b26-113">To lock a 1-D shape against rotation, set the LockWidth cell to a non-zero value (TRUE).</span></span>
  
<span data-ttu-id="48b26-114">Чтобы получить ссылку на ячейку LockRotate по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="48b26-114">To get a reference to the LockRotate cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="48b26-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="48b26-115">Cell name:</span></span>  <br/> | <span data-ttu-id="48b26-116">LockRotate</span><span class="sxs-lookup"><span data-stu-id="48b26-116">LockRotate</span></span>  <br/> |
   
<span data-ttu-id="48b26-117">Чтобы получить ссылку на ячейку LockRotate по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="48b26-117">To get a reference to the LockRotate cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="48b26-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="48b26-118">Section index:</span></span>  <br/> |<span data-ttu-id="48b26-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="48b26-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="48b26-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="48b26-120">Row index:</span></span>  <br/> |<span data-ttu-id="48b26-121">**Висровлокк**</span><span class="sxs-lookup"><span data-stu-id="48b26-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="48b26-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="48b26-122">Cell index:</span></span>  <br/> |<span data-ttu-id="48b26-123">**Вислоккротате**</span><span class="sxs-lookup"><span data-stu-id="48b26-123">**visLockRotate**</span></span> <br/> |
   

