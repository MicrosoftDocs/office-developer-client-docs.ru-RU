---
title: ShapeShdwType Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033173
localization_priority: Normal
ms.assetid: 1461148d-90a9-6f7c-1b28-9310ffaf0e3b
description: Указывает тип тени для фигуры.
ms.openlocfilehash: 607881e4a520f1376562394c6e40ab5d2508906d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430261"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a><span data-ttu-id="3e60b-103">ShapeShdwType Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="3e60b-103">ShapeShdwType Cell (Fill Format Section)</span></span>

<span data-ttu-id="3e60b-104">Указывает тип тени для фигуры.</span><span class="sxs-lookup"><span data-stu-id="3e60b-104">Specifies the type of shadow for a shape.</span></span> 
  
|<span data-ttu-id="3e60b-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3e60b-105">**Value**</span></span>|<span data-ttu-id="3e60b-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3e60b-106">**Description**</span></span>|<span data-ttu-id="3e60b-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="3e60b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3e60b-108">0</span><span class="sxs-lookup"><span data-stu-id="3e60b-108">0</span></span>  <br/> |<span data-ttu-id="3e60b-109">Использование по умолчанию страницы (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e60b-109">Use page default (the default)</span></span>  <br/> |<span data-ttu-id="3e60b-110">**visFSTPageDefault**</span><span class="sxs-lookup"><span data-stu-id="3e60b-110">**visFSTPageDefault**</span></span> <br/> |
|<span data-ttu-id="3e60b-111">1</span><span class="sxs-lookup"><span data-stu-id="3e60b-111">1</span></span>  <br/> |<span data-ttu-id="3e60b-112">Простой</span><span class="sxs-lookup"><span data-stu-id="3e60b-112">Simple</span></span>  <br/> |<span data-ttu-id="3e60b-113">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="3e60b-113">**visFSTSimple**</span></span> <br/> |
|<span data-ttu-id="3e60b-114">2</span><span class="sxs-lookup"><span data-stu-id="3e60b-114">2</span></span>  <br/> |<span data-ttu-id="3e60b-115">Косая</span><span class="sxs-lookup"><span data-stu-id="3e60b-115">Oblique</span></span>  <br/> |<span data-ttu-id="3e60b-116">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="3e60b-116">**visFSTOblique**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e60b-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="3e60b-117">Remarks</span></span>

<span data-ttu-id="3e60b-118">Используйте эту ячейку для применения тени фигуры, которая отличается от страницы по умолчанию (тип тени страницы определяется в ячейке ShdwType в разделе Свойства страниц).</span><span class="sxs-lookup"><span data-stu-id="3e60b-118">Use this cell to apply a shape shadow that is different from the page default (the page default shadow type is defined in the ShdwType cell in the Page Properties Section).</span></span>
  
<span data-ttu-id="3e60b-119">Простые типы теней описываются как офсетные тени в пользовательском интерфейсе (пользовательском интерфейсе).</span><span class="sxs-lookup"><span data-stu-id="3e60b-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="3e60b-120">Простая тень дает эффект тени фигуры на параллельной плоскости, расположенной за фигурой.</span><span class="sxs-lookup"><span data-stu-id="3e60b-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located behind the shape.</span></span> <span data-ttu-id="3e60b-121">Косые тени описываются как косые тени в пользовательском интерфейсе и дают эффект отбрасываемой тени на плоскость перпендикулярно фигуре.</span><span class="sxs-lookup"><span data-stu-id="3e60b-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="3e60b-122">Список предопределяемых простых и косых типов  теней см. в поле Стиль в диалоговом окне **Shadow** (на вкладке **Главная,** в группе **Shape** нажмите кнопку **Тень,** а затем нажмите параметры **Shadow).**</span><span class="sxs-lookup"><span data-stu-id="3e60b-122">For a list of predefined simple and oblique shadow types, see the **Style** box in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="3e60b-123">Чтобы получить ссылку на ячейку ShapeShdwType по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="3e60b-123">To get a reference to the ShapeShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e60b-124">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3e60b-124">Cell name:</span></span>  <br/> |<span data-ttu-id="3e60b-125">ShapeShdwType</span><span class="sxs-lookup"><span data-stu-id="3e60b-125">ShapeShdwType</span></span>  <br/> |
   
<span data-ttu-id="3e60b-126">Чтобы получить ссылку на ячейку ShapeShdwType по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3e60b-126">To get a reference to the ShapeShdwType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e60b-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3e60b-127">Section index:</span></span>  <br/> |<span data-ttu-id="3e60b-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3e60b-128">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3e60b-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3e60b-129">Row index:</span></span>  <br/> |<span data-ttu-id="3e60b-130">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="3e60b-130">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="3e60b-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3e60b-131">Cell index:</span></span>  <br/> |<span data-ttu-id="3e60b-132">**visFillShdwType**</span><span class="sxs-lookup"><span data-stu-id="3e60b-132">**visFillShdwType**</span></span> <br/> |
   

