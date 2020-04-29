---
title: LineAdjustTo Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
localization_priority: Normal
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: Определяет, какая из динамических соединителей находится сверху друг от друга.
ms.openlocfilehash: e4fb32c0fcb488173324ea597edc2c9d13f6bfca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414027"
---
# <a name="lineadjustto-cell-page-layout-section"></a><span data-ttu-id="930a3-103">LineAdjustTo Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="930a3-103">LineAdjustTo Cell (Page Layout Section)</span></span>

<span data-ttu-id="930a3-104">Определяет, какая из динамических соединителей находится сверху друг от друга.</span><span class="sxs-lookup"><span data-stu-id="930a3-104">Determines which dynamic connectors line up on top of one another.</span></span>
  
|<span data-ttu-id="930a3-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="930a3-105">**Value**</span></span>|<span data-ttu-id="930a3-106">**Прав**</span><span class="sxs-lookup"><span data-stu-id="930a3-106">**Adjustment**</span></span>|<span data-ttu-id="930a3-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="930a3-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="930a3-108">нуль</span><span class="sxs-lookup"><span data-stu-id="930a3-108">0</span></span>  <br/> |<span data-ttu-id="930a3-109">Стиль маршрутизации по умолчанию</span><span class="sxs-lookup"><span data-stu-id="930a3-109">Routing style default</span></span>  <br/> |<span data-ttu-id="930a3-110">**висплолинеаджусттодефаулт**</span><span class="sxs-lookup"><span data-stu-id="930a3-110">**visPLOLineAdjustToDefault**</span></span> <br/> |
|<span data-ttu-id="930a3-111">1,1</span><span class="sxs-lookup"><span data-stu-id="930a3-111">1</span></span>  <br/> |<span data-ttu-id="930a3-112">Линии, близкие друг к другу</span><span class="sxs-lookup"><span data-stu-id="930a3-112">Lines that are close to each other</span></span>  <br/> |<span data-ttu-id="930a3-113">**висплолинеаджусттоалл**</span><span class="sxs-lookup"><span data-stu-id="930a3-113">**visPLOLineAdjustToAll**</span></span> <br/> |
|<span data-ttu-id="930a3-114">2</span><span class="sxs-lookup"><span data-stu-id="930a3-114">2</span></span>  <br/> |<span data-ttu-id="930a3-115">Нет строк</span><span class="sxs-lookup"><span data-stu-id="930a3-115">No lines</span></span>  <br/> |<span data-ttu-id="930a3-116">**висплолинеаджусттононе**</span><span class="sxs-lookup"><span data-stu-id="930a3-116">**visPLOLineAdjustToNone**</span></span> <br/> |
|<span data-ttu-id="930a3-117">4</span><span class="sxs-lookup"><span data-stu-id="930a3-117">3</span></span>  <br/> |<span data-ttu-id="930a3-118">Связанные линии</span><span class="sxs-lookup"><span data-stu-id="930a3-118">Related lines</span></span>  <br/> |<span data-ttu-id="930a3-119">**висплолинеаджустторелатед**</span><span class="sxs-lookup"><span data-stu-id="930a3-119">**visPLOLineAdjustToRelated**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="930a3-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="930a3-120">Remarks</span></span>

<span data-ttu-id="930a3-121">Значение этой ячейки также можно задать на вкладке **Макет и маршрутизация** в диалоговом окне **Параметры страницы** (на вкладке **конструктор** щелкните стрелку **Параметры страницы** , а затем выберите **Макет и маршрутизация**).</span><span class="sxs-lookup"><span data-stu-id="930a3-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="930a3-122">Чтобы получить ссылку на ячейку LineAdjustTo по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="930a3-122">To get a reference to the LineAdjustTo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="930a3-123">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="930a3-123">Cell name:</span></span>  <br/> |<span data-ttu-id="930a3-124">LineAdjustTo</span><span class="sxs-lookup"><span data-stu-id="930a3-124">LineAdjustTo</span></span>  <br/> |
   
<span data-ttu-id="930a3-125">Чтобы получить ссылку на ячейку LineAdjustTo по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="930a3-125">To get a reference to the LineAdjustTo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="930a3-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="930a3-126">Section index:</span></span>  <br/> |<span data-ttu-id="930a3-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="930a3-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="930a3-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="930a3-128">Row index:</span></span>  <br/> |<span data-ttu-id="930a3-129">**висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="930a3-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="930a3-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="930a3-130">Cell index:</span></span>  <br/> |<span data-ttu-id="930a3-131">**висплолинеаджустто**</span><span class="sxs-lookup"><span data-stu-id="930a3-131">**visPLOLineAdjustTo**</span></span> <br/> |
   

