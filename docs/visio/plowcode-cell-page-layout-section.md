---
title: PlowCode Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251660
localization_priority: Normal
ms.assetid: e43f3d29-7def-d36e-ac64-62f0a389d415
description: Определяет, перемещаются ли размещаемые фигуры, когда вы удаляете размещаемую фигуру рядом с другой размещаемой фигурой на странице документа.
ms.openlocfilehash: 4ea85ddbaf7662305a2a82fc7f0b814019624841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420355"
---
# <a name="plowcode-cell-page-layout-section"></a><span data-ttu-id="81dbd-103">PlowCode Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="81dbd-103">PlowCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="81dbd-104">Определяет, перемещаются ли размещаемые фигуры, когда вы удаляете размещаемую фигуру рядом с другой размещаемой фигурой на странице документа.</span><span class="sxs-lookup"><span data-stu-id="81dbd-104">Determines whether placeable shapes move away when you drop a placeable shape near another placeable shape on the drawing page.</span></span>
  
|<span data-ttu-id="81dbd-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="81dbd-105">**Value**</span></span>|<span data-ttu-id="81dbd-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="81dbd-106">**Description**</span></span>|<span data-ttu-id="81dbd-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="81dbd-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="81dbd-108">нуль</span><span class="sxs-lookup"><span data-stu-id="81dbd-108">0</span></span>  <br/> |<span data-ttu-id="81dbd-109">Не перемещать фигуры</span><span class="sxs-lookup"><span data-stu-id="81dbd-109">Don't move shapes</span></span>  <br/> |<span data-ttu-id="81dbd-110">**висплопловноне**</span><span class="sxs-lookup"><span data-stu-id="81dbd-110">**visPLOPlowNone**</span></span> <br/> |
|<span data-ttu-id="81dbd-111">1,1</span><span class="sxs-lookup"><span data-stu-id="81dbd-111">1</span></span>  <br/> |<span data-ttu-id="81dbd-112">Перемещение фигур</span><span class="sxs-lookup"><span data-stu-id="81dbd-112">Move shapes</span></span>  <br/> |<span data-ttu-id="81dbd-113">**висплопловалл**</span><span class="sxs-lookup"><span data-stu-id="81dbd-113">**visPLOPlowAll**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81dbd-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="81dbd-114">Remarks</span></span>

<span data-ttu-id="81dbd-115">Значение этой ячейки также можно задать на вкладке **Макет и маршрутизация** в диалоговом окне **Параметры страницы** (на вкладке **конструктор** щелкните стрелку **Параметры страницы** ), используя флажок **переместить другие фигуры при** снятом флажке.</span><span class="sxs-lookup"><span data-stu-id="81dbd-115">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) by using the **Move other shapes away on drop** check box.</span></span> 
  
<span data-ttu-id="81dbd-116">Чтобы получить ссылку на ячейку PlowCode по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="81dbd-116">To get a reference to the PlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81dbd-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="81dbd-117">Cell name:</span></span>  <br/> |<span data-ttu-id="81dbd-118">PlowCode</span><span class="sxs-lookup"><span data-stu-id="81dbd-118">PlowCode</span></span>  <br/> |
   
<span data-ttu-id="81dbd-119">Чтобы получить ссылку на ячейку PlowCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="81dbd-119">To get a reference to the PlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81dbd-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="81dbd-120">Section index:</span></span>  <br/> |<span data-ttu-id="81dbd-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="81dbd-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="81dbd-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="81dbd-122">Row index:</span></span>  <br/> |<span data-ttu-id="81dbd-123">**висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="81dbd-123">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="81dbd-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="81dbd-124">Cell index:</span></span>  <br/> |<span data-ttu-id="81dbd-125">**висплопловкоде**</span><span class="sxs-lookup"><span data-stu-id="81dbd-125">**visPLOPlowCode**</span></span> <br/> |
   

