---
title: DynamicsOff Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251641
localization_priority: Normal
ms.assetid: 055764aa-9681-ffb0-83ce-fdd612fe37af
description: Определяет, перемещаются ли размещаемые фигуры, а соединители перенаправляются по другим фигурам и соединительным линиям на странице документа.
ms.openlocfilehash: d1075ab1b0512d5db1c7b7a5f2895305318dae7d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315723"
---
# <a name="dynamicsoff-cell-page-layout-section"></a><span data-ttu-id="5eabf-103">DynamicsOff Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="5eabf-103">DynamicsOff Cell (Page Layout Section)</span></span>

<span data-ttu-id="5eabf-104">Определяет, перемещаются ли размещаемые фигуры, а соединители перенаправляются по другим фигурам и соединительным линиям на странице документа.</span><span class="sxs-lookup"><span data-stu-id="5eabf-104">Determines whether placeable shapes move and connectors reroute around other shapes and connectors on the drawing page.</span></span>
  
|<span data-ttu-id="5eabf-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="5eabf-105">**Value**</span></span>|<span data-ttu-id="5eabf-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5eabf-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5eabf-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5eabf-107">TRUE</span></span>  <br/> | <span data-ttu-id="5eabf-108">Отключить Dynamics.</span><span class="sxs-lookup"><span data-stu-id="5eabf-108">Disable dynamics.</span></span>  <br/> |
| <span data-ttu-id="5eabf-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5eabf-109">FALSE</span></span>  <br/> | <span data-ttu-id="5eabf-110">Включение Dynamics.</span><span class="sxs-lookup"><span data-stu-id="5eabf-110">Enable dynamics.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5eabf-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="5eabf-111">Remarks</span></span>

<span data-ttu-id="5eabf-112">Вы можете отключить Dynamics, чтобы увеличить производительность решения.</span><span class="sxs-lookup"><span data-stu-id="5eabf-112">You can disable dynamics to increase your solution's performance.</span></span> <span data-ttu-id="5eabf-113">Например, если ваше решение добавляет размещаемые фигуры в документ и вы не хотите, чтобы приложение перенаправляло соединители и изменить положение фигур каждый раз при добавлении фигуры, можно отключить Dynamics.</span><span class="sxs-lookup"><span data-stu-id="5eabf-113">For example, if your solution adds placeable shapes to a drawing and you don't want the application to reroute connectors and reposition shapes each time you add a shape, you can disable dynamics.</span></span> <span data-ttu-id="5eabf-114">После того как решение добавит фигуры, повторно включите Dynamics.</span><span class="sxs-lookup"><span data-stu-id="5eabf-114">After your solution adds the shapes, re-enable dynamics.</span></span>
  
<span data-ttu-id="5eabf-115">Чтобы получить ссылку на ячейку DynamicsOff по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="5eabf-115">To get a reference to the DynamicsOff cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5eabf-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5eabf-116">Cell name:</span></span>  <br/> | <span data-ttu-id="5eabf-117">DynamicsOff</span><span class="sxs-lookup"><span data-stu-id="5eabf-117">DynamicsOff</span></span>  <br/> |
   
<span data-ttu-id="5eabf-118">Чтобы получить ссылку на ячейку DynamicsOff по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5eabf-118">To get a reference to the DynamicsOff cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5eabf-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5eabf-119">Section index:</span></span>  <br/> |<span data-ttu-id="5eabf-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5eabf-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5eabf-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5eabf-121">Row index:</span></span>  <br/> |<span data-ttu-id="5eabf-122">**Висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="5eabf-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="5eabf-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5eabf-123">Cell index:</span></span>  <br/> |<span data-ttu-id="5eabf-124">**Висплодинамиксофф**</span><span class="sxs-lookup"><span data-stu-id="5eabf-124">**visPLODynamicsOff**</span></span> <br/> |
   

