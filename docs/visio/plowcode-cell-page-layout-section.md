---
title: Ячейка PlowCode (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251660
localization_priority: Normal
ms.assetid: e43f3d29-7def-d36e-ac64-62f0a389d415
description: Определяет, будет ли размещаемые фигуры перемещение (удаление) при удалении размещаемой фигуры рядом с другой размещаемой фигуры на странице документа.
ms.openlocfilehash: e180ce679f280cbccbda80b67170f2f26473bd8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814404"
---
# <a name="plowcode-cell-page-layout-section"></a><span data-ttu-id="8b363-103">Ячейка PlowCode (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="8b363-103">PlowCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="8b363-104">Определяет, будет ли размещаемые фигуры перемещение (удаление) при удалении размещаемой фигуры рядом с другой размещаемой фигуры на странице документа.</span><span class="sxs-lookup"><span data-stu-id="8b363-104">Determines whether placeable shapes move away when you drop a placeable shape near another placeable shape on the drawing page.</span></span>
  
|<span data-ttu-id="8b363-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8b363-105">**Value**</span></span>|<span data-ttu-id="8b363-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8b363-106">**Description**</span></span>|<span data-ttu-id="8b363-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="8b363-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8b363-108">0</span><span class="sxs-lookup"><span data-stu-id="8b363-108">0</span></span>  <br/> |<span data-ttu-id="8b363-109">Не перемещать фигур</span><span class="sxs-lookup"><span data-stu-id="8b363-109">Don't move shapes</span></span>  <br/> |<span data-ttu-id="8b363-110">**visPLOPlowNone**</span><span class="sxs-lookup"><span data-stu-id="8b363-110">**visPLOPlowNone**</span></span> <br/> |
|<span data-ttu-id="8b363-111">1</span><span class="sxs-lookup"><span data-stu-id="8b363-111">1</span></span>  <br/> |<span data-ttu-id="8b363-112">Перемещение фигур</span><span class="sxs-lookup"><span data-stu-id="8b363-112">Move shapes</span></span>  <br/> |<span data-ttu-id="8b363-113">**visPLOPlowAll**</span><span class="sxs-lookup"><span data-stu-id="8b363-113">**visPLOPlowAll**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b363-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="8b363-114">Remarks</span></span>

<span data-ttu-id="8b363-115">Значение ячейки также можно настроить на вкладке **Макет и маршрутизации** в диалоговом окне " **Параметры страницы** " (на вкладке " **Конструктор** ", щелкните стрелку **Параметры страницы** ) с помощью флажок **Сдвигать другие фигуры при размещении** .</span><span class="sxs-lookup"><span data-stu-id="8b363-115">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) by using the **Move other shapes away on drop** check box.</span></span> 
  
<span data-ttu-id="8b363-116">Чтобы получить ссылку на ячейку PlowCode по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="8b363-116">To get a reference to the PlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b363-117">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="8b363-117">Cell name:</span></span>  <br/> |<span data-ttu-id="8b363-118">PlowCode</span><span class="sxs-lookup"><span data-stu-id="8b363-118">PlowCode</span></span>  <br/> |
   
<span data-ttu-id="8b363-119">Для получения ссылки на ячейки PlowCode по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="8b363-119">To get a reference to the PlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b363-120">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8b363-120">Section index:</span></span>  <br/> |<span data-ttu-id="8b363-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8b363-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8b363-122">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8b363-122">Row index:</span></span>  <br/> |<span data-ttu-id="8b363-123">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="8b363-123">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="8b363-124">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8b363-124">Cell index:</span></span>  <br/> |<span data-ttu-id="8b363-125">**visPLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="8b363-125">**visPLOPlowCode**</span></span> <br/> |
   

