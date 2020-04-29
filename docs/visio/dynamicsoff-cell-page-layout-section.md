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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437478"
---
# <a name="dynamicsoff-cell-page-layout-section"></a><span data-ttu-id="bd64e-103">DynamicsOff Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="bd64e-103">DynamicsOff Cell (Page Layout Section)</span></span>

<span data-ttu-id="bd64e-104">Определяет, перемещаются ли размещаемые фигуры, а соединители перенаправляются по другим фигурам и соединительным линиям на странице документа.</span><span class="sxs-lookup"><span data-stu-id="bd64e-104">Determines whether placeable shapes move and connectors reroute around other shapes and connectors on the drawing page.</span></span>
  
|<span data-ttu-id="bd64e-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="bd64e-105">**Value**</span></span>|<span data-ttu-id="bd64e-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bd64e-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bd64e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="bd64e-107">TRUE</span></span>  <br/> | <span data-ttu-id="bd64e-108">Отключить Dynamics.</span><span class="sxs-lookup"><span data-stu-id="bd64e-108">Disable dynamics.</span></span>  <br/> |
| <span data-ttu-id="bd64e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="bd64e-109">FALSE</span></span>  <br/> | <span data-ttu-id="bd64e-110">Включение Dynamics.</span><span class="sxs-lookup"><span data-stu-id="bd64e-110">Enable dynamics.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd64e-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="bd64e-111">Remarks</span></span>

<span data-ttu-id="bd64e-112">Вы можете отключить Dynamics, чтобы увеличить производительность решения.</span><span class="sxs-lookup"><span data-stu-id="bd64e-112">You can disable dynamics to increase your solution's performance.</span></span> <span data-ttu-id="bd64e-113">Например, если ваше решение добавляет размещаемые фигуры в документ и вы не хотите, чтобы приложение перенаправляло соединители и изменить положение фигур каждый раз при добавлении фигуры, можно отключить Dynamics.</span><span class="sxs-lookup"><span data-stu-id="bd64e-113">For example, if your solution adds placeable shapes to a drawing and you don't want the application to reroute connectors and reposition shapes each time you add a shape, you can disable dynamics.</span></span> <span data-ttu-id="bd64e-114">После того как решение добавит фигуры, повторно включите Dynamics.</span><span class="sxs-lookup"><span data-stu-id="bd64e-114">After your solution adds the shapes, re-enable dynamics.</span></span>
  
<span data-ttu-id="bd64e-115">Чтобы получить ссылку на ячейку DynamicsOff по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="bd64e-115">To get a reference to the DynamicsOff cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd64e-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="bd64e-116">Cell name:</span></span>  <br/> | <span data-ttu-id="bd64e-117">DynamicsOff</span><span class="sxs-lookup"><span data-stu-id="bd64e-117">DynamicsOff</span></span>  <br/> |
   
<span data-ttu-id="bd64e-118">Чтобы получить ссылку на ячейку DynamicsOff по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="bd64e-118">To get a reference to the DynamicsOff cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd64e-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bd64e-119">Section index:</span></span>  <br/> |<span data-ttu-id="bd64e-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bd64e-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bd64e-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bd64e-121">Row index:</span></span>  <br/> |<span data-ttu-id="bd64e-122">**висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="bd64e-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="bd64e-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bd64e-123">Cell index:</span></span>  <br/> |<span data-ttu-id="bd64e-124">**висплодинамиксофф**</span><span class="sxs-lookup"><span data-stu-id="bd64e-124">**visPLODynamicsOff**</span></span> <br/> |
   

