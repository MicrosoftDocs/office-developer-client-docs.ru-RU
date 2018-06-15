---
title: Ячейка LockGroup (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
localization_priority: Normal
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: Блокирует группу, его нельзя разгруппировать.
ms.openlocfilehash: 4d09d514a3fff8ada40c67eb9cd9537539a1039a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19814150"
---
# <a name="lockgroup-cell-protection-section"></a><span data-ttu-id="fb115-103">Ячейка LockGroup (раздел Защита)</span><span class="sxs-lookup"><span data-stu-id="fb115-103">LockGroup Cell (Protection Section)</span></span>

<span data-ttu-id="fb115-104">Блокирует группу, его нельзя разгруппировать.</span><span class="sxs-lookup"><span data-stu-id="fb115-104">Locks a group so that it cannot be ungrouped.</span></span>
  
|<span data-ttu-id="fb115-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="fb115-105">**Value**</span></span>|<span data-ttu-id="fb115-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fb115-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fb115-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="fb115-107">TRUE</span></span>  <br/> |<span data-ttu-id="fb115-108">Группа не может быть без группировки.</span><span class="sxs-lookup"><span data-stu-id="fb115-108">Group cannot be ungrouped.</span></span>  <br/> |
|<span data-ttu-id="fb115-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="fb115-109">FALSE</span></span>  <br/> |<span data-ttu-id="fb115-110">Группа может быть без группировки.</span><span class="sxs-lookup"><span data-stu-id="fb115-110">Group can be ungrouped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb115-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="fb115-111">Remarks</span></span>

<span data-ttu-id="fb115-112">Значение LockGroupCell значение TRUE, также будет отключено удаления любой фигуры, которые являются участниками группы.</span><span class="sxs-lookup"><span data-stu-id="fb115-112">Setting the LockGroupCell value to TRUE also prevents deletion of any shapes that are members of the group.</span></span>
  
<span data-ttu-id="fb115-113">Чтобы получить ссылку на ячейку LockGroup по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fb115-113">To get a reference to the LockGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fb115-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="fb115-114">Cell name:</span></span>  <br/> |<span data-ttu-id="fb115-115">LockGroup</span><span class="sxs-lookup"><span data-stu-id="fb115-115">LockGroup</span></span>  <br/> |
   
<span data-ttu-id="fb115-116">Для получения ссылки на ячейки LockGroup по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="fb115-116">To get a reference to the LockGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fb115-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fb115-117">Section index:</span></span>  <br/> |<span data-ttu-id="fb115-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fb115-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="fb115-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fb115-119">Row index:</span></span>  <br/> |<span data-ttu-id="fb115-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="fb115-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="fb115-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fb115-121">Cell index:</span></span>  <br/> |<span data-ttu-id="fb115-122">**visLockGroup**</span><span class="sxs-lookup"><span data-stu-id="fb115-122">**visLockGroup**</span></span> <br/> |
   

