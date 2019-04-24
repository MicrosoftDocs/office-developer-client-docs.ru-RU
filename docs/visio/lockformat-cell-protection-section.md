---
title: LockFormat Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
localization_priority: Normal
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: Блокирует форматирование фигуры, чтобы его нельзя было изменить.
ms.openlocfilehash: e0d1bb8a65b8087136e57bb46ad9f5363da30030
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359615"
---
# <a name="lockformat-cell-protection-section"></a><span data-ttu-id="b3404-103">LockFormat Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="b3404-103">LockFormat Cell (Protection Section)</span></span>

<span data-ttu-id="b3404-104">Блокирует форматирование фигуры, чтобы его нельзя было изменить.</span><span class="sxs-lookup"><span data-stu-id="b3404-104">Locks the formatting of a shape so it cannot be changed.</span></span>
  
|<span data-ttu-id="b3404-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="b3404-105">**Value**</span></span>|<span data-ttu-id="b3404-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b3404-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b3404-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b3404-107">TRUE</span></span>  <br/> | <span data-ttu-id="b3404-108">Форматирование не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="b3404-108">Formatting cannot be changed.</span></span>  <br/> |
| <span data-ttu-id="b3404-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b3404-109">FALSE</span></span>  <br/> | <span data-ttu-id="b3404-110">Форматирование можно изменить.</span><span class="sxs-lookup"><span data-stu-id="b3404-110">Formatting can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3404-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="b3404-111">Remarks</span></span>

<span data-ttu-id="b3404-112">Чтобы получить ссылку на ячейку LockFormat по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="b3404-112">To get a reference to the LockFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3404-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b3404-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b3404-114">LockFormat</span><span class="sxs-lookup"><span data-stu-id="b3404-114">LockFormat</span></span>  <br/> |
   
<span data-ttu-id="b3404-115">Чтобы получить ссылку на ячейку LockFormat по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b3404-115">To get a reference to the LockFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3404-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b3404-116">Section index:</span></span>  <br/> |<span data-ttu-id="b3404-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b3404-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b3404-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b3404-118">Row index:</span></span>  <br/> |<span data-ttu-id="b3404-119">**Висровлокк**</span><span class="sxs-lookup"><span data-stu-id="b3404-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="b3404-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b3404-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b3404-121">**Вислоккформат**</span><span class="sxs-lookup"><span data-stu-id="b3404-121">**visLockFormat**</span></span> <br/> |
   

