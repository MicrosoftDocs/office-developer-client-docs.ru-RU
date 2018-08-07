---
title: Ячейка LineAdjustFrom (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251887
localization_priority: Normal
ms.assetid: 6949c717-dc69-1d17-5215-eb6efce56fcb
description: Определяет, какие динамических соединители пробелы приложения друг от друга, если они маршрутизировать друг на друга.
ms.openlocfilehash: ee3a107f7e19b53017c2ea24c94babceb49620d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814067"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a><span data-ttu-id="822d8-103">Ячейка LineAdjustFrom (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="822d8-103">LineAdjustFrom Cell (Page Layout Section)</span></span>

<span data-ttu-id="822d8-104">Определяет, какие динамических соединители пробелы приложения друг от друга, если они маршрутизировать друг на друга.</span><span class="sxs-lookup"><span data-stu-id="822d8-104">Determines which dynamic connectors the application spaces apart if they route on top of each other.</span></span>
  
|<span data-ttu-id="822d8-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="822d8-105">**Value**</span></span>|<span data-ttu-id="822d8-106">**Корректировка**</span><span class="sxs-lookup"><span data-stu-id="822d8-106">**Adjustment**</span></span>|<span data-ttu-id="822d8-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="822d8-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="822d8-108">0</span><span class="sxs-lookup"><span data-stu-id="822d8-108">0</span></span>  <br/> |<span data-ttu-id="822d8-109">Несвязанные линии</span><span class="sxs-lookup"><span data-stu-id="822d8-109">Unrelated lines</span></span>  <br/> |<span data-ttu-id="822d8-110">**visPLOLineAdjustFromNotRelated**</span><span class="sxs-lookup"><span data-stu-id="822d8-110">**visPLOLineAdjustFromNotRelated**</span></span> <br/> |
|<span data-ttu-id="822d8-111">1</span><span class="sxs-lookup"><span data-stu-id="822d8-111">1</span></span>  <br/> |<span data-ttu-id="822d8-112">Все строки</span><span class="sxs-lookup"><span data-stu-id="822d8-112">All lines</span></span>  <br/> |<span data-ttu-id="822d8-113">**visPLOLineAdjustFromAll**</span><span class="sxs-lookup"><span data-stu-id="822d8-113">**visPLOLineAdjustFromAll**</span></span> <br/> |
|<span data-ttu-id="822d8-114">2</span><span class="sxs-lookup"><span data-stu-id="822d8-114">2</span></span>  <br/> |<span data-ttu-id="822d8-115">Без строк-разделителей</span><span class="sxs-lookup"><span data-stu-id="822d8-115">No lines</span></span>  <br/> |<span data-ttu-id="822d8-116">**visPLOLineAdjustFromNone**</span><span class="sxs-lookup"><span data-stu-id="822d8-116">**visPLOLineAdjustFromNone**</span></span> <br/> |
|<span data-ttu-id="822d8-117">3</span><span class="sxs-lookup"><span data-stu-id="822d8-117">3</span></span>  <br/> |<span data-ttu-id="822d8-118">Маршрутизации по умолчанию стилей</span><span class="sxs-lookup"><span data-stu-id="822d8-118">Routing style default</span></span>  <br/> |<span data-ttu-id="822d8-119">**visPLOLineAdjustFromRoutingDefault**</span><span class="sxs-lookup"><span data-stu-id="822d8-119">**visPLOLineAdjustFromRoutingDefault**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="822d8-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="822d8-120">Remarks</span></span>

<span data-ttu-id="822d8-121">Значение ячейки также можно настроить на вкладке **Макет и маршрутизации** в диалоговом окне " **Параметры страницы** " (на вкладки " **Конструктор** ", нажмите кнопку со стрелкой **Параметры страницы** и нажмите кнопку **Макет и маршрутизации**).</span><span class="sxs-lookup"><span data-stu-id="822d8-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="822d8-122">Чтобы получить ссылку на ячейку LineAdjustFrom по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="822d8-122">To get a reference to the LineAdjustFrom cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="822d8-123">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="822d8-123">Cell name:</span></span>  <br/> |<span data-ttu-id="822d8-124">LineAdjustFrom</span><span class="sxs-lookup"><span data-stu-id="822d8-124">LineAdjustFrom</span></span>  <br/> |
   
<span data-ttu-id="822d8-125">Для получения ссылки на ячейки LineAdjustFrom по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="822d8-125">To get a reference to the LineAdjustFrom cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="822d8-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="822d8-126">Section index:</span></span>  <br/> |<span data-ttu-id="822d8-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="822d8-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="822d8-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="822d8-128">Row index:</span></span>  <br/> |<span data-ttu-id="822d8-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="822d8-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="822d8-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="822d8-130">Cell index:</span></span>  <br/> |<span data-ttu-id="822d8-131">**visPLOLineAdjustFrom**</span><span class="sxs-lookup"><span data-stu-id="822d8-131">**visPLOLineAdjustFrom**</span></span> <br/> |
   

