---
title: Ячейка EnableGrid (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251642
localization_priority: Normal
ms.assetid: bfea4ef4-1b30-eb22-215d-3b9b73098da9
description: Определяет, будет ли приложение размещает фигур на основе по сетке внутренним, невидимой страницы при настройке макета в диалоговом окне "Настройка макета". (На вкладке конструктор в группе макет нажмите кнопку Изменить расположение и нажмите кнопку Дополнительные параметры макета.)
ms.openlocfilehash: 3371767343132219ebc38134b93afd1da46c7a45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813682"
---
# <a name="enablegrid-cell-page-layout-section"></a><span data-ttu-id="35fda-104">Ячейка EnableGrid (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="35fda-104">EnableGrid Cell (Page Layout Section)</span></span>

<span data-ttu-id="35fda-105">Определяет, будет ли приложение размещает фигур на основе по сетке внутренним, невидимой страницы при настройке макета в диалоговом окне " **Настройка макета** ".</span><span class="sxs-lookup"><span data-stu-id="35fda-105">Determines whether the application lays out shapes based on an internal, invisible page grid when you configure the layout in the **Configure Layout** dialog box.</span></span> <span data-ttu-id="35fda-106">(На вкладке **Конструктор** в группе **Макет** нажмите кнопку **Изменить расположение**и нажмите кнопку **Дополнительные параметры макета**.)</span><span class="sxs-lookup"><span data-stu-id="35fda-106">(On the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**.)</span></span>
  
|<span data-ttu-id="35fda-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="35fda-107">**Value**</span></span>|<span data-ttu-id="35fda-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="35fda-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="35fda-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="35fda-109">TRUE</span></span>  <br/> |<span data-ttu-id="35fda-110">Используйте сетку внутренней страницы.</span><span class="sxs-lookup"><span data-stu-id="35fda-110">Use the internal page grid.</span></span>  <br/> |
|<span data-ttu-id="35fda-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="35fda-111">FALSE</span></span>  <br/> |<span data-ttu-id="35fda-112">Не используйте сетку внутренней страницы.</span><span class="sxs-lookup"><span data-stu-id="35fda-112">Do not use the internal page grid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35fda-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="35fda-113">Remarks</span></span>

<span data-ttu-id="35fda-114">Создание сетки страницы с помощью **пространство между фигурами** и их значения **Средний размер фигуры** в диалоговом окне **Макет и маршрутизация интервалы** .</span><span class="sxs-lookup"><span data-stu-id="35fda-114">You create this page grid by using the **Space between shapes** and the **Average shape size** values in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="35fda-115">(На вкладке **Конструктор** щелкните стрелку **Параметры страницы** , нажмите кнопку **Макет и маршрутизации**и нажмите кнопку **интервалы**.)</span><span class="sxs-lookup"><span data-stu-id="35fda-115">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span> 
  
<span data-ttu-id="35fda-116">Если эта функция включена, приложения выравнивание центральной точки каждого размещаемой фигуры с центром блокировки сетки внутренней страницы.</span><span class="sxs-lookup"><span data-stu-id="35fda-116">When you enable this feature, the application aligns each placeable shape's center point with the center of a block on the internal page grid.</span></span> 
  
<span data-ttu-id="35fda-117">Чтобы получить ссылку на ячейку EnableGrid по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="35fda-117">To get a reference to the EnableGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35fda-118">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="35fda-118">Cell name:</span></span>  <br/> |<span data-ttu-id="35fda-119">EnableGrid</span><span class="sxs-lookup"><span data-stu-id="35fda-119">EnableGrid</span></span>  <br/> |
   
<span data-ttu-id="35fda-120">Для получения ссылки на ячейки EnableGrid по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="35fda-120">To get a reference to the EnableGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35fda-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="35fda-121">Section index:</span></span>  <br/> |<span data-ttu-id="35fda-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="35fda-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="35fda-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="35fda-123">Row index:</span></span>  <br/> |<span data-ttu-id="35fda-124">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="35fda-124">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="35fda-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="35fda-125">Cell index:</span></span>  <br/> |<span data-ttu-id="35fda-126">**visPLOEnableGrid**</span><span class="sxs-lookup"><span data-stu-id="35fda-126">**visPLOEnableGrid**</span></span> <br/> |
   

