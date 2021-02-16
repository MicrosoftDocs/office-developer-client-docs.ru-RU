---
title: Can Glue Cell (Controls Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
localization_priority: Normal
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: Определяет, можно ли приклеить handle-контроля к другим фигурам.
ms.openlocfilehash: 2f5e65ab72c584f88b56e273b0d73abf969a6588
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423295"
---
# <a name="can-glue-cell-controls-section"></a><span data-ttu-id="fac7e-103">Can Glue Cell (Controls Section)</span><span class="sxs-lookup"><span data-stu-id="fac7e-103">Can Glue Cell (Controls Section)</span></span>

<span data-ttu-id="fac7e-104">Определяет, можно ли приклеить handle-контроля к другим фигурам.</span><span class="sxs-lookup"><span data-stu-id="fac7e-104">Determines whether a control handle can be glued to other shapes.</span></span>
  
|<span data-ttu-id="fac7e-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="fac7e-105">**Value**</span></span>|<span data-ttu-id="fac7e-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fac7e-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fac7e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="fac7e-107">TRUE</span></span>  <br/> | <span data-ttu-id="fac7e-108">Handle control can be glued.</span><span class="sxs-lookup"><span data-stu-id="fac7e-108">Control handle can be glued.</span></span>  <br/> |
| <span data-ttu-id="fac7e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="fac7e-109">FALSE</span></span>  <br/> | <span data-ttu-id="fac7e-110">Handle control cannot be glued.</span><span class="sxs-lookup"><span data-stu-id="fac7e-110">Control handle cannot be glued.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fac7e-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="fac7e-111">Remarks</span></span>

<span data-ttu-id="fac7e-112">Чтобы получить ссылку на ячейку Can Glue по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="fac7e-112">To get a reference to the Can Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fac7e-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fac7e-113">Cell name:</span></span>  <br/> | <span data-ttu-id="fac7e-114">Controls.</span><span class="sxs-lookup"><span data-stu-id="fac7e-114">Controls.</span></span>  <span data-ttu-id="fac7e-115">*name*  . Элементы управления CanGluewhere.</span><span class="sxs-lookup"><span data-stu-id="fac7e-115">*name*  .CanGluewhere Controls.</span></span>  <span data-ttu-id="fac7e-116">*имя* — название строки элементов управления.</span><span class="sxs-lookup"><span data-stu-id="fac7e-116">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="fac7e-117">Чтобы получить ссылку на ячейку Can Glue по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fac7e-117">To get a reference to the Can Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fac7e-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fac7e-118">Section index:</span></span>  <br/> |<span data-ttu-id="fac7e-119">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="fac7e-119">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="fac7e-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fac7e-120">Row index:</span></span>  <br/> |<span data-ttu-id="fac7e-121">**visRowControl**  +   *i* где *i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="fac7e-121">**visRowControl** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="fac7e-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fac7e-122">Cell index:</span></span>  <br/> |<span data-ttu-id="fac7e-123">**visCtlGlue**</span><span class="sxs-lookup"><span data-stu-id="fac7e-123">**visCtlGlue**</span></span> <br/> |
   

