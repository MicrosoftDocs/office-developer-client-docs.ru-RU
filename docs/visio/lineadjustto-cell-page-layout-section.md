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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359313"
---
# <a name="lineadjustto-cell-page-layout-section"></a><span data-ttu-id="b4b30-103">LineAdjustTo Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="b4b30-103">LineAdjustTo Cell (Page Layout Section)</span></span>

<span data-ttu-id="b4b30-104">Определяет, какая из динамических соединителей находится сверху друг от друга.</span><span class="sxs-lookup"><span data-stu-id="b4b30-104">Determines which dynamic connectors line up on top of one another.</span></span>
  
|<span data-ttu-id="b4b30-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b4b30-105">**Value**</span></span>|<span data-ttu-id="b4b30-106">**Прав**</span><span class="sxs-lookup"><span data-stu-id="b4b30-106">**Adjustment**</span></span>|<span data-ttu-id="b4b30-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="b4b30-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b4b30-108">нуль</span><span class="sxs-lookup"><span data-stu-id="b4b30-108">0</span></span>  <br/> |<span data-ttu-id="b4b30-109">Стиль маршрутизации по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b4b30-109">Routing style default</span></span>  <br/> |<span data-ttu-id="b4b30-110">**Висплолинеаджусттодефаулт**</span><span class="sxs-lookup"><span data-stu-id="b4b30-110">**visPLOLineAdjustToDefault**</span></span> <br/> |
|<span data-ttu-id="b4b30-111">1,1</span><span class="sxs-lookup"><span data-stu-id="b4b30-111">1</span></span>  <br/> |<span data-ttu-id="b4b30-112">Линии, близкие друг к другу</span><span class="sxs-lookup"><span data-stu-id="b4b30-112">Lines that are close to each other</span></span>  <br/> |<span data-ttu-id="b4b30-113">**Висплолинеаджусттоалл**</span><span class="sxs-lookup"><span data-stu-id="b4b30-113">**visPLOLineAdjustToAll**</span></span> <br/> |
|<span data-ttu-id="b4b30-114">2</span><span class="sxs-lookup"><span data-stu-id="b4b30-114">2</span></span>  <br/> |<span data-ttu-id="b4b30-115">Нет строк</span><span class="sxs-lookup"><span data-stu-id="b4b30-115">No lines</span></span>  <br/> |<span data-ttu-id="b4b30-116">**Висплолинеаджусттононе**</span><span class="sxs-lookup"><span data-stu-id="b4b30-116">**visPLOLineAdjustToNone**</span></span> <br/> |
|<span data-ttu-id="b4b30-117">4</span><span class="sxs-lookup"><span data-stu-id="b4b30-117">3</span></span>  <br/> |<span data-ttu-id="b4b30-118">Связанные линии</span><span class="sxs-lookup"><span data-stu-id="b4b30-118">Related lines</span></span>  <br/> |<span data-ttu-id="b4b30-119">**Висплолинеаджустторелатед**</span><span class="sxs-lookup"><span data-stu-id="b4b30-119">**visPLOLineAdjustToRelated**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4b30-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4b30-120">Remarks</span></span>

<span data-ttu-id="b4b30-121">Значение этой ячейки также можно задать на вкладке **Макет и маршрутизация** в диалоговом окне **Параметры страницы** (на вкладке **конструктор** щелкните стрелку **Параметры страницы** , а затем выберите **Макет и маршрутизация**).</span><span class="sxs-lookup"><span data-stu-id="b4b30-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="b4b30-122">Чтобы получить ссылку на ячейку LineAdjustTo по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="b4b30-122">To get a reference to the LineAdjustTo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4b30-123">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b4b30-123">Cell name:</span></span>  <br/> |<span data-ttu-id="b4b30-124">LineAdjustTo</span><span class="sxs-lookup"><span data-stu-id="b4b30-124">LineAdjustTo</span></span>  <br/> |
   
<span data-ttu-id="b4b30-125">Чтобы получить ссылку на ячейку LineAdjustTo по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b4b30-125">To get a reference to the LineAdjustTo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4b30-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b4b30-126">Section index:</span></span>  <br/> |<span data-ttu-id="b4b30-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b4b30-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b4b30-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b4b30-128">Row index:</span></span>  <br/> |<span data-ttu-id="b4b30-129">**Висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="b4b30-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="b4b30-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b4b30-130">Cell index:</span></span>  <br/> |<span data-ttu-id="b4b30-131">**Висплолинеаджустто**</span><span class="sxs-lookup"><span data-stu-id="b4b30-131">**visPLOLineAdjustTo**</span></span> <br/> |
   

