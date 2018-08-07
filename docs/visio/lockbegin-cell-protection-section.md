---
title: Ячейка LockBegin (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm600
localization_priority: Normal
ms.assetid: cce34aba-caae-51ee-992e-92a490b68ea5
description: Блокирует начальную точку (НачалоX, НачалоY) одномерной фигуры в определенное расположение.
ms.openlocfilehash: c9b9a0e9b69de9b76d78ca7cebfb69116bd2fb72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814113"
---
# <a name="lockbegin-cell-protection-section"></a><span data-ttu-id="66317-103">Ячейка LockBegin (раздел "Защита")</span><span class="sxs-lookup"><span data-stu-id="66317-103">LockBegin Cell (Protection Section)</span></span>

<span data-ttu-id="66317-104">Блокирует начальную точку (НачалоX, НачалоY) одномерной фигуры в определенное расположение.</span><span class="sxs-lookup"><span data-stu-id="66317-104">Locks the begin point (BeginX, BeginY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="66317-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="66317-105">**Value**</span></span>|<span data-ttu-id="66317-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="66317-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="66317-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="66317-107">TRUE</span></span>  <br/> | <span data-ttu-id="66317-108">Заблокированный начальной точки.</span><span class="sxs-lookup"><span data-stu-id="66317-108">Begin point is locked.</span></span>  <br/> |
| <span data-ttu-id="66317-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="66317-109">FALSE</span></span>  <br/> | <span data-ttu-id="66317-110">Начните не блокируется.</span><span class="sxs-lookup"><span data-stu-id="66317-110">Begin is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66317-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="66317-111">Remarks</span></span>

<span data-ttu-id="66317-112">Чтобы получить ссылку на ячейку LockBegin по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="66317-112">To get a reference to the LockBegin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="66317-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="66317-113">Cell name:</span></span>  <br/> | <span data-ttu-id="66317-114">LockBegin</span><span class="sxs-lookup"><span data-stu-id="66317-114">LockBegin</span></span>  <br/> |
   
<span data-ttu-id="66317-115">Для получения ссылки на ячейки LockBegin по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="66317-115">To get a reference to the LockBegin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="66317-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="66317-116">Section index:</span></span>  <br/> |<span data-ttu-id="66317-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="66317-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="66317-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="66317-118">Row index:</span></span>  <br/> |<span data-ttu-id="66317-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="66317-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="66317-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="66317-120">Cell index:</span></span>  <br/> |<span data-ttu-id="66317-121">**visLockBegin**</span><span class="sxs-lookup"><span data-stu-id="66317-121">**visLockBegin**</span></span> <br/> |
   

