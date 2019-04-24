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
description: Блокирует фигуру таким образом, чтобы ее нельзя было удалить.
ms.openlocfilehash: 0819969c9ba17a52de19341b359b33ceae5b44d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359621"
---
# <a name="lockdelete-cell-protection-section"></a><span data-ttu-id="45c2d-103">LockDelete Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="45c2d-103">LockDelete Cell (Protection Section)</span></span>

<span data-ttu-id="45c2d-104">Блокирует фигуру таким образом, чтобы ее нельзя было удалить.</span><span class="sxs-lookup"><span data-stu-id="45c2d-104">Locks the shape so that it cannot be deleted.</span></span>
  
|<span data-ttu-id="45c2d-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="45c2d-105">**Value**</span></span>|<span data-ttu-id="45c2d-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="45c2d-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="45c2d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="45c2d-107">TRUE</span></span>  <br/> | <span data-ttu-id="45c2d-108">Удаление фигуры невозможно</span><span class="sxs-lookup"><span data-stu-id="45c2d-108">Shape cannot be deleted</span></span>  <br/> |
| <span data-ttu-id="45c2d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="45c2d-109">FALSE</span></span>  <br/> | <span data-ttu-id="45c2d-110">Фигуру можно удалить.</span><span class="sxs-lookup"><span data-stu-id="45c2d-110">Shape can be deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45c2d-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="45c2d-111">Remarks</span></span>

<span data-ttu-id="45c2d-112">Чтобы получить ссылку на ячейку LockDelete по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="45c2d-112">To get a reference to the LockDelete cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="45c2d-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="45c2d-113">Cell name:</span></span>  <br/> | <span data-ttu-id="45c2d-114">LockDelete</span><span class="sxs-lookup"><span data-stu-id="45c2d-114">LockDelete</span></span>  <br/> |
   
<span data-ttu-id="45c2d-115">Чтобы получить ссылку на ячейку LockDelete по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="45c2d-115">To get a reference to the LockDelete cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="45c2d-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="45c2d-116">Section index:</span></span>  <br/> |<span data-ttu-id="45c2d-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="45c2d-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="45c2d-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="45c2d-118">Row index:</span></span>  <br/> |<span data-ttu-id="45c2d-119">**Висровлокк**</span><span class="sxs-lookup"><span data-stu-id="45c2d-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="45c2d-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="45c2d-120">Cell index:</span></span>  <br/> |<span data-ttu-id="45c2d-121">**Вислоккделете**</span><span class="sxs-lookup"><span data-stu-id="45c2d-121">**visLockDelete**</span></span> <br/> |
   

