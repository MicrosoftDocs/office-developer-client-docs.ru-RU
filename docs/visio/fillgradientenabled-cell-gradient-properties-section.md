---
title: Ячейка FillGradientEnabled (раздел "Свойства градиента")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: Определяет, включена ли градиентной заливки для этой фигуры.
ms.openlocfilehash: 20a38d4c45af163bc00364a45dc31269bf97251f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813766"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a><span data-ttu-id="b9126-103">Ячейка FillGradientEnabled (раздел "Свойства градиента")</span><span class="sxs-lookup"><span data-stu-id="b9126-103">FillGradientEnabled Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="b9126-104">Определяет, включена ли градиентной заливки для этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="b9126-104">Determines whether a fill gradient is enabled for this shape.</span></span> 
  
|<span data-ttu-id="b9126-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b9126-105">**Value**</span></span>|<span data-ttu-id="b9126-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b9126-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9126-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b9126-107">TRUE</span></span>  <br/> |<span data-ttu-id="b9126-108">Градиентные заливки отображается на форме.</span><span class="sxs-lookup"><span data-stu-id="b9126-108">Gradient fill is displayed on the shape.</span></span>  <br/> |
|<span data-ttu-id="b9126-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b9126-109">FALSE</span></span>  <br/> |<span data-ttu-id="b9126-110">Градиентные заливки не отображаются на форме.</span><span class="sxs-lookup"><span data-stu-id="b9126-110">Gradient fills are not displayed on the shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9126-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="b9126-111">Remarks</span></span>

<span data-ttu-id="b9126-112">Для получения ссылки на ячейки **FillGradientEnabled** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="b9126-112">To get a reference to the **FillGradientEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b9126-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="b9126-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b9126-114">FillGradientEnabled</span><span class="sxs-lookup"><span data-stu-id="b9126-114">FillGradientEnabled</span></span>  <br/> |
   
<span data-ttu-id="b9126-115">Для получения ссылки на ячейки **FillGradientEnabled** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="b9126-115">To get a reference to the **FillGradientEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b9126-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b9126-116">Section index:</span></span>  <br/> |<span data-ttu-id="b9126-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b9126-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b9126-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b9126-118">Row index:</span></span>  <br/> |<span data-ttu-id="b9126-119">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="b9126-119">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="b9126-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b9126-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b9126-121">** visFillGradientEnabled **</span><span class="sxs-lookup"><span data-stu-id="b9126-121">**visFillGradientEnabled **</span></span> <br/> |
   

