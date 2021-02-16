---
title: LockReplace Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Указывает, может ли фигура участвовать в операции замены (в качестве целевой или заменяемой фигуры).
ms.openlocfilehash: 8b0e3175cacd9b906d91a4185dcd98fad604d8bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404143"
---
# <a name="lockreplace-cell-protection-section"></a><span data-ttu-id="356b9-103">LockReplace Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="356b9-103">LockReplace Cell (Protection Section)</span></span>

<span data-ttu-id="356b9-104">Указывает, может ли фигура участвовать в операции замены (в качестве целевой или заменяемой фигуры).</span><span class="sxs-lookup"><span data-stu-id="356b9-104">Indicates whether a shape can participate in a replacement operation (as either a target or a replacement shape).</span></span> 
  
|<span data-ttu-id="356b9-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="356b9-105">**Value**</span></span>|<span data-ttu-id="356b9-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="356b9-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="356b9-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="356b9-107">TRUE</span></span>  <br/> |<span data-ttu-id="356b9-108">Фигуру нельзя заменить или использовать в качестве замены.</span><span class="sxs-lookup"><span data-stu-id="356b9-108">The shape cannot be replaced or be used as a replacement shape.</span></span>  <br/> <span data-ttu-id="356b9-109">Для фигуры на холсте кнопка "Изменить **фигуру"** отключена при выборе фигуры.</span><span class="sxs-lookup"><span data-stu-id="356b9-109">For a shape on the canvas, the **Change Shape** button is disabled when the shape is selected.</span></span>  <br/> <span data-ttu-id="356b9-110">Для фигуры на трафарете она не появляется в  качестве замены при нажатии кнопки "Изменить фигуру".</span><span class="sxs-lookup"><span data-stu-id="356b9-110">For a shape on a stencil, the shape does not appear as a replacement shape when the **Change Shape** button is clicked.</span></span>  <br/> |
|<span data-ttu-id="356b9-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="356b9-111">FALSE</span></span>  <br/> |<span data-ttu-id="356b9-112">Фигуру можно заменить или использовать в качестве замены.</span><span class="sxs-lookup"><span data-stu-id="356b9-112">The shape can be replaced or used as a replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="356b9-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="356b9-113">Remarks</span></span>

<span data-ttu-id="356b9-114">Чтобы получить ссылку на ячейку **LockReplace** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="356b9-114">To get a reference to the **LockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="356b9-115">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="356b9-115">Cell name:</span></span>  <br/> | <span data-ttu-id="356b9-116">LockReplace</span><span class="sxs-lookup"><span data-stu-id="356b9-116">LockReplace</span></span>  <br/> |
   
<span data-ttu-id="356b9-117">Чтобы получить ссылку на ячейку **LockReplace** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="356b9-117">To get a reference to the **LockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="356b9-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="356b9-118">Section index:</span></span>  <br/> |<span data-ttu-id="356b9-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="356b9-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="356b9-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="356b9-120">Row index:</span></span>  <br/> |<span data-ttu-id="356b9-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="356b9-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="356b9-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="356b9-122">Cell index:</span></span>  <br/> |<span data-ttu-id="356b9-123">**visLockReplace**</span><span class="sxs-lookup"><span data-stu-id="356b9-123">**visLockReplace**</span></span> <br/> |
   

