---
title: FillGradientEnabled Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: Определяет, включен ли градиент заполнения для этой фигуры.
ms.openlocfilehash: 17f617c13b632318be22b86a3354a194f0f835f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431213"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a><span data-ttu-id="66817-103">FillGradientEnabled Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="66817-103">FillGradientEnabled Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="66817-104">Определяет, включен ли градиент заполнения для этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="66817-104">Determines whether a fill gradient is enabled for this shape.</span></span> 
  
|<span data-ttu-id="66817-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="66817-105">**Value**</span></span>|<span data-ttu-id="66817-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="66817-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="66817-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="66817-107">TRUE</span></span>  <br/> |<span data-ttu-id="66817-108">На фигуре отображается заполнение Gradient.</span><span class="sxs-lookup"><span data-stu-id="66817-108">Gradient fill is displayed on the shape.</span></span>  <br/> |
|<span data-ttu-id="66817-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="66817-109">FALSE</span></span>  <br/> |<span data-ttu-id="66817-110">Заливки Gradient не отображаются на фигуре.</span><span class="sxs-lookup"><span data-stu-id="66817-110">Gradient fills are not displayed on the shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66817-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="66817-111">Remarks</span></span>

<span data-ttu-id="66817-112">Чтобы получить ссылку на **ячейку FillGradientEnabled** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="66817-112">To get a reference to the **FillGradientEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="66817-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="66817-113">Cell name:</span></span>  <br/> | <span data-ttu-id="66817-114">FillGradientEnabled</span><span class="sxs-lookup"><span data-stu-id="66817-114">FillGradientEnabled</span></span>  <br/> |
   
<span data-ttu-id="66817-115">Чтобы получить ссылку на **ячейку FillGradientEnabled** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="66817-115">To get a reference to the **FillGradientEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="66817-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="66817-116">Section index:</span></span>  <br/> |<span data-ttu-id="66817-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="66817-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="66817-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="66817-118">Row index:</span></span>  <br/> |<span data-ttu-id="66817-119">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="66817-119">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="66817-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="66817-120">Cell index:</span></span>  <br/> |<span data-ttu-id="66817-121">\*\*visFillGradientEnabled \*\*</span><span class="sxs-lookup"><span data-stu-id="66817-121">\*\*visFillGradientEnabled \*\*</span></span> <br/> |
   

