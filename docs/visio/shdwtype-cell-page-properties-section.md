---
title: Ячейка ShdwType (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Указывает тип тени по умолчанию для страницы.
ms.openlocfilehash: 1fc5c31a723d5d409110d94ff543a45dadabf264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814844"
---
# <a name="shdwtype-cell-page-properties-section"></a><span data-ttu-id="12171-103">Ячейка ShdwType (раздел "Свойства страницы")</span><span class="sxs-lookup"><span data-stu-id="12171-103">ShdwType Cell (Page Properties Section)</span></span>

<span data-ttu-id="12171-104">Указывает тип тени по умолчанию для страницы.</span><span class="sxs-lookup"><span data-stu-id="12171-104">Indicates the default shadow type for a page.</span></span>
  
|<span data-ttu-id="12171-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="12171-105">**Value**</span></span>|<span data-ttu-id="12171-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="12171-106">**Description**</span></span>|<span data-ttu-id="12171-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="12171-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="12171-108">1</span><span class="sxs-lookup"><span data-stu-id="12171-108">1</span></span>  <br/> | <span data-ttu-id="12171-109">Простое</span><span class="sxs-lookup"><span data-stu-id="12171-109">Simple</span></span>  <br/> |<span data-ttu-id="12171-110">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="12171-110">**visFSTSimple**</span></span> <br/> |
| <span data-ttu-id="12171-111">2</span><span class="sxs-lookup"><span data-stu-id="12171-111">2</span></span>  <br/> | <span data-ttu-id="12171-112">Наклон</span><span class="sxs-lookup"><span data-stu-id="12171-112">Oblique</span></span>  <br/> |<span data-ttu-id="12171-113">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="12171-113">**visFSTOblique**</span></span> <br/> |
|<span data-ttu-id="12171-114">3</span><span class="sxs-lookup"><span data-stu-id="12171-114">3</span></span>  <br/> |<span data-ttu-id="12171-115">Внутренний</span><span class="sxs-lookup"><span data-stu-id="12171-115">Inner</span></span>  <br/> |<span data-ttu-id="12171-116">**visFSTInner**</span><span class="sxs-lookup"><span data-stu-id="12171-116">**visFSTInner**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12171-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="12171-117">Remarks</span></span>

 <span data-ttu-id="12171-118">При использовании ShapeShdwType ячейки (тип тени для отдельных фигуры на странице) страница по умолчанию (**visFSTPageDefault** ) используется тип тени, описанных в этой ячейке.</span><span class="sxs-lookup"><span data-stu-id="12171-118">The shadow type described in this cell is used whenever the ShapeShdwType Cell (the shadow type for an individual shape on the page) is set to Page Default (**visFSTPageDefault** ).</span></span> 
  
<span data-ttu-id="12171-119">Простая тень типов описаны как смещения тени пользовательского интерфейса (UI).</span><span class="sxs-lookup"><span data-stu-id="12171-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="12171-120">Простая тень дает влияние фигуры, теневую на параллельный плоскости, расположенной некоторые расстояние под ним.</span><span class="sxs-lookup"><span data-stu-id="12171-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located some distance behind it.</span></span> <span data-ttu-id="12171-121">Наклон тени описанными наклон теней в пользовательском Интерфейсе и создания эффекта тени приведение на плоскости перпендикулярно фигуры.</span><span class="sxs-lookup"><span data-stu-id="12171-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="12171-122">Список типов предварительно заданных простой и наклон тени, можно найти в списке **стиль** на вкладке **теней** диалогового окна **Параметры страницы** (на вкладки " **Конструктор** ", нажмите стрелку **Параметры страницы** ).</span><span class="sxs-lookup"><span data-stu-id="12171-122">For a list of predefined simple and oblique shadow types, see the **Style** list on the **Shadows** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="12171-123">Чтобы получить ссылку на ячейку ShdwType по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="12171-123">To get a reference to the ShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="12171-124">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="12171-124">Cell name:</span></span>  <br/> | <span data-ttu-id="12171-125">ShdwType</span><span class="sxs-lookup"><span data-stu-id="12171-125">ShdwType</span></span>  <br/> |
   
<span data-ttu-id="12171-126">Для получения ссылки на ячейки ShapeShdwOffsetX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="12171-126">To get a reference to the ShapeShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="12171-127">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="12171-127">Section index:</span></span>  <br/> |<span data-ttu-id="12171-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="12171-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="12171-129">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="12171-129">Row index:</span></span>  <br/> |<span data-ttu-id="12171-130">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="12171-130">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="12171-131">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="12171-131">Cell index:</span></span>  <br/> |<span data-ttu-id="12171-132">**visPageShdwType**</span><span class="sxs-lookup"><span data-stu-id="12171-132">**visPageShdwType**</span></span> <br/> |
   

