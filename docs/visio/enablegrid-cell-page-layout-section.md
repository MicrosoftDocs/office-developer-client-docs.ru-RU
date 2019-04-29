---
title: EnableGrid Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251642
localization_priority: Normal
ms.assetid: bfea4ef4-1b30-eb22-215d-3b9b73098da9
description: Определяет, размещает ли приложение фигуры на основе внутренней невидимой сетки страницы при настройке макета в диалоговом окне "Настройка макета". (На вкладке Конструктор в группе Макет выберите пункт изменить макет страницы, а затем щелкните Дополнительные параметры макета.)
ms.openlocfilehash: 11299ca7c9b0ea050542baf97e2cab3a27fa52ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424443"
---
# <a name="enablegrid-cell-page-layout-section"></a><span data-ttu-id="bcee8-104">EnableGrid Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="bcee8-104">EnableGrid Cell (Page Layout Section)</span></span>

<span data-ttu-id="bcee8-105">Определяет, размещает ли приложение фигуры на основе внутренней невидимой сетки страницы при настройке макета в диалоговом окне " **Настройка макета** ".</span><span class="sxs-lookup"><span data-stu-id="bcee8-105">Determines whether the application lays out shapes based on an internal, invisible page grid when you configure the layout in the **Configure Layout** dialog box.</span></span> <span data-ttu-id="bcee8-106">(На вкладке **конструктор** в группе **Макет** выберите пункт **изменить макет страницы**, а затем щелкните **Дополнительные параметры макета**.)</span><span class="sxs-lookup"><span data-stu-id="bcee8-106">(On the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**.)</span></span>
  
|<span data-ttu-id="bcee8-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="bcee8-107">**Value**</span></span>|<span data-ttu-id="bcee8-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bcee8-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bcee8-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="bcee8-109">TRUE</span></span>  <br/> |<span data-ttu-id="bcee8-110">Используйте внутреннюю сетку страниц.</span><span class="sxs-lookup"><span data-stu-id="bcee8-110">Use the internal page grid.</span></span>  <br/> |
|<span data-ttu-id="bcee8-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="bcee8-111">FALSE</span></span>  <br/> |<span data-ttu-id="bcee8-112">Не используйте внутреннюю сетку страниц.</span><span class="sxs-lookup"><span data-stu-id="bcee8-112">Do not use the internal page grid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcee8-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="bcee8-113">Remarks</span></span>

<span data-ttu-id="bcee8-114">Эта сетка страницы создается с использованием интервала **между фигурами** и **среднего значения размера фигуры** в диалоговом окне **Макет и маршрутизация** .</span><span class="sxs-lookup"><span data-stu-id="bcee8-114">You create this page grid by using the **Space between shapes** and the **Average shape size** values in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="bcee8-115">На вкладке **конструктор** щелкните стрелку **Параметры страницы** , выберите **Макет и маршрутизация**, а затем щелкните интервалы. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="bcee8-115">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span> 
  
<span data-ttu-id="bcee8-116">При включении этой функции приложение выравнивает каждую центральную точку фигуры с помощью центра блока на внутренней сетке страниц.</span><span class="sxs-lookup"><span data-stu-id="bcee8-116">When you enable this feature, the application aligns each placeable shape's center point with the center of a block on the internal page grid.</span></span> 
  
<span data-ttu-id="bcee8-117">Чтобы получить ссылку на ячейку EnableGrid по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="bcee8-117">To get a reference to the EnableGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bcee8-118">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="bcee8-118">Cell name:</span></span>  <br/> |<span data-ttu-id="bcee8-119">EnableGrid</span><span class="sxs-lookup"><span data-stu-id="bcee8-119">EnableGrid</span></span>  <br/> |
   
<span data-ttu-id="bcee8-120">Чтобы получить ссылку на ячейку EnableGrid по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="bcee8-120">To get a reference to the EnableGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bcee8-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bcee8-121">Section index:</span></span>  <br/> |<span data-ttu-id="bcee8-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bcee8-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bcee8-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bcee8-123">Row index:</span></span>  <br/> |<span data-ttu-id="bcee8-124">**Висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="bcee8-124">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="bcee8-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bcee8-125">Cell index:</span></span>  <br/> |<span data-ttu-id="bcee8-126">**Висплоенаблегрид**</span><span class="sxs-lookup"><span data-stu-id="bcee8-126">**visPLOEnableGrid**</span></span> <br/> |
   

