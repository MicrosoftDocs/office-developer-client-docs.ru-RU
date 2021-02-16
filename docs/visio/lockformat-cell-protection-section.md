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
description: Блокирует форматирование фигуры, поэтому ее нельзя изменить.
ms.openlocfilehash: e0d1bb8a65b8087136e57bb46ad9f5363da30030
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409680"
---
# <a name="lockformat-cell-protection-section"></a><span data-ttu-id="72fcd-103">LockFormat Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="72fcd-103">LockFormat Cell (Protection Section)</span></span>

<span data-ttu-id="72fcd-104">Блокирует форматирование фигуры, поэтому ее нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="72fcd-104">Locks the formatting of a shape so it cannot be changed.</span></span>
  
|<span data-ttu-id="72fcd-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="72fcd-105">**Value**</span></span>|<span data-ttu-id="72fcd-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="72fcd-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="72fcd-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="72fcd-107">TRUE</span></span>  <br/> | <span data-ttu-id="72fcd-108">Форматирование нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="72fcd-108">Formatting cannot be changed.</span></span>  <br/> |
| <span data-ttu-id="72fcd-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="72fcd-109">FALSE</span></span>  <br/> | <span data-ttu-id="72fcd-110">Форматирование можно изменить.</span><span class="sxs-lookup"><span data-stu-id="72fcd-110">Formatting can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72fcd-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="72fcd-111">Remarks</span></span>

<span data-ttu-id="72fcd-112">Чтобы получить ссылку на ячейку LockFormat по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="72fcd-112">To get a reference to the LockFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="72fcd-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="72fcd-113">Cell name:</span></span>  <br/> | <span data-ttu-id="72fcd-114">LockFormat</span><span class="sxs-lookup"><span data-stu-id="72fcd-114">LockFormat</span></span>  <br/> |
   
<span data-ttu-id="72fcd-115">Чтобы получить ссылку на ячейку LockFormat по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="72fcd-115">To get a reference to the LockFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="72fcd-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="72fcd-116">Section index:</span></span>  <br/> |<span data-ttu-id="72fcd-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="72fcd-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="72fcd-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="72fcd-118">Row index:</span></span>  <br/> |<span data-ttu-id="72fcd-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="72fcd-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="72fcd-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="72fcd-120">Cell index:</span></span>  <br/> |<span data-ttu-id="72fcd-121">**visLockFormat**</span><span class="sxs-lookup"><span data-stu-id="72fcd-121">**visLockFormat**</span></span> <br/> |
   

