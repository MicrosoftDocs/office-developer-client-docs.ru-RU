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
# <a name="type--c-cell-connection-points-section"></a><span data-ttu-id="eb769-103">Type / C Cell (Connection Points Section)</span><span class="sxs-lookup"><span data-stu-id="eb769-103">Type / C Cell (Connection Points Section)</span></span>

<span data-ttu-id="eb769-104">Определяет тип точки подключения.</span><span class="sxs-lookup"><span data-stu-id="eb769-104">Determines the connection point type.</span></span>
  
|<span data-ttu-id="eb769-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="eb769-105">**Value**</span></span>|<span data-ttu-id="eb769-106">**Тип**</span><span class="sxs-lookup"><span data-stu-id="eb769-106">**Type**</span></span>|<span data-ttu-id="eb769-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="eb769-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eb769-108">нуль</span><span class="sxs-lookup"><span data-stu-id="eb769-108">0</span></span>  <br/> |<span data-ttu-id="eb769-109">Входящего</span><span class="sxs-lookup"><span data-stu-id="eb769-109">Inward</span></span>  <br/> |<span data-ttu-id="eb769-110">**Вискннкттипеинвард**</span><span class="sxs-lookup"><span data-stu-id="eb769-110">**visCnnctTypeInward**</span></span> <br/> |
|<span data-ttu-id="eb769-111">1,1</span><span class="sxs-lookup"><span data-stu-id="eb769-111">1</span></span>  <br/> |<span data-ttu-id="eb769-112">Наруж</span><span class="sxs-lookup"><span data-stu-id="eb769-112">Outward</span></span>  <br/> |<span data-ttu-id="eb769-113">**Вискннкттипеаутвард**</span><span class="sxs-lookup"><span data-stu-id="eb769-113">**visCnnctTypeOutward**</span></span> <br/> |
|<span data-ttu-id="eb769-114">2</span><span class="sxs-lookup"><span data-stu-id="eb769-114">2</span></span>  <br/> |<span data-ttu-id="eb769-115">&amp; Внешнее</span><span class="sxs-lookup"><span data-stu-id="eb769-115">Inward &amp; Outward</span></span>  <br/> |<span data-ttu-id="eb769-116">**Вискннкттипеинвардаутвард**</span><span class="sxs-lookup"><span data-stu-id="eb769-116">**visCnnctTypeInwardOutward**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb769-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="eb769-117">Remarks</span></span>

<span data-ttu-id="eb769-118">Кроме того, можно задать тип точки подключения, выбрав инструмент **соединитель** , выбрав фигуру и щелкнув правой кнопкой мыши точку подключения.</span><span class="sxs-lookup"><span data-stu-id="eb769-118">You can also set the connection point type by choosing the **Connector** tool, selecting a shape, and then right-clicking a connection point.</span></span> <span data-ttu-id="eb769-119">Для этого необходимо запустить в режиме [разработчика](run-in-developer-mode-display-the-developer-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="eb769-119">To do this, you need to run in [developer](run-in-developer-mode-display-the-developer-tab.md) mode.</span></span> 
  
<span data-ttu-id="eb769-120">Чтобы получить ссылку на ячейку Type/C по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="eb769-120">To get a reference to the Type / C cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb769-121">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="eb769-121">Cell name:</span></span>  <br/> |<span data-ttu-id="eb769-122">Connections. Type [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="eb769-122">Connections.Type[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="eb769-123">Чтобы получить ссылку на ячейку Type/C по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="eb769-123">To get a reference to the Type / C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb769-124">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="eb769-124">Section index:</span></span>  <br/> |<span data-ttu-id="eb769-125">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="eb769-125">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="eb769-126">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="eb769-126">Row index:</span></span>  <br/> |<span data-ttu-id="eb769-127">**висровконнектионптс** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="eb769-127">**visRowConnectionPts** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="eb769-128">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="eb769-128">Cell index:</span></span>  <br/> |<span data-ttu-id="eb769-129">**вискннкттипе** (нерасширенные строки) **вискннктк** (расширенные строки)</span><span class="sxs-lookup"><span data-stu-id="eb769-129">**visCnnctType** (non-extended rows) **visCnnctC** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="eb769-130">Сведения о нерасширенных и расширенных строках можно найти в статье точки подключения.</span><span class="sxs-lookup"><span data-stu-id="eb769-130">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

