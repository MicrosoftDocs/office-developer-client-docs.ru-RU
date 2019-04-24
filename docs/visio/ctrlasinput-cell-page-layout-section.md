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
description: Определяет, какая фигура является родительской, при использовании фигур с управляющими маркерами. В этой ячейке задается поведение всех фигур на странице документа.
ms.openlocfilehash: a530c48156043bec0cd58d79aead1a403c17ddce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282910"
---
# <a name="ctrlasinput-cell-page-layout-section"></a><span data-ttu-id="6d3a7-104">CtrlAsInput Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-104">CtrlAsInput Cell (Page Layout Section)</span></span>

<span data-ttu-id="6d3a7-105">Определяет, какая фигура является родительской, при использовании фигур с управляющими маркерами.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-105">Determines which shape is the parent when using shapes with control handles.</span></span> <span data-ttu-id="6d3a7-106">В этой ячейке задается поведение всех фигур на странице документа.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-106">This cell sets the behavior for all the shapes on the drawing page.</span></span>
  
|<span data-ttu-id="6d3a7-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="6d3a7-107">**Value**</span></span>|<span data-ttu-id="6d3a7-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6d3a7-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6d3a7-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="6d3a7-109">TRUE</span></span>  <br/> | <span data-ttu-id="6d3a7-110">Задайте фигуру, к которой подключен управляющий маркер, в качестве родительского.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-110">Set the shape that the control handle is connected to as the parent.</span></span>  <br/> |
| <span data-ttu-id="6d3a7-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="6d3a7-111">FALSE</span></span>  <br/> | <span data-ttu-id="6d3a7-112">Значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-112">The default.</span></span> <span data-ttu-id="6d3a7-113">Set Shape, который содержит управляющий маркер в качестве родителя.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-113">Set shape that contains the control handle as the parent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d3a7-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6d3a7-114">Remarks</span></span>

<span data-ttu-id="6d3a7-115">Чтобы получить ссылку на ячейку CtrlAsInput по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="6d3a7-115">To get a reference to the CtrlAsInput cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d3a7-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="6d3a7-116">Cell name:</span></span>  <br/> | <span data-ttu-id="6d3a7-117">CtrlAsInput</span><span class="sxs-lookup"><span data-stu-id="6d3a7-117">CtrlAsInput</span></span>  <br/> |
   
<span data-ttu-id="6d3a7-118">Чтобы получить ссылку на ячейку CtrlAsInput по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="6d3a7-118">To get a reference to the CtrlAsInput cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d3a7-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6d3a7-119">Section index:</span></span>  <br/> |<span data-ttu-id="6d3a7-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6d3a7-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6d3a7-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6d3a7-121">Row index:</span></span>  <br/> |<span data-ttu-id="6d3a7-122">**Висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="6d3a7-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="6d3a7-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6d3a7-123">Cell index:</span></span>  <br/> |<span data-ttu-id="6d3a7-124">**Висплоктрласинпут**</span><span class="sxs-lookup"><span data-stu-id="6d3a7-124">**visPLOCtrlAsInput**</span></span> <br/> |
   

