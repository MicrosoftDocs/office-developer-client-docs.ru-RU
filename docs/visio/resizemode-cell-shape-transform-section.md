---
title: ResizeMode Cell (Shape Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251203
localization_priority: Normal
ms.assetid: 49816e46-fa83-3ee4-1451-9c85fbd0f519
description: Показывает текущее поведение изменения размеров фигуры.
ms.openlocfilehash: 7e9080fcd4604e2dbdc1dae31992f05e5b512213
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421965"
---
# <a name="resizemode-cell-shape-transform-section"></a><span data-ttu-id="402c6-103">ResizeMode Cell (Shape Transform Section)</span><span class="sxs-lookup"><span data-stu-id="402c6-103">ResizeMode Cell (Shape Transform Section)</span></span>

<span data-ttu-id="402c6-104">Показывает текущее поведение изменения размеров фигуры.</span><span class="sxs-lookup"><span data-stu-id="402c6-104">Shows the current resize behavior setting for the shape.</span></span>
  
|<span data-ttu-id="402c6-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="402c6-105">**Value**</span></span>|<span data-ttu-id="402c6-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="402c6-106">**Description**</span></span>|<span data-ttu-id="402c6-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="402c6-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="402c6-108">0</span><span class="sxs-lookup"><span data-stu-id="402c6-108">0</span></span>  <br/> |<span data-ttu-id="402c6-109">Используйте параметр группы.</span><span class="sxs-lookup"><span data-stu-id="402c6-109">Use group's setting.</span></span>  <br/> |<span data-ttu-id="402c6-110">**visXFormResizeDontCare**</span><span class="sxs-lookup"><span data-stu-id="402c6-110">**visXFormResizeDontCare**</span></span> <br/> |
|<span data-ttu-id="402c6-111">1 </span><span class="sxs-lookup"><span data-stu-id="402c6-111">1</span></span>  <br/> |<span data-ttu-id="402c6-112">Только для перенастройки.</span><span class="sxs-lookup"><span data-stu-id="402c6-112">Reposition only.</span></span>  <br/> |<span data-ttu-id="402c6-113">**visXFormResizeSpread**</span><span class="sxs-lookup"><span data-stu-id="402c6-113">**visXFormResizeSpread**</span></span> <br/> |
|<span data-ttu-id="402c6-114">2 </span><span class="sxs-lookup"><span data-stu-id="402c6-114">2</span></span>  <br/> |<span data-ttu-id="402c6-115">Масштабировать с помощью группы.</span><span class="sxs-lookup"><span data-stu-id="402c6-115">Scale with group.</span></span>  <br/> |<span data-ttu-id="402c6-116">**visXFormResizeScale**</span><span class="sxs-lookup"><span data-stu-id="402c6-116">**visXFormResizeScale**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="402c6-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="402c6-117">Remarks</span></span>

<span data-ttu-id="402c6-118">Вы также можете установить это значение  на вкладке **"Поведение"** в диалоговом окне "Поведение" (на вкладке "Разработчик" в группе "Проектирование фигур" щелкните [](run-in-developer-mode-display-the-developer-tab.md) **"Поведение").** </span><span class="sxs-lookup"><span data-stu-id="402c6-118">You can also set this value on the **Behavior** tab in the **Behavior** dialog box (on the [Developer](run-in-developer-mode-display-the-developer-tab.md)tab, in the **Shape Design** group, click **Behavior**).</span></span> <span data-ttu-id="402c6-119">Чтобы получить ссылку на ячейку ResizeMode по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="402c6-119">To get a reference to the ResizeMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="402c6-120">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="402c6-120">Cell name:</span></span>  <br/> |<span data-ttu-id="402c6-121">ResizeMode</span><span class="sxs-lookup"><span data-stu-id="402c6-121">ResizeMode</span></span>  <br/> |
   
<span data-ttu-id="402c6-122">Чтобы получить ссылку на ячейку ResizeMode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="402c6-122">To get a reference to the ResizeMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="402c6-123">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="402c6-123">Section index:</span></span>  <br/> |<span data-ttu-id="402c6-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="402c6-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="402c6-125">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="402c6-125">Row index:</span></span>  <br/> |<span data-ttu-id="402c6-126">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="402c6-126">**visRowXFormOut**</span></span> <br/> |
|<span data-ttu-id="402c6-127">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="402c6-127">Cell index:</span></span>  <br/> |<span data-ttu-id="402c6-128">**visXFormResizeMode**</span><span class="sxs-lookup"><span data-stu-id="402c6-128">**visXFormResizeMode**</span></span> <br/> |
   

