---
title: LineAdjustFrom Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251887
localization_priority: Normal
ms.assetid: 6949c717-dc69-1d17-5215-eb6efce56fcb
description: Определяет, какие динамические соединители пространство приложения друг от друга, если они следования друг на друга.
ms.openlocfilehash: 3eb9f5513ee3ce2f5dce96cb47c356bca29a289c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415189"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a><span data-ttu-id="b745f-103">LineAdjustFrom Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="b745f-103">LineAdjustFrom Cell (Page Layout Section)</span></span>

<span data-ttu-id="b745f-104">Определяет, какие динамические соединители пространство приложения друг от друга, если они следования друг на друга.</span><span class="sxs-lookup"><span data-stu-id="b745f-104">Determines which dynamic connectors the application spaces apart if they route on top of each other.</span></span>
  
|<span data-ttu-id="b745f-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b745f-105">**Value**</span></span>|<span data-ttu-id="b745f-106">**Регулировка**</span><span class="sxs-lookup"><span data-stu-id="b745f-106">**Adjustment**</span></span>|<span data-ttu-id="b745f-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="b745f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b745f-108">0</span><span class="sxs-lookup"><span data-stu-id="b745f-108">0</span></span>  <br/> |<span data-ttu-id="b745f-109">Несвязанные строки</span><span class="sxs-lookup"><span data-stu-id="b745f-109">Unrelated lines</span></span>  <br/> |<span data-ttu-id="b745f-110">**visPLOLineAdjustFromNotRelated**</span><span class="sxs-lookup"><span data-stu-id="b745f-110">**visPLOLineAdjustFromNotRelated**</span></span> <br/> |
|<span data-ttu-id="b745f-111">1</span><span class="sxs-lookup"><span data-stu-id="b745f-111">1</span></span>  <br/> |<span data-ttu-id="b745f-112">Все строки</span><span class="sxs-lookup"><span data-stu-id="b745f-112">All lines</span></span>  <br/> |<span data-ttu-id="b745f-113">**visPLOLineAdjustFromAll**</span><span class="sxs-lookup"><span data-stu-id="b745f-113">**visPLOLineAdjustFromAll**</span></span> <br/> |
|<span data-ttu-id="b745f-114">2</span><span class="sxs-lookup"><span data-stu-id="b745f-114">2</span></span>  <br/> |<span data-ttu-id="b745f-115">Нет строк</span><span class="sxs-lookup"><span data-stu-id="b745f-115">No lines</span></span>  <br/> |<span data-ttu-id="b745f-116">**visPLOLineAdjustFromNone**</span><span class="sxs-lookup"><span data-stu-id="b745f-116">**visPLOLineAdjustFromNone**</span></span> <br/> |
|<span data-ttu-id="b745f-117">3</span><span class="sxs-lookup"><span data-stu-id="b745f-117">3</span></span>  <br/> |<span data-ttu-id="b745f-118">По умолчанию стиль маршрутивки</span><span class="sxs-lookup"><span data-stu-id="b745f-118">Routing style default</span></span>  <br/> |<span data-ttu-id="b745f-119">**visPLOLineAdjustFromRoutingDefault**</span><span class="sxs-lookup"><span data-stu-id="b745f-119">**visPLOLineAdjustFromRoutingDefault**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b745f-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="b745f-120">Remarks</span></span>

<span data-ttu-id="b745f-121">Вы также можете установить значение этой ячейки на вкладке  Layout и   **Routing** в диалоговом окне Настройка страницы (на вкладке Дизайн щелкните стрелку установки страницы, а затем нажмите макет и маршрутинг).</span><span class="sxs-lookup"><span data-stu-id="b745f-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="b745f-122">Чтобы получить ссылку на ячейку LineAdjustFrom по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="b745f-122">To get a reference to the LineAdjustFrom cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b745f-123">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b745f-123">Cell name:</span></span>  <br/> |<span data-ttu-id="b745f-124">LineAdjustFrom</span><span class="sxs-lookup"><span data-stu-id="b745f-124">LineAdjustFrom</span></span>  <br/> |
   
<span data-ttu-id="b745f-125">Чтобы получить ссылку на ячейку LineAdjustFrom по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b745f-125">To get a reference to the LineAdjustFrom cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b745f-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b745f-126">Section index:</span></span>  <br/> |<span data-ttu-id="b745f-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b745f-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b745f-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b745f-128">Row index:</span></span>  <br/> |<span data-ttu-id="b745f-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b745f-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="b745f-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b745f-130">Cell index:</span></span>  <br/> |<span data-ttu-id="b745f-131">**visPLOLineAdjustFrom**</span><span class="sxs-lookup"><span data-stu-id="b745f-131">**visPLOLineAdjustFrom**</span></span> <br/> |
   

