---
title: Ячейка DynamicsOff (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251641
localization_priority: Normal
ms.assetid: 055764aa-9681-ffb0-83ce-fdd612fe37af
description: Определяет, будет ли размещаемые фигуры и соединители перенаправление вокруг другие фигуры и соединители на странице документа.
ms.openlocfilehash: 72d65860d1a2ee37efd5287ae3f4baf54bd3addb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813665"
---
# <a name="dynamicsoff-cell-page-layout-section"></a><span data-ttu-id="4d295-103">Ячейка DynamicsOff (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="4d295-103">DynamicsOff Cell (Page Layout Section)</span></span>

<span data-ttu-id="4d295-104">Определяет, будет ли размещаемые фигуры и соединители перенаправление вокруг другие фигуры и соединители на странице документа.</span><span class="sxs-lookup"><span data-stu-id="4d295-104">Determines whether placeable shapes move and connectors reroute around other shapes and connectors on the drawing page.</span></span>
  
|<span data-ttu-id="4d295-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="4d295-105">**Value**</span></span>|<span data-ttu-id="4d295-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4d295-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4d295-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="4d295-107">TRUE</span></span>  <br/> | <span data-ttu-id="4d295-108">Отключение dynamics.</span><span class="sxs-lookup"><span data-stu-id="4d295-108">Disable dynamics.</span></span>  <br/> |
| <span data-ttu-id="4d295-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="4d295-109">FALSE</span></span>  <br/> | <span data-ttu-id="4d295-110">Включение dynamics.</span><span class="sxs-lookup"><span data-stu-id="4d295-110">Enable dynamics.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d295-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="4d295-111">Remarks</span></span>

<span data-ttu-id="4d295-112">Можно отключить dynamics для повышения производительности решения.</span><span class="sxs-lookup"><span data-stu-id="4d295-112">You can disable dynamics to increase your solution's performance.</span></span> <span data-ttu-id="4d295-113">Например если решение добавляет размещаемые фигуры на рисунок и требуется приложение для перенаправления соединители и изменить положение фигур каждый раз при добавлении фигуры, можно отключить dynamics.</span><span class="sxs-lookup"><span data-stu-id="4d295-113">For example, if your solution adds placeable shapes to a drawing and you don't want the application to reroute connectors and reposition shapes each time you add a shape, you can disable dynamics.</span></span> <span data-ttu-id="4d295-114">После решения добавляет фигур, повторно включите dynamics.</span><span class="sxs-lookup"><span data-stu-id="4d295-114">After your solution adds the shapes, re-enable dynamics.</span></span>
  
<span data-ttu-id="4d295-115">Чтобы получить ссылку на ячейку DynamicsOff по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="4d295-115">To get a reference to the DynamicsOff cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4d295-116">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="4d295-116">Cell name:</span></span>  <br/> | <span data-ttu-id="4d295-117">DynamicsOff</span><span class="sxs-lookup"><span data-stu-id="4d295-117">DynamicsOff</span></span>  <br/> |
   
<span data-ttu-id="4d295-118">Для получения ссылки на ячейки DynamicsOff по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="4d295-118">To get a reference to the DynamicsOff cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4d295-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4d295-119">Section index:</span></span>  <br/> |<span data-ttu-id="4d295-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4d295-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4d295-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4d295-121">Row index:</span></span>  <br/> |<span data-ttu-id="4d295-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="4d295-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="4d295-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4d295-123">Cell index:</span></span>  <br/> |<span data-ttu-id="4d295-124">**visPLODynamicsOff**</span><span class="sxs-lookup"><span data-stu-id="4d295-124">**visPLODynamicsOff**</span></span> <br/> |
   

