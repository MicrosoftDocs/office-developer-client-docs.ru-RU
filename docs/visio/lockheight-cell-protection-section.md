---
title: Ячейка LockHeight (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm635
localization_priority: Normal
ms.assetid: 218b957e-5af6-e53b-1453-a84164ae456e
description: Блокирует высоту фигуры таким образом, чтобы его высота не изменяется при изменении размера фигуры.
ms.openlocfilehash: f6afe6037ff3d0810cc532bbc18bb749ee589bb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814137"
---
# <a name="lockheight-cell-protection-section"></a><span data-ttu-id="30388-103">Ячейка LockHeight (раздел "Защита")</span><span class="sxs-lookup"><span data-stu-id="30388-103">LockHeight Cell (Protection Section)</span></span>

<span data-ttu-id="30388-104">Блокирует высоту фигуры таким образом, чтобы его высота не изменяется при изменении размера фигуры.</span><span class="sxs-lookup"><span data-stu-id="30388-104">Locks the height of the shape so that its height remains unchanged when the shape is resized.</span></span>
  
|<span data-ttu-id="30388-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="30388-105">**Value**</span></span>|<span data-ttu-id="30388-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="30388-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="30388-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="30388-107">TRUE</span></span>  <br/> | <span data-ttu-id="30388-108">Высота блокировки.</span><span class="sxs-lookup"><span data-stu-id="30388-108">Height is locked.</span></span>  <br/> |
| <span data-ttu-id="30388-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="30388-109">FALSE</span></span>  <br/> | <span data-ttu-id="30388-110">Высота не блокируется.</span><span class="sxs-lookup"><span data-stu-id="30388-110">Height is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30388-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="30388-111">Remarks</span></span>

<span data-ttu-id="30388-112">Чтобы получить ссылку на ячейку LockHeight по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="30388-112">To get a reference to the LockHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="30388-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="30388-113">Cell name:</span></span>  <br/> | <span data-ttu-id="30388-114">LockHeight</span><span class="sxs-lookup"><span data-stu-id="30388-114">LockHeight</span></span>  <br/> |
   
<span data-ttu-id="30388-115">Для получения ссылки на ячейки LockHeight по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="30388-115">To get a reference to the LockHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="30388-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="30388-116">Section index:</span></span>  <br/> |<span data-ttu-id="30388-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="30388-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="30388-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="30388-118">Row index:</span></span>  <br/> |<span data-ttu-id="30388-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="30388-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="30388-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="30388-120">Cell index:</span></span>  <br/> |<span data-ttu-id="30388-121">**visLockHeight**</span><span class="sxs-lookup"><span data-stu-id="30388-121">**visLockHeight**</span></span> <br/> |
   

