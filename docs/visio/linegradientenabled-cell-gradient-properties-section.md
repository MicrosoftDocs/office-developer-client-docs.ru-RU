---
title: LineGradientEnabled Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: Определяет, включен ли градиент линии для линии или границы фигуры.
ms.openlocfilehash: 1d2b33275d26bb0c8e5550bcb7cf282c64d34544
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416379"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a><span data-ttu-id="8c29a-103">LineGradientEnabled Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="8c29a-103">LineGradientEnabled Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="8c29a-104">Определяет, включен ли градиент линии для линии или границы фигуры.</span><span class="sxs-lookup"><span data-stu-id="8c29a-104">Determines whether a line gradient is enabled for a line or border of a shape.</span></span> 
  
|<span data-ttu-id="8c29a-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8c29a-105">**Value**</span></span>|<span data-ttu-id="8c29a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8c29a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8c29a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="8c29a-107">TRUE</span></span>  <br/> |<span data-ttu-id="8c29a-108">Градиент отображается на линии или границе фигуры.</span><span class="sxs-lookup"><span data-stu-id="8c29a-108">Gradient is displayed on the line or border of a shape.</span></span>  <br/> |
|<span data-ttu-id="8c29a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="8c29a-109">FALSE</span></span>  <br/> |<span data-ttu-id="8c29a-110">Градиенты не отображаются на линии или границе фигуры.</span><span class="sxs-lookup"><span data-stu-id="8c29a-110">Gradients are not displayed on the line or border of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c29a-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="8c29a-111">Remarks</span></span>

<span data-ttu-id="8c29a-112">Чтобы получить ссылку на ячейку **LineGradientEnabled** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="8c29a-112">To get a reference to the **LineGradientEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8c29a-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="8c29a-113">Cell name:</span></span>  <br/> | <span data-ttu-id="8c29a-114">LineGradientEnabled</span><span class="sxs-lookup"><span data-stu-id="8c29a-114">LineGradientEnabled</span></span>  <br/> |
   
<span data-ttu-id="8c29a-115">Чтобы получить ссылку на ячейку **LineGradientEnabled** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="8c29a-115">To get a reference to the **LineGradientEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8c29a-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8c29a-116">Section index:</span></span>  <br/> |<span data-ttu-id="8c29a-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8c29a-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8c29a-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8c29a-118">Row index:</span></span>  <br/> |<span data-ttu-id="8c29a-119">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="8c29a-119">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="8c29a-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8c29a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="8c29a-121">**visLineGradientEnabled**</span><span class="sxs-lookup"><span data-stu-id="8c29a-121">**visLineGradientEnabled**</span></span> <br/> |
   

