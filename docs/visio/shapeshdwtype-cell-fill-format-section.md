---
title: Ячейка ShapeShdwType (раздел "Формат заливки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033173
localization_priority: Normal
ms.assetid: 1461148d-90a9-6f7c-1b28-9310ffaf0e3b
description: Указывает тип тени фигуры.
ms.openlocfilehash: b96ad4a877d72bf4457ec3cf038a29a2b414e0f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814795"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a><span data-ttu-id="4ef4f-103">Ячейка ShapeShdwType (раздел "Формат заливки")</span><span class="sxs-lookup"><span data-stu-id="4ef4f-103">ShapeShdwType Cell (Fill Format Section)</span></span>

<span data-ttu-id="4ef4f-104">Указывает тип тени фигуры.</span><span class="sxs-lookup"><span data-stu-id="4ef4f-104">Specifies the type of shadow for a shape.</span></span> 
  
|<span data-ttu-id="4ef4f-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="4ef4f-105">**Value**</span></span>|<span data-ttu-id="4ef4f-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4ef4f-106">**Description**</span></span>|<span data-ttu-id="4ef4f-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="4ef4f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4ef4f-108">0</span><span class="sxs-lookup"><span data-stu-id="4ef4f-108">0</span></span>  <br/> |<span data-ttu-id="4ef4f-109">Использование страницы по умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ef4f-109">Use page default (the default)</span></span>  <br/> |<span data-ttu-id="4ef4f-110">**visFSTPageDefault**</span><span class="sxs-lookup"><span data-stu-id="4ef4f-110">**visFSTPageDefault**</span></span> <br/> |
|<span data-ttu-id="4ef4f-111">1</span><span class="sxs-lookup"><span data-stu-id="4ef4f-111">1</span></span>  <br/> |<span data-ttu-id="4ef4f-112">Простое</span><span class="sxs-lookup"><span data-stu-id="4ef4f-112">Simple</span></span>  <br/> |<span data-ttu-id="4ef4f-113">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="4ef4f-113">**visFSTSimple**</span></span> <br/> |
|<span data-ttu-id="4ef4f-114">2</span><span class="sxs-lookup"><span data-stu-id="4ef4f-114">2</span></span>  <br/> |<span data-ttu-id="4ef4f-115">Наклон</span><span class="sxs-lookup"><span data-stu-id="4ef4f-115">Oblique</span></span>  <br/> |<span data-ttu-id="4ef4f-116">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="4ef4f-116">**visFSTOblique**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ef4f-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="4ef4f-117">Remarks</span></span>

<span data-ttu-id="4ef4f-118">Используйте эту ячейку для применения тени фигуры, отличный от страницы по умолчанию (типа тени по умолчанию определяется в ячейке ShdwType в разделе Страница свойств).</span><span class="sxs-lookup"><span data-stu-id="4ef4f-118">Use this cell to apply a shape shadow that is different from the page default (the page default shadow type is defined in the ShdwType cell in the Page Properties Section).</span></span>
  
<span data-ttu-id="4ef4f-119">Простая тень типов описаны как смещения тени пользовательского интерфейса (UI).</span><span class="sxs-lookup"><span data-stu-id="4ef4f-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="4ef4f-120">Простая тень дает эффект фигуры, теневую на параллельный плоскости, расположенной за фигуры.</span><span class="sxs-lookup"><span data-stu-id="4ef4f-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located behind the shape.</span></span> <span data-ttu-id="4ef4f-121">Наклон тени описанными наклон теней в пользовательском Интерфейсе и создания эффекта тени приведение на плоскости перпендикулярно фигуры.</span><span class="sxs-lookup"><span data-stu-id="4ef4f-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="4ef4f-122">Список типов предварительно заданных простой и наклон тени, просмотрите окно **стиль** в диалоговом окне **теневой** (на вкладке **Главная** в группе **фигуру** нажмите кнопку **тень**и нажмите кнопку **Параметры тени**).</span><span class="sxs-lookup"><span data-stu-id="4ef4f-122">For a list of predefined simple and oblique shadow types, see the **Style** box in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="4ef4f-123">Чтобы получить ссылку на ячейку ShapeShdwType по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="4ef4f-123">To get a reference to the ShapeShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ef4f-124">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="4ef4f-124">Cell name:</span></span>  <br/> |<span data-ttu-id="4ef4f-125">ShapeShdwType</span><span class="sxs-lookup"><span data-stu-id="4ef4f-125">ShapeShdwType</span></span>  <br/> |
   
<span data-ttu-id="4ef4f-126">Для получения ссылки на ячейки ShapeShdwType по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="4ef4f-126">To get a reference to the ShapeShdwType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ef4f-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4ef4f-127">Section index:</span></span>  <br/> |<span data-ttu-id="4ef4f-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4ef4f-128">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4ef4f-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4ef4f-129">Row index:</span></span>  <br/> |<span data-ttu-id="4ef4f-130">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="4ef4f-130">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="4ef4f-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4ef4f-131">Cell index:</span></span>  <br/> |<span data-ttu-id="4ef4f-132">**visFillShdwType**</span><span class="sxs-lookup"><span data-stu-id="4ef4f-132">**visFillShdwType**</span></span> <br/> |
   

