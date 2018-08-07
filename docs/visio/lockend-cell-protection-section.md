---
title: Ячейка LockEnd (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
localization_priority: Normal
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: Блокирует конечную точку (КонецX, КонецY) одномерной фигуры в определенное расположение.
ms.openlocfilehash: d29f07e5b4b77ed2fb8b104769a2fdca55abcc8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814131"
---
# <a name="lockend-cell-protection-section"></a><span data-ttu-id="74446-103">Ячейка LockEnd (раздел "Защита")</span><span class="sxs-lookup"><span data-stu-id="74446-103">LockEnd Cell (Protection Section)</span></span>

<span data-ttu-id="74446-104">Блокирует конечную точку (КонецX, КонецY) одномерной фигуры в определенное расположение.</span><span class="sxs-lookup"><span data-stu-id="74446-104">Locks the endpoint (EndX, EndY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="74446-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="74446-105">**Value**</span></span>|<span data-ttu-id="74446-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="74446-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="74446-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="74446-107">TRUE</span></span>  <br/> | <span data-ttu-id="74446-108">Конечная точка блокировки.</span><span class="sxs-lookup"><span data-stu-id="74446-108">Endpoint is locked.</span></span>  <br/> |
| <span data-ttu-id="74446-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="74446-109">FALSE</span></span>  <br/> | <span data-ttu-id="74446-110">Конечная точка не блокируется.</span><span class="sxs-lookup"><span data-stu-id="74446-110">Endpoint is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74446-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="74446-111">Remarks</span></span>

<span data-ttu-id="74446-112">Чтобы получить ссылку на ячейку LockEnd по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="74446-112">To get a reference to the LockEnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="74446-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="74446-113">Cell name:</span></span>  <br/> | <span data-ttu-id="74446-114">LockEnd</span><span class="sxs-lookup"><span data-stu-id="74446-114">LockEnd</span></span>  <br/> |
   
<span data-ttu-id="74446-115">Для получения ссылки на ячейки LockEnd по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="74446-115">To get a reference to the LockEnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="74446-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="74446-116">Section index:</span></span>  <br/> |<span data-ttu-id="74446-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="74446-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="74446-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="74446-118">Row index:</span></span>  <br/> |<span data-ttu-id="74446-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="74446-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="74446-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="74446-120">Cell index:</span></span>  <br/> |<span data-ttu-id="74446-121">**visLockEnd**</span><span class="sxs-lookup"><span data-stu-id="74446-121">**visLockEnd**</span></span> <br/> |
   

