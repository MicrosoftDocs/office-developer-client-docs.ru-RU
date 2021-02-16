---
title: ReplaceLockShapeData Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Указывает, переоценили ли значения указанных ячеек в фигуре хозяина значения (включая локальные значения) фигуры, заменяемой во время операции замены фигуры. ReplaceLockShapeData определяет, переопределяются ли все данные фигуры заменяемой фигуры.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408875"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a><span data-ttu-id="f8637-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span><span class="sxs-lookup"><span data-stu-id="f8637-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="f8637-105">Указывает, переоценили ли значения указанных ячеек в фигуре хозяина значения (включая локальные значения) фигуры, заменяемой во время операции замены фигуры.</span><span class="sxs-lookup"><span data-stu-id="f8637-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="f8637-106">**ReplaceLockShapeData** определяет, переопределяются ли все данные фигуры заменяемой фигуры.</span><span class="sxs-lookup"><span data-stu-id="f8637-106">The **ReplaceLockShapeData** determines whether the shape data of the master shape overwrites all of the shape data of the shape being replaced.</span></span> 
  
|<span data-ttu-id="f8637-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f8637-107">**Value**</span></span>|<span data-ttu-id="f8637-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f8637-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f8637-109">1 (TRUE)</span><span class="sxs-lookup"><span data-stu-id="f8637-109">1 (TRUE)</span></span>  <br/> |<span data-ttu-id="f8637-110">Все строки и значения раздела **"Данные** фигуры" фигуры копируется на заменяемую фигуру, а все локальные значения из заменяемой старой фигуры удаляются.</span><span class="sxs-lookup"><span data-stu-id="f8637-110">All rows and values of the **Shape Data** section of the master shape are copied onto the replacement shape and any local values from the old shape being replaced are discarded.</span></span>  <br/> |
|<span data-ttu-id="f8637-111">0 (FALSE)</span><span class="sxs-lookup"><span data-stu-id="f8637-111">0 (FALSE)</span></span>  <br/> |<span data-ttu-id="f8637-112">Строки и значения раздела **"Данные** фигуры" фигуры копируется в заменяемую фигуру.</span><span class="sxs-lookup"><span data-stu-id="f8637-112">The rows and values of the **Shape Data** section of the master shape are copied to the replacement shape.</span></span> <span data-ttu-id="f8637-113">Все строки в разделе **"Данные фигуры"** старой фигуры с локальными значениями переносятся на заменяемую фигуру.</span><span class="sxs-lookup"><span data-stu-id="f8637-113">Any rows in the **Shape Data** section of the old shape with local values are transferred to the replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8637-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f8637-114">Remarks</span></span>

<span data-ttu-id="f8637-115">Чтобы получить ссылку на ячейку **ReplaceLockShapeData** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="f8637-115">To get a reference to the **ReplaceLockShapeData** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8637-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f8637-116">Cell name:</span></span>  <br/> | <span data-ttu-id="f8637-117">ReplaceLockShapeData</span><span class="sxs-lookup"><span data-stu-id="f8637-117">ReplaceLockShapeData</span></span>  <br/> |
   
<span data-ttu-id="f8637-118">Чтобы получить ссылку на ячейку **ReplaceLockShapeData** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f8637-118">To get a reference to the **ReplaceLockShapeData** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8637-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f8637-119">Section index:</span></span>  <br/> |<span data-ttu-id="f8637-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f8637-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f8637-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f8637-121">Row index:</span></span>  <br/> |<span data-ttu-id="f8637-122">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="f8637-122">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="f8637-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f8637-123">Cell index:</span></span>  <br/> |<span data-ttu-id="f8637-124">**visReplaceLockShapeData**</span><span class="sxs-lookup"><span data-stu-id="f8637-124">**visReplaceLockShapeData**</span></span> <br/> |
   

