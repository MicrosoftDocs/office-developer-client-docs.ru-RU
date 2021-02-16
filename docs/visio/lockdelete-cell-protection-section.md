---
title: LockDelete Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
localization_priority: Normal
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: Блокирует фигуру, чтобы ее нельзя было удалить.
ms.openlocfilehash: 0819969c9ba17a52de19341b359b33ceae5b44d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423141"
---
# <a name="lockdelete-cell-protection-section"></a><span data-ttu-id="f88d8-103">LockDelete Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="f88d8-103">LockDelete Cell (Protection Section)</span></span>

<span data-ttu-id="f88d8-104">Блокирует фигуру, чтобы ее нельзя было удалить.</span><span class="sxs-lookup"><span data-stu-id="f88d8-104">Locks the shape so that it cannot be deleted.</span></span>
  
|<span data-ttu-id="f88d8-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f88d8-105">**Value**</span></span>|<span data-ttu-id="f88d8-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f88d8-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f88d8-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f88d8-107">TRUE</span></span>  <br/> | <span data-ttu-id="f88d8-108">Фигура не может быть удалена</span><span class="sxs-lookup"><span data-stu-id="f88d8-108">Shape cannot be deleted</span></span>  <br/> |
| <span data-ttu-id="f88d8-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f88d8-109">FALSE</span></span>  <br/> | <span data-ttu-id="f88d8-110">Фигуру можно удалить.</span><span class="sxs-lookup"><span data-stu-id="f88d8-110">Shape can be deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f88d8-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="f88d8-111">Remarks</span></span>

<span data-ttu-id="f88d8-112">Чтобы получить ссылку на ячейку LockDelete по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="f88d8-112">To get a reference to the LockDelete cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f88d8-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f88d8-113">Cell name:</span></span>  <br/> | <span data-ttu-id="f88d8-114">LockDelete</span><span class="sxs-lookup"><span data-stu-id="f88d8-114">LockDelete</span></span>  <br/> |
   
<span data-ttu-id="f88d8-115">Чтобы получить ссылку на ячейку LockDelete по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f88d8-115">To get a reference to the LockDelete cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f88d8-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f88d8-116">Section index:</span></span>  <br/> |<span data-ttu-id="f88d8-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f88d8-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f88d8-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f88d8-118">Row index:</span></span>  <br/> |<span data-ttu-id="f88d8-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="f88d8-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="f88d8-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f88d8-120">Cell index:</span></span>  <br/> |<span data-ttu-id="f88d8-121">**visLockDelete**</span><span class="sxs-lookup"><span data-stu-id="f88d8-121">**visLockDelete**</span></span> <br/> |
   

