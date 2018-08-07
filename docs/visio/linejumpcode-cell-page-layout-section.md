---
title: Ячейка LineJumpCode (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm540
localization_priority: Normal
ms.assetid: 56f9043d-a632-65df-c710-45867cce1627
description: Определяет соединители, к которым требуется добавить переходы.
ms.openlocfilehash: abb7208c2cfbd6b1423e091efc1d526f8b10b57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814075"
---
# <a name="linejumpcode-cell-page-layout-section"></a><span data-ttu-id="04183-103">Ячейка LineJumpCode (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="04183-103">LineJumpCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="04183-104">Определяет соединители, к которым требуется добавить переходы.</span><span class="sxs-lookup"><span data-stu-id="04183-104">Determines the connectors to which you want to add jumps.</span></span>
  
|<span data-ttu-id="04183-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="04183-105">**Value**</span></span>|<span data-ttu-id="04183-106">**Соединители, к которым требуется добавить переходы**</span><span class="sxs-lookup"><span data-stu-id="04183-106">**Connectors to which you want to add jumps**</span></span>|<span data-ttu-id="04183-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="04183-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="04183-108">0</span><span class="sxs-lookup"><span data-stu-id="04183-108">0</span></span>  <br/> |<span data-ttu-id="04183-109">Нет</span><span class="sxs-lookup"><span data-stu-id="04183-109">None</span></span>  <br/> |<span data-ttu-id="04183-110">**visPLOJumpNone**</span><span class="sxs-lookup"><span data-stu-id="04183-110">**visPLOJumpNone**</span></span> <br/> |
|<span data-ttu-id="04183-111">1</span><span class="sxs-lookup"><span data-stu-id="04183-111">1</span></span>  <br/> |<span data-ttu-id="04183-112">Горизонтальные линии</span><span class="sxs-lookup"><span data-stu-id="04183-112">Horizontal lines</span></span>  <br/> |<span data-ttu-id="04183-113">**visPLOJumpHorizontal**</span><span class="sxs-lookup"><span data-stu-id="04183-113">**visPLOJumpHorizontal**</span></span> <br/> |
|<span data-ttu-id="04183-114">2</span><span class="sxs-lookup"><span data-stu-id="04183-114">2</span></span>  <br/> |<span data-ttu-id="04183-115">Вертикальные линии</span><span class="sxs-lookup"><span data-stu-id="04183-115">Vertical lines</span></span>  <br/> |<span data-ttu-id="04183-116">**visPLOJumpVertical**</span><span class="sxs-lookup"><span data-stu-id="04183-116">**visPLOJumpVertical**</span></span> <br/> |
|<span data-ttu-id="04183-117">3</span><span class="sxs-lookup"><span data-stu-id="04183-117">3</span></span>  <br/> |<span data-ttu-id="04183-118">Последняя строка маршрутизации</span><span class="sxs-lookup"><span data-stu-id="04183-118">Last routed line</span></span>  <br/> |<span data-ttu-id="04183-119">**visPLOJumpLastRouted**</span><span class="sxs-lookup"><span data-stu-id="04183-119">**visPLOJumpLastRouted**</span></span> <br/> |
|<span data-ttu-id="04183-120">4</span><span class="sxs-lookup"><span data-stu-id="04183-120">4</span></span>  <br/> |<span data-ttu-id="04183-121">Предыдущей строки (Основные фигуры в *z* -порядке)</span><span class="sxs-lookup"><span data-stu-id="04183-121">Last displayed line (top shape in the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="04183-122">**visPLOJumpDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="04183-122">**visPLOJumpDisplayOrder**</span></span> <br/> |
|<span data-ttu-id="04183-123">5</span><span class="sxs-lookup"><span data-stu-id="04183-123">5</span></span>  <br/> |<span data-ttu-id="04183-124">Сначала отображается строка (фигуры в нижней части *z* -порядке)</span><span class="sxs-lookup"><span data-stu-id="04183-124">First displayed line (shape at the bottom of the  *z*  -order)</span></span>  <br/> |<span data-ttu-id="04183-125">**visPLOJumpReverseDisplayOrder**</span><span class="sxs-lookup"><span data-stu-id="04183-125">**visPLOJumpReverseDisplayOrder**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04183-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="04183-126">Remarks</span></span>

<span data-ttu-id="04183-127">Значение ячейки также можно настроить на вкладке **Макет и маршрутизации** в диалоговом окне " **Параметры страницы** " (на вкладки " **Конструктор** ", нажмите кнопку со стрелкой **Параметры страницы** и нажмите кнопку **Макет и маршрутизации**).</span><span class="sxs-lookup"><span data-stu-id="04183-127">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="04183-128">Чтобы получить ссылку на ячейку LineJumpCode по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="04183-128">To get a reference to the LineJumpCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="04183-129">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="04183-129">Cell name:</span></span>  <br/> |<span data-ttu-id="04183-130">LineJumpCode</span><span class="sxs-lookup"><span data-stu-id="04183-130">LineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="04183-131">Для получения ссылки на ячейки LineJumpCode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="04183-131">To get a reference to the LineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="04183-132">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="04183-132">Section index:</span></span>  <br/> |<span data-ttu-id="04183-133">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="04183-133">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="04183-134">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="04183-134">Row index:</span></span>  <br/> |<span data-ttu-id="04183-135">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="04183-135">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="04183-136">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="04183-136">Cell index:</span></span>  <br/> |<span data-ttu-id="04183-137">**visPLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="04183-137">**visPLOJumpCode**</span></span> <br/> |
   

