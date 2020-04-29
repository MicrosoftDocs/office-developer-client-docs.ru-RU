---
title: ShdwType Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Указывает тип тени по умолчанию для страницы.
ms.openlocfilehash: f1fc72484d94788ca2798760ca935c89c3e841ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424100"
---
# <a name="shdwtype-cell-page-properties-section"></a><span data-ttu-id="fdc84-103">ShdwType Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="fdc84-103">ShdwType Cell (Page Properties Section)</span></span>

<span data-ttu-id="fdc84-104">Указывает тип тени по умолчанию для страницы.</span><span class="sxs-lookup"><span data-stu-id="fdc84-104">Indicates the default shadow type for a page.</span></span>
  
|<span data-ttu-id="fdc84-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="fdc84-105">**Value**</span></span>|<span data-ttu-id="fdc84-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fdc84-106">**Description**</span></span>|<span data-ttu-id="fdc84-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="fdc84-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="fdc84-108">1,1</span><span class="sxs-lookup"><span data-stu-id="fdc84-108">1</span></span>  <br/> | <span data-ttu-id="fdc84-109">Простое</span><span class="sxs-lookup"><span data-stu-id="fdc84-109">Simple</span></span>  <br/> |<span data-ttu-id="fdc84-110">**висфстсимпле**</span><span class="sxs-lookup"><span data-stu-id="fdc84-110">**visFSTSimple**</span></span> <br/> |
| <span data-ttu-id="fdc84-111">2</span><span class="sxs-lookup"><span data-stu-id="fdc84-111">2</span></span>  <br/> | <span data-ttu-id="fdc84-112">Наклон</span><span class="sxs-lookup"><span data-stu-id="fdc84-112">Oblique</span></span>  <br/> |<span data-ttu-id="fdc84-113">**висфстобликуе**</span><span class="sxs-lookup"><span data-stu-id="fdc84-113">**visFSTOblique**</span></span> <br/> |
|<span data-ttu-id="fdc84-114">4</span><span class="sxs-lookup"><span data-stu-id="fdc84-114">3</span></span>  <br/> |<span data-ttu-id="fdc84-115">Inner</span><span class="sxs-lookup"><span data-stu-id="fdc84-115">Inner</span></span>  <br/> |<span data-ttu-id="fdc84-116">**висфстиннер**</span><span class="sxs-lookup"><span data-stu-id="fdc84-116">**visFSTInner**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fdc84-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="fdc84-117">Remarks</span></span>

 <span data-ttu-id="fdc84-118">Тип Shadow, описанный в этой ячейке, используется всякий раз, когда ячейка ShapeShdwType (тип тени для отдельной фигуры на странице) имеет значение Default страницы (**висфстпажедефаулт** ).</span><span class="sxs-lookup"><span data-stu-id="fdc84-118">The shadow type described in this cell is used whenever the ShapeShdwType Cell (the shadow type for an individual shape on the page) is set to Page Default (**visFSTPageDefault** ).</span></span> 
  
<span data-ttu-id="fdc84-119">Простые типы тени описаны в виде теней со смещением в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="fdc84-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="fdc84-120">Простая тень дает эффект тени фигуры на параллельную плоскость, расположенную на некоторый расстоянии.</span><span class="sxs-lookup"><span data-stu-id="fdc84-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located some distance behind it.</span></span> <span data-ttu-id="fdc84-121">Наклонные тени описываются в виде наклонных теней в пользовательском интерфейсе и приводят к эффекту тени, приведенной на плоскость, перпендикулярную фигуре.</span><span class="sxs-lookup"><span data-stu-id="fdc84-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="fdc84-122">Список предварительно определенных простых и наклонных типов тени представлен в списке **стилей** на вкладке **Shadows** диалогового окна **Параметры страницы** (на вкладке **конструктор** щелкните стрелку **Параметры страницы** ).</span><span class="sxs-lookup"><span data-stu-id="fdc84-122">For a list of predefined simple and oblique shadow types, see the **Style** list on the **Shadows** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="fdc84-123">Чтобы получить ссылку на ячейку ShdwType по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="fdc84-123">To get a reference to the ShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fdc84-124">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="fdc84-124">Cell name:</span></span>  <br/> | <span data-ttu-id="fdc84-125">ShdwType</span><span class="sxs-lookup"><span data-stu-id="fdc84-125">ShdwType</span></span>  <br/> |
   
<span data-ttu-id="fdc84-126">Чтобы получить ссылку на ячейку ShapeShdwOffsetX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="fdc84-126">To get a reference to the ShapeShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fdc84-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fdc84-127">Section index:</span></span>  <br/> |<span data-ttu-id="fdc84-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fdc84-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fdc84-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fdc84-129">Row index:</span></span>  <br/> |<span data-ttu-id="fdc84-130">**висровпаже**</span><span class="sxs-lookup"><span data-stu-id="fdc84-130">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="fdc84-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fdc84-131">Cell index:</span></span>  <br/> |<span data-ttu-id="fdc84-132">**виспажешдвтипе**</span><span class="sxs-lookup"><span data-stu-id="fdc84-132">**visPageShdwType**</span></span> <br/> |
   

