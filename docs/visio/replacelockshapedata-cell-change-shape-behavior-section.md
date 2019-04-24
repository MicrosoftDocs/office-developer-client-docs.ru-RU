---
title: ReplaceLockShapeData Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Указывает, перезаписывает ли значения заданных ячеек в главной фигуре значения (включая локальные значения) фигуры, которые заменяются во время операции замены фигуры. ReplaceLockShapeData определяет, будут ли данные фигуры основной фигуры перезаписывать все данные фигуры заменяемой фигуры.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348344"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a><span data-ttu-id="db6ec-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span><span class="sxs-lookup"><span data-stu-id="db6ec-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="db6ec-105">Указывает, перезаписывает ли значения заданных ячеек в главной фигуре значения (включая локальные значения) фигуры, которые заменяются во время операции замены фигуры.</span><span class="sxs-lookup"><span data-stu-id="db6ec-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="db6ec-106">**ReplaceLockShapeData** определяет, будут ли данные фигуры основной фигуры перезаписывать все данные фигуры заменяемой фигуры.</span><span class="sxs-lookup"><span data-stu-id="db6ec-106">The **ReplaceLockShapeData** determines whether the shape data of the master shape overwrites all of the shape data of the shape being replaced.</span></span> 
  
|<span data-ttu-id="db6ec-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="db6ec-107">**Value**</span></span>|<span data-ttu-id="db6ec-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="db6ec-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="db6ec-109">1 (TRUE)</span><span class="sxs-lookup"><span data-stu-id="db6ec-109">1 (TRUE)</span></span>  <br/> |<span data-ttu-id="db6ec-110">Все строки и значения раздела **данных фигуры** образца фигуры копируются в фигуру замены, а все локальные значения из старой замененной фигуры отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="db6ec-110">All rows and values of the **Shape Data** section of the master shape are copied onto the replacement shape and any local values from the old shape being replaced are discarded.</span></span>  <br/> |
|<span data-ttu-id="db6ec-111">0 (ЛОЖЬ)</span><span class="sxs-lookup"><span data-stu-id="db6ec-111">0 (FALSE)</span></span>  <br/> |<span data-ttu-id="db6ec-112">Строки и значения раздела **данных фигуры** образца фигуры копируются в заменяющую фигуру.</span><span class="sxs-lookup"><span data-stu-id="db6ec-112">The rows and values of the **Shape Data** section of the master shape are copied to the replacement shape.</span></span> <span data-ttu-id="db6ec-113">Все строки в разделе **данных фигуры** старой фигуры с локальными значениями передаются в заменяющую фигуру.</span><span class="sxs-lookup"><span data-stu-id="db6ec-113">Any rows in the **Shape Data** section of the old shape with local values are transferred to the replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db6ec-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="db6ec-114">Remarks</span></span>

<span data-ttu-id="db6ec-115">Чтобы получить ссылку на ячейку **ReplaceLockShapeData** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="db6ec-115">To get a reference to the **ReplaceLockShapeData** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="db6ec-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="db6ec-116">Cell name:</span></span>  <br/> | <span data-ttu-id="db6ec-117">ReplaceLockShapeData</span><span class="sxs-lookup"><span data-stu-id="db6ec-117">ReplaceLockShapeData</span></span>  <br/> |
   
<span data-ttu-id="db6ec-118">Чтобы получить ссылку на ячейку **ReplaceLockShapeData** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="db6ec-118">To get a reference to the **ReplaceLockShapeData** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="db6ec-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="db6ec-119">Section index:</span></span>  <br/> |<span data-ttu-id="db6ec-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="db6ec-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="db6ec-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="db6ec-121">Row index:</span></span>  <br/> |<span data-ttu-id="db6ec-122">**Висровреплацебехавиорс**</span><span class="sxs-lookup"><span data-stu-id="db6ec-122">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="db6ec-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="db6ec-123">Cell index:</span></span>  <br/> |<span data-ttu-id="db6ec-124">**Висреплацелоккшапедата**</span><span class="sxs-lookup"><span data-stu-id="db6ec-124">**visReplaceLockShapeData**</span></span> <br/> |
   

