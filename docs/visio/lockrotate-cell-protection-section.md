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
description: Блокирует поворачивать двухградивные фигуры с помощью вращающейся оси или команды Поворота влево на 90° или 90° вправо.
ms.openlocfilehash: 36da1868e4f974bd19d00e86e31bea96eb8ad5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404675"
---
# <a name="lockrotate-cell-protection-section"></a><span data-ttu-id="22684-103">LockRotate Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="22684-103">LockRotate Cell (Protection Section)</span></span>

<span data-ttu-id="22684-104">Блокирует поворачивать двухградивные фигуры с помощью вращающейся оси или команды Поворота влево **на 90°** или **90°** вправо.</span><span class="sxs-lookup"><span data-stu-id="22684-104">Locks 2-D shapes against being rotated with the rotation handle or the **Rotate Left 90°** or **Rotate Right 90°** command.</span></span> 
  
|<span data-ttu-id="22684-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="22684-105">**Value**</span></span>|<span data-ttu-id="22684-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="22684-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="22684-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="22684-107">TRUE</span></span>  <br/> | <span data-ttu-id="22684-108">Фигура не может быть повернута.</span><span class="sxs-lookup"><span data-stu-id="22684-108">Shape cannot be rotated.</span></span>  <br/> |
| <span data-ttu-id="22684-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="22684-109">FALSE</span></span>  <br/> | <span data-ttu-id="22684-110">Фигуру можно поворачивать (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="22684-110">Shape can be rotated (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22684-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="22684-111">Remarks</span></span>

<span data-ttu-id="22684-112">Ячейка LockRotate не препятствует повороту 1-D-фигуры при перетаскивке конечной точки.</span><span class="sxs-lookup"><span data-stu-id="22684-112">The LockRotate cell does not prevent a 1-D shape from being rotated when an endpoint is dragged.</span></span> <span data-ttu-id="22684-113">Чтобы заблокировать 1-D-фигуру от поворота, установите для ячейки LockWidth ненулевой значение (TRUE).</span><span class="sxs-lookup"><span data-stu-id="22684-113">To lock a 1-D shape against rotation, set the LockWidth cell to a non-zero value (TRUE).</span></span>
  
<span data-ttu-id="22684-114">Чтобы получить ссылку на ячейку LockRotate по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="22684-114">To get a reference to the LockRotate cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="22684-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="22684-115">Cell name:</span></span>  <br/> | <span data-ttu-id="22684-116">LockRotate</span><span class="sxs-lookup"><span data-stu-id="22684-116">LockRotate</span></span>  <br/> |
   
<span data-ttu-id="22684-117">Чтобы получить ссылку на ячейку LockRotate по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="22684-117">To get a reference to the LockRotate cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="22684-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="22684-118">Section index:</span></span>  <br/> |<span data-ttu-id="22684-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="22684-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="22684-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="22684-120">Row index:</span></span>  <br/> |<span data-ttu-id="22684-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="22684-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="22684-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="22684-122">Cell index:</span></span>  <br/> |<span data-ttu-id="22684-123">**visLockRotate**</span><span class="sxs-lookup"><span data-stu-id="22684-123">**visLockRotate**</span></span> <br/> |
   

