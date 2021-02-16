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
description: Определяет, перемещаются ли перемещаемые фигуры, а соединители перенадвигаются вокруг других фигур и соединители на странице рисования.
ms.openlocfilehash: d1075ab1b0512d5db1c7b7a5f2895305318dae7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437478"
---
# <a name="dynamicsoff-cell-page-layout-section"></a><span data-ttu-id="c6ed6-103">DynamicsOff Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="c6ed6-103">DynamicsOff Cell (Page Layout Section)</span></span>

<span data-ttu-id="c6ed6-104">Определяет, перемещаются ли перемещаемые фигуры, а соединители перенадвигаются вокруг других фигур и соединители на странице рисования.</span><span class="sxs-lookup"><span data-stu-id="c6ed6-104">Determines whether placeable shapes move and connectors reroute around other shapes and connectors on the drawing page.</span></span>
  
|<span data-ttu-id="c6ed6-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c6ed6-105">**Value**</span></span>|<span data-ttu-id="c6ed6-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c6ed6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c6ed6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c6ed6-107">TRUE</span></span>  <br/> | <span data-ttu-id="c6ed6-108">Отключать динамику.</span><span class="sxs-lookup"><span data-stu-id="c6ed6-108">Disable dynamics.</span></span>  <br/> |
| <span data-ttu-id="c6ed6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c6ed6-109">FALSE</span></span>  <br/> | <span data-ttu-id="c6ed6-110">Включить динамику.</span><span class="sxs-lookup"><span data-stu-id="c6ed6-110">Enable dynamics.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6ed6-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="c6ed6-111">Remarks</span></span>

<span data-ttu-id="c6ed6-112">Вы можете отключить динамику, чтобы повысить производительность решения.</span><span class="sxs-lookup"><span data-stu-id="c6ed6-112">You can disable dynamics to increase your solution's performance.</span></span> <span data-ttu-id="c6ed6-113">Например, если ваше решение добавляет в рисунок местоимяемые фигуры и вы не хотите, чтобы приложение перенанимал соединители и менял положение фигур при каждом добавлении фигуры, вы можете отключить динамику.</span><span class="sxs-lookup"><span data-stu-id="c6ed6-113">For example, if your solution adds placeable shapes to a drawing and you don't want the application to reroute connectors and reposition shapes each time you add a shape, you can disable dynamics.</span></span> <span data-ttu-id="c6ed6-114">После того как ваше решение добавит фигуры, повторно в включить динамику.</span><span class="sxs-lookup"><span data-stu-id="c6ed6-114">After your solution adds the shapes, re-enable dynamics.</span></span>
  
<span data-ttu-id="c6ed6-115">Чтобы получить ссылку на ячейку DynamicsOff по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="c6ed6-115">To get a reference to the DynamicsOff cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c6ed6-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c6ed6-116">Cell name:</span></span>  <br/> | <span data-ttu-id="c6ed6-117">DynamicsOff</span><span class="sxs-lookup"><span data-stu-id="c6ed6-117">DynamicsOff</span></span>  <br/> |
   
<span data-ttu-id="c6ed6-118">Чтобы получить ссылку на ячейку DynamicsOff по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c6ed6-118">To get a reference to the DynamicsOff cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c6ed6-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c6ed6-119">Section index:</span></span>  <br/> |<span data-ttu-id="c6ed6-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c6ed6-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c6ed6-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c6ed6-121">Row index:</span></span>  <br/> |<span data-ttu-id="c6ed6-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="c6ed6-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="c6ed6-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c6ed6-123">Cell index:</span></span>  <br/> |<span data-ttu-id="c6ed6-124">**visPLODynamicsOff**</span><span class="sxs-lookup"><span data-stu-id="c6ed6-124">**visPLODynamicsOff**</span></span> <br/> |
   

