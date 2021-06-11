---
title: Type / C Cell (Connection Points Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
localization_priority: Normal
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: Определяет тип точки подключения.
ms.openlocfilehash: a73554d9f3a3bce6a039689d2c0b192a1c5b69aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415238"
---
# <a name="type--c-cell-connection-points-section"></a><span data-ttu-id="e5d24-103">Type / C Cell (Connection Points Section)</span><span class="sxs-lookup"><span data-stu-id="e5d24-103">Type / C Cell (Connection Points Section)</span></span>

<span data-ttu-id="e5d24-104">Определяет тип точки подключения.</span><span class="sxs-lookup"><span data-stu-id="e5d24-104">Determines the connection point type.</span></span>
  
|<span data-ttu-id="e5d24-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e5d24-105">**Value**</span></span>|<span data-ttu-id="e5d24-106">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e5d24-106">**Type**</span></span>|<span data-ttu-id="e5d24-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="e5d24-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e5d24-108">0</span><span class="sxs-lookup"><span data-stu-id="e5d24-108">0</span></span>  <br/> |<span data-ttu-id="e5d24-109">Внутреннее</span><span class="sxs-lookup"><span data-stu-id="e5d24-109">Inward</span></span>  <br/> |<span data-ttu-id="e5d24-110">**visCnnctTypeInward**</span><span class="sxs-lookup"><span data-stu-id="e5d24-110">**visCnnctTypeInward**</span></span> <br/> |
|<span data-ttu-id="e5d24-111">1</span><span class="sxs-lookup"><span data-stu-id="e5d24-111">1</span></span>  <br/> |<span data-ttu-id="e5d24-112">Внешний</span><span class="sxs-lookup"><span data-stu-id="e5d24-112">Outward</span></span>  <br/> |<span data-ttu-id="e5d24-113">**visCnnctTypeOutward**</span><span class="sxs-lookup"><span data-stu-id="e5d24-113">**visCnnctTypeOutward**</span></span> <br/> |
|<span data-ttu-id="e5d24-114">2</span><span class="sxs-lookup"><span data-stu-id="e5d24-114">2</span></span>  <br/> |<span data-ttu-id="e5d24-115">Внутреннее &amp; внешнее</span><span class="sxs-lookup"><span data-stu-id="e5d24-115">Inward &amp; Outward</span></span>  <br/> |<span data-ttu-id="e5d24-116">**visCnnctTypeInwardOutward**</span><span class="sxs-lookup"><span data-stu-id="e5d24-116">**visCnnctTypeInwardOutward**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5d24-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="e5d24-117">Remarks</span></span>

<span data-ttu-id="e5d24-118">Вы также можете установить тип точки подключения, выбрав средство **Connector,** выбрав фигуру, а затем щелкнув правой кнопкой мыши точку подключения.</span><span class="sxs-lookup"><span data-stu-id="e5d24-118">You can also set the connection point type by choosing the **Connector** tool, selecting a shape, and then right-clicking a connection point.</span></span> <span data-ttu-id="e5d24-119">Для этого необходимо запустить в режиме [разработчика.](run-in-developer-mode-display-the-developer-tab.md)</span><span class="sxs-lookup"><span data-stu-id="e5d24-119">To do this, you need to run in [developer](run-in-developer-mode-display-the-developer-tab.md) mode.</span></span> 
  
<span data-ttu-id="e5d24-120">Чтобы получить ссылку на ячейку Type /C по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e5d24-120">To get a reference to the Type / C cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e5d24-121">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e5d24-121">Cell name:</span></span>  <br/> |<span data-ttu-id="e5d24-122">Connections.Type[i] где *i* = <1>, 2, 3... </span><span class="sxs-lookup"><span data-stu-id="e5d24-122">Connections.Type[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e5d24-123">Чтобы получить ссылку на ячейку Type /C по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e5d24-123">To get a reference to the Type / C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e5d24-124">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e5d24-124">Section index:</span></span>  <br/> |<span data-ttu-id="e5d24-125">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="e5d24-125">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="e5d24-126">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e5d24-126">Row index:</span></span>  <br/> |<span data-ttu-id="e5d24-127">**visRowConnectionPts**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="e5d24-127">**visRowConnectionPts** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="e5d24-128">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e5d24-128">Cell index:</span></span>  <br/> |<span data-ttu-id="e5d24-129">**visCnnctType** (не расширенные строки) **visCnnctC** (расширенные строки)</span><span class="sxs-lookup"><span data-stu-id="e5d24-129">**visCnnctType** (non-extended rows) **visCnnctC** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="e5d24-130">Сведения о расширенных и расширенных строках см. в строке Точки подключения.</span><span class="sxs-lookup"><span data-stu-id="e5d24-130">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

