---
title: Ячейка LockVtxEdit (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
localization_priority: Normal
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: Блокирует грани фигуры, их нельзя изменить.
ms.openlocfilehash: 3766df62bb85e1470ad0fa46274b9bbbd96b8406
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19814170"
---
# <a name="lockvtxedit-cell-protection-section"></a><span data-ttu-id="59874-103">Ячейка LockVtxEdit (раздел "Защита")</span><span class="sxs-lookup"><span data-stu-id="59874-103">LockVtxEdit Cell (Protection Section)</span></span>

<span data-ttu-id="59874-104">Блокирует грани фигуры, их нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="59874-104">Locks the vertices of a shape so that they cannot be edited.</span></span>
  
|<span data-ttu-id="59874-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="59874-105">**Value**</span></span>|<span data-ttu-id="59874-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="59874-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="59874-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="59874-107">TRUE</span></span>  <br/> |<span data-ttu-id="59874-108">Невозможно изменить вершин.</span><span class="sxs-lookup"><span data-stu-id="59874-108">Vertices cannot be edited.</span></span>  <br/> |
|<span data-ttu-id="59874-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="59874-109">FALSE</span></span>  <br/> |<span data-ttu-id="59874-110">Можно изменять вершины.</span><span class="sxs-lookup"><span data-stu-id="59874-110">Vertices can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59874-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="59874-111">Remarks</span></span>

<span data-ttu-id="59874-112">Чтобы получить ссылку на ячейку LockVtxEdit по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="59874-112">To get a reference to the LockVtxEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59874-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="59874-113">Cell name:</span></span>  <br/> |<span data-ttu-id="59874-114">LockVtxEdit</span><span class="sxs-lookup"><span data-stu-id="59874-114">LockVtxEdit</span></span>  <br/> |
   
<span data-ttu-id="59874-115">Для получения ссылки на ячейки LockVtxEdit по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="59874-115">To get a reference to the LockVtxEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59874-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="59874-116">Section index:</span></span>  <br/> |<span data-ttu-id="59874-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="59874-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="59874-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="59874-118">Row index:</span></span>  <br/> |<span data-ttu-id="59874-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="59874-119">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="59874-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="59874-120">Cell index:</span></span>  <br/> |<span data-ttu-id="59874-121">**visLockVtxEdit**</span><span class="sxs-lookup"><span data-stu-id="59874-121">**visLockVtxEdit**</span></span> <br/> |
   

