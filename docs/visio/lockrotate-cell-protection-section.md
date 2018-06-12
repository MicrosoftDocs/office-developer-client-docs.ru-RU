---
title: Ячейка LockRotate (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm655
localization_priority: Normal
ms.assetid: 2d97b31d-9008-307d-273a-1726007eeb34
description: Блокирует плоских фигур с поворот с помощью маркера вращения или слева поворот 90° или 90° команду Поворот вправо.
ms.openlocfilehash: 450fe4786594472d018b705df4678fe636390ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814146"
---
# <a name="lockrotate-cell-protection-section"></a><span data-ttu-id="bd5e6-103">Ячейка LockRotate (раздел Защита)</span><span class="sxs-lookup"><span data-stu-id="bd5e6-103">LockRotate Cell (Protection Section)</span></span>

<span data-ttu-id="bd5e6-104">Блокирует плоских фигур с поворот маркер вращения **Поворот левой 90 °** или **Поворот вправо 90 °** команды.</span><span class="sxs-lookup"><span data-stu-id="bd5e6-104">Locks 2-D shapes against being rotated with the rotation handle or the **Rotate Left 90°** or **Rotate Right 90°** command.</span></span> 
  
|<span data-ttu-id="bd5e6-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="bd5e6-105">**Value**</span></span>|<span data-ttu-id="bd5e6-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bd5e6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bd5e6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="bd5e6-107">TRUE</span></span>  <br/> | <span data-ttu-id="bd5e6-108">Не удается вращаться фигуры.</span><span class="sxs-lookup"><span data-stu-id="bd5e6-108">Shape cannot be rotated.</span></span>  <br/> |
| <span data-ttu-id="bd5e6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="bd5e6-109">FALSE</span></span>  <br/> | <span data-ttu-id="bd5e6-110">Фигура может быть вращаться (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="bd5e6-110">Shape can be rotated (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd5e6-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="bd5e6-111">Remarks</span></span>

<span data-ttu-id="bd5e6-112">Ячейка LockRotate не запрещает одномерной фигуры поворот при перетаскивании конечную точку.</span><span class="sxs-lookup"><span data-stu-id="bd5e6-112">The LockRotate cell does not prevent a 1-D shape from being rotated when an endpoint is dragged.</span></span> <span data-ttu-id="bd5e6-113">Блокировка одномерной фигуры от вращение значение ячейки LockWidth отличное от нуля значение (TRUE).</span><span class="sxs-lookup"><span data-stu-id="bd5e6-113">To lock a 1-D shape against rotation, set the LockWidth cell to a non-zero value (TRUE).</span></span>
  
<span data-ttu-id="bd5e6-114">Чтобы получить ссылку на ячейку LockRotate по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="bd5e6-114">To get a reference to the LockRotate cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd5e6-115">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="bd5e6-115">Cell name:</span></span>  <br/> | <span data-ttu-id="bd5e6-116">LockRotate</span><span class="sxs-lookup"><span data-stu-id="bd5e6-116">LockRotate</span></span>  <br/> |
   
<span data-ttu-id="bd5e6-117">Для получения ссылки на ячейки LockRotate по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="bd5e6-117">To get a reference to the LockRotate cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd5e6-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bd5e6-118">Section index:</span></span>  <br/> |<span data-ttu-id="bd5e6-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bd5e6-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bd5e6-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bd5e6-120">Row index:</span></span>  <br/> |<span data-ttu-id="bd5e6-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="bd5e6-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="bd5e6-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bd5e6-122">Cell index:</span></span>  <br/> |<span data-ttu-id="bd5e6-123">**visLockRotate**</span><span class="sxs-lookup"><span data-stu-id="bd5e6-123">**visLockRotate**</span></span> <br/> |
   

