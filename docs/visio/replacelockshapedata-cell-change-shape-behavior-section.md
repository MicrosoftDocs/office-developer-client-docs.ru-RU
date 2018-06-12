---
title: Ячейка ReplaceLockShapeData (изменение фигуры поведение раздел)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Указывает ли значений указанного ячеек в основной фигуры перезаписи значений (в том числе локального значения) во время операции замены фигуры в процессе замены фигуры. ReplaceLockShapeData определяет, будет ли данные фигуры основной фигуры перезаписывает все данные фигуры фигура.
ms.openlocfilehash: 07547140c7c96e49663270e51a90fd559afedf29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814601"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a><span data-ttu-id="420ae-104">Ячейка ReplaceLockShapeData (изменение фигуры поведение раздел)</span><span class="sxs-lookup"><span data-stu-id="420ae-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="420ae-105">Указывает ли значений указанного ячеек в основной фигуры перезаписи значений (в том числе локального значения) во время операции замены фигуры в процессе замены фигуры.</span><span class="sxs-lookup"><span data-stu-id="420ae-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="420ae-106">**ReplaceLockShapeData** определяет, будет ли данные фигуры основной фигуры перезаписывает все данные фигуры фигура.</span><span class="sxs-lookup"><span data-stu-id="420ae-106">The **ReplaceLockShapeData** determines whether the shape data of the master shape overwrites all of the shape data of the shape being replaced.</span></span> 
  
|<span data-ttu-id="420ae-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="420ae-107">**Value**</span></span>|<span data-ttu-id="420ae-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="420ae-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="420ae-109">1 (TRUE)</span><span class="sxs-lookup"><span data-stu-id="420ae-109">1 (TRUE)</span></span>  <br/> |<span data-ttu-id="420ae-110">Все строки и значения в разделе **Данных фигуры** основной фигуры, копируются на замещающий фигуру и все локальные значения из старого фигура не учитываются.</span><span class="sxs-lookup"><span data-stu-id="420ae-110">All rows and values of the **Shape Data** section of the master shape are copied onto the replacement shape and any local values from the old shape being replaced are discarded.</span></span>  <br/> |
|<span data-ttu-id="420ae-111">0 (FALSE)</span><span class="sxs-lookup"><span data-stu-id="420ae-111">0 (FALSE)</span></span>  <br/> |<span data-ttu-id="420ae-112">Фигуры замещения копируются строки и значения в разделе **Данных фигуры** основной фигуры.</span><span class="sxs-lookup"><span data-stu-id="420ae-112">The rows and values of the **Shape Data** section of the master shape are copied to the replacement shape.</span></span> <span data-ttu-id="420ae-113">Все строки в разделе **Данных фигуры** старый фигуры на локальном значения переносятся фигуры замещения.</span><span class="sxs-lookup"><span data-stu-id="420ae-113">Any rows in the **Shape Data** section of the old shape with local values are transferred to the replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="420ae-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="420ae-114">Remarks</span></span>

<span data-ttu-id="420ae-115">Для получения ссылки на ячейки **ReplaceLockShapeData** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="420ae-115">To get a reference to the **ReplaceLockShapeData** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="420ae-116">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="420ae-116">Cell name:</span></span>  <br/> | <span data-ttu-id="420ae-117">ReplaceLockShapeData</span><span class="sxs-lookup"><span data-stu-id="420ae-117">ReplaceLockShapeData</span></span>  <br/> |
   
<span data-ttu-id="420ae-118">Для получения ссылки на ячейки **ReplaceLockShapeData** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="420ae-118">To get a reference to the **ReplaceLockShapeData** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="420ae-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="420ae-119">Section index:</span></span>  <br/> |<span data-ttu-id="420ae-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="420ae-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="420ae-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="420ae-121">Row index:</span></span>  <br/> |<span data-ttu-id="420ae-122">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="420ae-122">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="420ae-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="420ae-123">Cell index:</span></span>  <br/> |<span data-ttu-id="420ae-124">**visReplaceLockShapeData**</span><span class="sxs-lookup"><span data-stu-id="420ae-124">**visReplaceLockShapeData**</span></span> <br/> |
   

