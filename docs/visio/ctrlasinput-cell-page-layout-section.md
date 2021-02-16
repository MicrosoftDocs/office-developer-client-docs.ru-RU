---
title: CtrlAsInput Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
localization_priority: Normal
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: Определяет, какая фигура является родительской при использовании фигур с окнами управления. Эта ячейка задает поведение для всех фигур на странице рисования.
ms.openlocfilehash: a530c48156043bec0cd58d79aead1a403c17ddce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422623"
---
# <a name="ctrlasinput-cell-page-layout-section"></a><span data-ttu-id="c8d71-104">CtrlAsInput Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="c8d71-104">CtrlAsInput Cell (Page Layout Section)</span></span>

<span data-ttu-id="c8d71-105">Определяет, какая фигура является родительской при использовании фигур с окнами управления.</span><span class="sxs-lookup"><span data-stu-id="c8d71-105">Determines which shape is the parent when using shapes with control handles.</span></span> <span data-ttu-id="c8d71-106">Эта ячейка задает поведение для всех фигур на странице рисования.</span><span class="sxs-lookup"><span data-stu-id="c8d71-106">This cell sets the behavior for all the shapes on the drawing page.</span></span>
  
|<span data-ttu-id="c8d71-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c8d71-107">**Value**</span></span>|<span data-ttu-id="c8d71-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c8d71-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c8d71-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="c8d71-109">TRUE</span></span>  <br/> | <span data-ttu-id="c8d71-110">За установите фигуру, к которую подключено handle-контроля, в качестве родительского.</span><span class="sxs-lookup"><span data-stu-id="c8d71-110">Set the shape that the control handle is connected to as the parent.</span></span>  <br/> |
| <span data-ttu-id="c8d71-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="c8d71-111">FALSE</span></span>  <br/> | <span data-ttu-id="c8d71-112">Значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c8d71-112">The default.</span></span> <span data-ttu-id="c8d71-113">За установите фигуру, содержаную handle для управления, в качестве родительского.</span><span class="sxs-lookup"><span data-stu-id="c8d71-113">Set shape that contains the control handle as the parent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8d71-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c8d71-114">Remarks</span></span>

<span data-ttu-id="c8d71-115">Чтобы получить ссылку на ячейку CtrlAsInput по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="c8d71-115">To get a reference to the CtrlAsInput cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c8d71-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c8d71-116">Cell name:</span></span>  <br/> | <span data-ttu-id="c8d71-117">CtrlAsInput</span><span class="sxs-lookup"><span data-stu-id="c8d71-117">CtrlAsInput</span></span>  <br/> |
   
<span data-ttu-id="c8d71-118">Чтобы получить ссылку на ячейку CtrlAsInput по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c8d71-118">To get a reference to the CtrlAsInput cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c8d71-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c8d71-119">Section index:</span></span>  <br/> |<span data-ttu-id="c8d71-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c8d71-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c8d71-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c8d71-121">Row index:</span></span>  <br/> |<span data-ttu-id="c8d71-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="c8d71-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="c8d71-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c8d71-123">Cell index:</span></span>  <br/> |<span data-ttu-id="c8d71-124">**visPLOCtrlAsInput**</span><span class="sxs-lookup"><span data-stu-id="c8d71-124">**visPLOCtrlAsInput**</span></span> <br/> |
   

