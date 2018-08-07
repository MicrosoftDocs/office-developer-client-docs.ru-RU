---
title: Ячейка LineGradientEnabled (раздел "Свойства градиента")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: Определяет, включена ли градиент строки для линии или границы фигуры.
ms.openlocfilehash: d78a94a25c0290bd5e58522c9a45955868f31b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814070"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a><span data-ttu-id="d1883-103">Ячейка LineGradientEnabled (раздел "Свойства градиента")</span><span class="sxs-lookup"><span data-stu-id="d1883-103">LineGradientEnabled Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="d1883-104">Определяет, включена ли градиент строки для линии или границы фигуры.</span><span class="sxs-lookup"><span data-stu-id="d1883-104">Determines whether a line gradient is enabled for a line or border of a shape.</span></span> 
  
|<span data-ttu-id="d1883-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d1883-105">**Value**</span></span>|<span data-ttu-id="d1883-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d1883-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d1883-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d1883-107">TRUE</span></span>  <br/> |<span data-ttu-id="d1883-108">Градиентные отображается в строке или границы фигуры.</span><span class="sxs-lookup"><span data-stu-id="d1883-108">Gradient is displayed on the line or border of a shape.</span></span>  <br/> |
|<span data-ttu-id="d1883-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d1883-109">FALSE</span></span>  <br/> |<span data-ttu-id="d1883-110">Градиентом, не отображаются в строке или границы фигуры.</span><span class="sxs-lookup"><span data-stu-id="d1883-110">Gradients are not displayed on the line or border of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1883-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="d1883-111">Remarks</span></span>

<span data-ttu-id="d1883-112">Для получения ссылки на ячейки **LineGradientEnabled** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="d1883-112">To get a reference to the **LineGradientEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d1883-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="d1883-113">Cell name:</span></span>  <br/> | <span data-ttu-id="d1883-114">LineGradientEnabled</span><span class="sxs-lookup"><span data-stu-id="d1883-114">LineGradientEnabled</span></span>  <br/> |
   
<span data-ttu-id="d1883-115">Для получения ссылки на ячейки **LineGradientEnabled** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="d1883-115">To get a reference to the **LineGradientEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d1883-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d1883-116">Section index:</span></span>  <br/> |<span data-ttu-id="d1883-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d1883-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d1883-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d1883-118">Row index:</span></span>  <br/> |<span data-ttu-id="d1883-119">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="d1883-119">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="d1883-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d1883-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d1883-121">**visLineGradientEnabled**</span><span class="sxs-lookup"><span data-stu-id="d1883-121">**visLineGradientEnabled**</span></span> <br/> |
   

