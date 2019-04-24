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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344375"
---
# <a name="plowcode-cell-page-layout-section"></a><span data-ttu-id="4b9f7-103">PlowCode Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="4b9f7-103">PlowCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="4b9f7-104">Определяет, перемещаются ли размещаемые фигуры, когда вы удаляете размещаемую фигуру рядом с другой размещаемой фигурой на странице документа.</span><span class="sxs-lookup"><span data-stu-id="4b9f7-104">Determines whether placeable shapes move away when you drop a placeable shape near another placeable shape on the drawing page.</span></span>
  
|<span data-ttu-id="4b9f7-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="4b9f7-105">**Value**</span></span>|<span data-ttu-id="4b9f7-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4b9f7-106">**Description**</span></span>|<span data-ttu-id="4b9f7-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="4b9f7-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4b9f7-108">нуль</span><span class="sxs-lookup"><span data-stu-id="4b9f7-108">0</span></span>  <br/> |<span data-ttu-id="4b9f7-109">Не перемещать фигуры</span><span class="sxs-lookup"><span data-stu-id="4b9f7-109">Don't move shapes</span></span>  <br/> |<span data-ttu-id="4b9f7-110">**Висплопловноне**</span><span class="sxs-lookup"><span data-stu-id="4b9f7-110">**visPLOPlowNone**</span></span> <br/> |
|<span data-ttu-id="4b9f7-111">1,1</span><span class="sxs-lookup"><span data-stu-id="4b9f7-111">1</span></span>  <br/> |<span data-ttu-id="4b9f7-112">Перемещение фигур</span><span class="sxs-lookup"><span data-stu-id="4b9f7-112">Move shapes</span></span>  <br/> |<span data-ttu-id="4b9f7-113">**Висплопловалл**</span><span class="sxs-lookup"><span data-stu-id="4b9f7-113">**visPLOPlowAll**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b9f7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b9f7-114">Remarks</span></span>

<span data-ttu-id="4b9f7-115">Значение этой ячейки также можно задать на вкладке **Макет и маршрутизация** в диалоговом окне **Параметры страницы** (на вкладке **конструктор** щелкните стрелку **Параметры страницы** ), используя флажок **переместить другие фигуры при** снятом флажке.</span><span class="sxs-lookup"><span data-stu-id="4b9f7-115">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) by using the **Move other shapes away on drop** check box.</span></span> 
  
<span data-ttu-id="4b9f7-116">Чтобы получить ссылку на ячейку PlowCode по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="4b9f7-116">To get a reference to the PlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4b9f7-117">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="4b9f7-117">Cell name:</span></span>  <br/> |<span data-ttu-id="4b9f7-118">PlowCode</span><span class="sxs-lookup"><span data-stu-id="4b9f7-118">PlowCode</span></span>  <br/> |
   
<span data-ttu-id="4b9f7-119">Чтобы получить ссылку на ячейку PlowCode по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="4b9f7-119">To get a reference to the PlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4b9f7-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4b9f7-120">Section index:</span></span>  <br/> |<span data-ttu-id="4b9f7-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4b9f7-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4b9f7-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4b9f7-122">Row index:</span></span>  <br/> |<span data-ttu-id="4b9f7-123">**Висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="4b9f7-123">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="4b9f7-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4b9f7-124">Cell index:</span></span>  <br/> |<span data-ttu-id="4b9f7-125">**Висплопловкоде**</span><span class="sxs-lookup"><span data-stu-id="4b9f7-125">**visPLOPlowCode**</span></span> <br/> |
   

