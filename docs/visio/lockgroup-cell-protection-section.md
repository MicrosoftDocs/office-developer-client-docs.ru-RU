---
title: LockGroup Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
localization_priority: Normal
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: Блокирует группу так, чтобы ее нельзя было разгруппировать.
ms.openlocfilehash: 0cb2c0653780dcb653e5903faaaa0ebf30ea9d69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404311"
---
# <a name="lockgroup-cell-protection-section"></a><span data-ttu-id="db1bf-103">LockGroup Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="db1bf-103">LockGroup Cell (Protection Section)</span></span>

<span data-ttu-id="db1bf-104">Блокирует группу так, чтобы ее нельзя было разгруппировать.</span><span class="sxs-lookup"><span data-stu-id="db1bf-104">Locks a group so that it cannot be ungrouped.</span></span>
  
|<span data-ttu-id="db1bf-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="db1bf-105">**Value**</span></span>|<span data-ttu-id="db1bf-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="db1bf-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="db1bf-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="db1bf-107">TRUE</span></span>  <br/> |<span data-ttu-id="db1bf-108">Группу нельзя разгруппировать.</span><span class="sxs-lookup"><span data-stu-id="db1bf-108">Group cannot be ungrouped.</span></span>  <br/> |
|<span data-ttu-id="db1bf-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="db1bf-109">FALSE</span></span>  <br/> |<span data-ttu-id="db1bf-110">Группу можно разгруппировать.</span><span class="sxs-lookup"><span data-stu-id="db1bf-110">Group can be ungrouped.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db1bf-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="db1bf-111">Remarks</span></span>

<span data-ttu-id="db1bf-112">Установка значения LockGroupCell true также предотвращает удаление фигур, входящего в группу.</span><span class="sxs-lookup"><span data-stu-id="db1bf-112">Setting the LockGroupCell value to TRUE also prevents deletion of any shapes that are members of the group.</span></span>
  
<span data-ttu-id="db1bf-113">Чтобы получить ссылку на ячейку LockGroup по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="db1bf-113">To get a reference to the LockGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db1bf-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="db1bf-114">Cell name:</span></span>  <br/> |<span data-ttu-id="db1bf-115">LockGroup</span><span class="sxs-lookup"><span data-stu-id="db1bf-115">LockGroup</span></span>  <br/> |
   
<span data-ttu-id="db1bf-116">Чтобы получить ссылку на ячейку LockGroup по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="db1bf-116">To get a reference to the LockGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db1bf-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="db1bf-117">Section index:</span></span>  <br/> |<span data-ttu-id="db1bf-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="db1bf-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="db1bf-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="db1bf-119">Row index:</span></span>  <br/> |<span data-ttu-id="db1bf-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="db1bf-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="db1bf-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="db1bf-121">Cell index:</span></span>  <br/> |<span data-ttu-id="db1bf-122">**visLockGroup**</span><span class="sxs-lookup"><span data-stu-id="db1bf-122">**visLockGroup**</span></span> <br/> |
   

