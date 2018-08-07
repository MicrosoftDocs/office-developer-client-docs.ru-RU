---
title: Ячейка CtrlAsInput (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
localization_priority: Normal
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: Определяет, какие фигуры родительский при использовании фигур с помощью маркеров элемента управления. В этой ячейке указывается, что для всех фигур на странице документа.
ms.openlocfilehash: a87ba7451d73af50de4a110ecdc12b3e23e14d5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813518"
---
# <a name="ctrlasinput-cell-page-layout-section"></a><span data-ttu-id="f54b9-104">Ячейка CtrlAsInput (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="f54b9-104">CtrlAsInput Cell (Page Layout Section)</span></span>

<span data-ttu-id="f54b9-105">Определяет, какие фигуры родительский при использовании фигур с помощью маркеров элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f54b9-105">Determines which shape is the parent when using shapes with control handles.</span></span> <span data-ttu-id="f54b9-106">В этой ячейке указывается, что для всех фигур на странице документа.</span><span class="sxs-lookup"><span data-stu-id="f54b9-106">This cell sets the behavior for all the shapes on the drawing page.</span></span>
  
|<span data-ttu-id="f54b9-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f54b9-107">**Value**</span></span>|<span data-ttu-id="f54b9-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f54b9-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f54b9-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="f54b9-109">TRUE</span></span>  <br/> | <span data-ttu-id="f54b9-110">Задайте фигуры, подключенной к дескриптора элемента управления в качестве родительского.</span><span class="sxs-lookup"><span data-stu-id="f54b9-110">Set the shape that the control handle is connected to as the parent.</span></span>  <br/> |
| <span data-ttu-id="f54b9-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="f54b9-111">FALSE</span></span>  <br/> | <span data-ttu-id="f54b9-112">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f54b9-112">The default.</span></span> <span data-ttu-id="f54b9-113">Набор фигуры, содержащее дескриптор управления как родительский элемент.</span><span class="sxs-lookup"><span data-stu-id="f54b9-113">Set shape that contains the control handle as the parent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f54b9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f54b9-114">Remarks</span></span>

<span data-ttu-id="f54b9-115">Чтобы получить ссылку на ячейку CtrlAsInput по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f54b9-115">To get a reference to the CtrlAsInput cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f54b9-116">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="f54b9-116">Cell name:</span></span>  <br/> | <span data-ttu-id="f54b9-117">CtrlAsInput</span><span class="sxs-lookup"><span data-stu-id="f54b9-117">CtrlAsInput</span></span>  <br/> |
   
<span data-ttu-id="f54b9-118">Для получения ссылки на ячейки CtrlAsInput по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="f54b9-118">To get a reference to the CtrlAsInput cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f54b9-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f54b9-119">Section index:</span></span>  <br/> |<span data-ttu-id="f54b9-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f54b9-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f54b9-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f54b9-121">Row index:</span></span>  <br/> |<span data-ttu-id="f54b9-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="f54b9-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="f54b9-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f54b9-123">Cell index:</span></span>  <br/> |<span data-ttu-id="f54b9-124">**visPLOCtrlAsInput**</span><span class="sxs-lookup"><span data-stu-id="f54b9-124">**visPLOCtrlAsInput**</span></span> <br/> |
   

