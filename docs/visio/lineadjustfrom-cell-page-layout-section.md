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
description: Определяет, какие динамические соединители разделяются между приложениями, если они направляются друг на друга.
ms.openlocfilehash: 3eb9f5513ee3ce2f5dce96cb47c356bca29a289c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415189"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a><span data-ttu-id="87f25-103">LineAdjustFrom Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="87f25-103">LineAdjustFrom Cell (Page Layout Section)</span></span>

<span data-ttu-id="87f25-104">Определяет, какие динамические соединители разделяются между приложениями, если они направляются друг на друга.</span><span class="sxs-lookup"><span data-stu-id="87f25-104">Determines which dynamic connectors the application spaces apart if they route on top of each other.</span></span>
  
|<span data-ttu-id="87f25-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="87f25-105">**Value**</span></span>|<span data-ttu-id="87f25-106">**Прав**</span><span class="sxs-lookup"><span data-stu-id="87f25-106">**Adjustment**</span></span>|<span data-ttu-id="87f25-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="87f25-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="87f25-108">нуль</span><span class="sxs-lookup"><span data-stu-id="87f25-108">0</span></span>  <br/> |<span data-ttu-id="87f25-109">Несвязанные линии</span><span class="sxs-lookup"><span data-stu-id="87f25-109">Unrelated lines</span></span>  <br/> |<span data-ttu-id="87f25-110">**Висплолинеаджустфромнотрелатед**</span><span class="sxs-lookup"><span data-stu-id="87f25-110">**visPLOLineAdjustFromNotRelated**</span></span> <br/> |
|<span data-ttu-id="87f25-111">1,1</span><span class="sxs-lookup"><span data-stu-id="87f25-111">1</span></span>  <br/> |<span data-ttu-id="87f25-112">Все строки</span><span class="sxs-lookup"><span data-stu-id="87f25-112">All lines</span></span>  <br/> |<span data-ttu-id="87f25-113">**Висплолинеаджустфромалл**</span><span class="sxs-lookup"><span data-stu-id="87f25-113">**visPLOLineAdjustFromAll**</span></span> <br/> |
|<span data-ttu-id="87f25-114">2</span><span class="sxs-lookup"><span data-stu-id="87f25-114">2</span></span>  <br/> |<span data-ttu-id="87f25-115">Нет строк</span><span class="sxs-lookup"><span data-stu-id="87f25-115">No lines</span></span>  <br/> |<span data-ttu-id="87f25-116">**Висплолинеаджустфромноне**</span><span class="sxs-lookup"><span data-stu-id="87f25-116">**visPLOLineAdjustFromNone**</span></span> <br/> |
|<span data-ttu-id="87f25-117">4</span><span class="sxs-lookup"><span data-stu-id="87f25-117">3</span></span>  <br/> |<span data-ttu-id="87f25-118">Стиль маршрутизации по умолчанию</span><span class="sxs-lookup"><span data-stu-id="87f25-118">Routing style default</span></span>  <br/> |<span data-ttu-id="87f25-119">**Висплолинеаджустфромраутингдефаулт**</span><span class="sxs-lookup"><span data-stu-id="87f25-119">**visPLOLineAdjustFromRoutingDefault**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87f25-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="87f25-120">Remarks</span></span>

<span data-ttu-id="87f25-121">Значение этой ячейки также можно задать на вкладке **Макет и маршрутизация** в диалоговом окне **Параметры страницы** (на вкладке **конструктор** щелкните стрелку **Параметры страницы** , а затем выберите **Макет и маршрутизация**).</span><span class="sxs-lookup"><span data-stu-id="87f25-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="87f25-122">Чтобы получить ссылку на ячейку Линеаджустфром по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="87f25-122">To get a reference to the LineAdjustFrom cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87f25-123">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="87f25-123">Cell name:</span></span>  <br/> |<span data-ttu-id="87f25-124">Линеаджустфром</span><span class="sxs-lookup"><span data-stu-id="87f25-124">LineAdjustFrom</span></span>  <br/> |
   
<span data-ttu-id="87f25-125">Чтобы получить ссылку на ячейку Линеаджустфром по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="87f25-125">To get a reference to the LineAdjustFrom cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87f25-126">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="87f25-126">Section index:</span></span>  <br/> |<span data-ttu-id="87f25-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="87f25-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="87f25-128">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="87f25-128">Row index:</span></span>  <br/> |<span data-ttu-id="87f25-129">**Висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="87f25-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="87f25-130">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="87f25-130">Cell index:</span></span>  <br/> |<span data-ttu-id="87f25-131">**Висплолинеаджустфром**</span><span class="sxs-lookup"><span data-stu-id="87f25-131">**visPLOLineAdjustFrom**</span></span> <br/> |
   

