---
title: Ячейка LineAdjustTo (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
localization_priority: Normal
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: Определяет, какие динамических соединители выровнять друг на друга.
ms.openlocfilehash: 13540f9dc5e6e6861d3f3679bcf49204d553397a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814078"
---
# <a name="lineadjustto-cell-page-layout-section"></a><span data-ttu-id="0ecb7-103">Ячейка LineAdjustTo (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="0ecb7-103">LineAdjustTo Cell (Page Layout Section)</span></span>

<span data-ttu-id="0ecb7-104">Определяет, какие динамических соединители выровнять друг на друга.</span><span class="sxs-lookup"><span data-stu-id="0ecb7-104">Determines which dynamic connectors line up on top of one another.</span></span>
  
|<span data-ttu-id="0ecb7-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="0ecb7-105">**Value**</span></span>|<span data-ttu-id="0ecb7-106">**Корректировка**</span><span class="sxs-lookup"><span data-stu-id="0ecb7-106">**Adjustment**</span></span>|<span data-ttu-id="0ecb7-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="0ecb7-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0ecb7-108">0</span><span class="sxs-lookup"><span data-stu-id="0ecb7-108">0</span></span>  <br/> |<span data-ttu-id="0ecb7-109">Маршрутизации по умолчанию стилей</span><span class="sxs-lookup"><span data-stu-id="0ecb7-109">Routing style default</span></span>  <br/> |<span data-ttu-id="0ecb7-110">**visPLOLineAdjustToDefault**</span><span class="sxs-lookup"><span data-stu-id="0ecb7-110">**visPLOLineAdjustToDefault**</span></span> <br/> |
|<span data-ttu-id="0ecb7-111">1</span><span class="sxs-lookup"><span data-stu-id="0ecb7-111">1</span></span>  <br/> |<span data-ttu-id="0ecb7-112">Строки, приближается к друг с другом</span><span class="sxs-lookup"><span data-stu-id="0ecb7-112">Lines that are close to each other</span></span>  <br/> |<span data-ttu-id="0ecb7-113">**visPLOLineAdjustToAll**</span><span class="sxs-lookup"><span data-stu-id="0ecb7-113">**visPLOLineAdjustToAll**</span></span> <br/> |
|<span data-ttu-id="0ecb7-114">2</span><span class="sxs-lookup"><span data-stu-id="0ecb7-114">2</span></span>  <br/> |<span data-ttu-id="0ecb7-115">Без строк-разделителей</span><span class="sxs-lookup"><span data-stu-id="0ecb7-115">No lines</span></span>  <br/> |<span data-ttu-id="0ecb7-116">**visPLOLineAdjustToNone**</span><span class="sxs-lookup"><span data-stu-id="0ecb7-116">**visPLOLineAdjustToNone**</span></span> <br/> |
|<span data-ttu-id="0ecb7-117">3</span><span class="sxs-lookup"><span data-stu-id="0ecb7-117">3</span></span>  <br/> |<span data-ttu-id="0ecb7-118">Связанные строки</span><span class="sxs-lookup"><span data-stu-id="0ecb7-118">Related lines</span></span>  <br/> |<span data-ttu-id="0ecb7-119">**visPLOLineAdjustToRelated**</span><span class="sxs-lookup"><span data-stu-id="0ecb7-119">**visPLOLineAdjustToRelated**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ecb7-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="0ecb7-120">Remarks</span></span>

<span data-ttu-id="0ecb7-121">Значение ячейки также можно настроить на вкладке **Макет и маршрутизации** в диалоговом окне " **Параметры страницы** " (на вкладки " **Конструктор** ", нажмите кнопку со стрелкой **Параметры страницы** и нажмите кнопку **Макет и маршрутизации**).</span><span class="sxs-lookup"><span data-stu-id="0ecb7-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="0ecb7-122">Чтобы получить ссылку на ячейку LineAdjustTo по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0ecb7-122">To get a reference to the LineAdjustTo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ecb7-123">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="0ecb7-123">Cell name:</span></span>  <br/> |<span data-ttu-id="0ecb7-124">LineAdjustTo</span><span class="sxs-lookup"><span data-stu-id="0ecb7-124">LineAdjustTo</span></span>  <br/> |
   
<span data-ttu-id="0ecb7-125">Для получения ссылки на ячейки LineAdjustTo по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="0ecb7-125">To get a reference to the LineAdjustTo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ecb7-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0ecb7-126">Section index:</span></span>  <br/> |<span data-ttu-id="0ecb7-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0ecb7-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0ecb7-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0ecb7-128">Row index:</span></span>  <br/> |<span data-ttu-id="0ecb7-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="0ecb7-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="0ecb7-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0ecb7-130">Cell index:</span></span>  <br/> |<span data-ttu-id="0ecb7-131">**visPLOLineAdjustTo**</span><span class="sxs-lookup"><span data-stu-id="0ecb7-131">**visPLOLineAdjustTo**</span></span> <br/> |
   

