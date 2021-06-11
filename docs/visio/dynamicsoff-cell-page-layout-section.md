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
description: Определяет, перемещаются ли фигуры и соединители другие фигуры и соединители на странице рисования.
ms.openlocfilehash: d1075ab1b0512d5db1c7b7a5f2895305318dae7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437478"
---
# <a name="dynamicsoff-cell-page-layout-section"></a><span data-ttu-id="eeb6c-103">DynamicsOff Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="eeb6c-103">DynamicsOff Cell (Page Layout Section)</span></span>

<span data-ttu-id="eeb6c-104">Определяет, перемещаются ли фигуры и соединители другие фигуры и соединители на странице рисования.</span><span class="sxs-lookup"><span data-stu-id="eeb6c-104">Determines whether placeable shapes move and connectors reroute around other shapes and connectors on the drawing page.</span></span>
  
|<span data-ttu-id="eeb6c-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="eeb6c-105">**Value**</span></span>|<span data-ttu-id="eeb6c-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="eeb6c-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="eeb6c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="eeb6c-107">TRUE</span></span>  <br/> | <span data-ttu-id="eeb6c-108">Отключить динамику.</span><span class="sxs-lookup"><span data-stu-id="eeb6c-108">Disable dynamics.</span></span>  <br/> |
| <span data-ttu-id="eeb6c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="eeb6c-109">FALSE</span></span>  <br/> | <span data-ttu-id="eeb6c-110">Включить динамику.</span><span class="sxs-lookup"><span data-stu-id="eeb6c-110">Enable dynamics.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eeb6c-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="eeb6c-111">Remarks</span></span>

<span data-ttu-id="eeb6c-112">Вы можете отключить динамику, чтобы повысить производительность решения.</span><span class="sxs-lookup"><span data-stu-id="eeb6c-112">You can disable dynamics to increase your solution's performance.</span></span> <span data-ttu-id="eeb6c-113">Например, если при добавлении фигуры в рисунок добавляется допустимые фигуры и не нужно, чтобы приложение перенастрояли соединители и каждый раз перенастрояли фигуры при добавлении фигуры, можно отключить динамику.</span><span class="sxs-lookup"><span data-stu-id="eeb6c-113">For example, if your solution adds placeable shapes to a drawing and you don't want the application to reroute connectors and reposition shapes each time you add a shape, you can disable dynamics.</span></span> <span data-ttu-id="eeb6c-114">После того как решение добавит фигуры, повторно вбавьйте динамику.</span><span class="sxs-lookup"><span data-stu-id="eeb6c-114">After your solution adds the shapes, re-enable dynamics.</span></span>
  
<span data-ttu-id="eeb6c-115">Чтобы получить ссылку на ячейку DynamicsOff по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="eeb6c-115">To get a reference to the DynamicsOff cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eeb6c-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="eeb6c-116">Cell name:</span></span>  <br/> | <span data-ttu-id="eeb6c-117">DynamicsOff</span><span class="sxs-lookup"><span data-stu-id="eeb6c-117">DynamicsOff</span></span>  <br/> |
   
<span data-ttu-id="eeb6c-118">Чтобы получить ссылку на ячейку DynamicsOff по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="eeb6c-118">To get a reference to the DynamicsOff cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eeb6c-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="eeb6c-119">Section index:</span></span>  <br/> |<span data-ttu-id="eeb6c-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eeb6c-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="eeb6c-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="eeb6c-121">Row index:</span></span>  <br/> |<span data-ttu-id="eeb6c-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="eeb6c-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="eeb6c-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="eeb6c-123">Cell index:</span></span>  <br/> |<span data-ttu-id="eeb6c-124">**visPLODynamicsOff**</span><span class="sxs-lookup"><span data-stu-id="eeb6c-124">**visPLODynamicsOff**</span></span> <br/> |
   

