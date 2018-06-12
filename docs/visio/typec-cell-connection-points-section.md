---
title: Тип / ячейка C (раздел указывает подключение)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
localization_priority: Normal
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: Определяет тип точки подключения.
ms.openlocfilehash: 12c953a160ab99aad007e9b2bb9089d651aee553
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815085"
---
# <a name="type--c-cell-connection-points-section"></a><span data-ttu-id="05f9a-103">Тип / ячейка C (раздел указывает подключение)</span><span class="sxs-lookup"><span data-stu-id="05f9a-103">Type / C Cell (Connection Points Section)</span></span>

<span data-ttu-id="05f9a-104">Определяет тип точки подключения.</span><span class="sxs-lookup"><span data-stu-id="05f9a-104">Determines the connection point type.</span></span>
  
|<span data-ttu-id="05f9a-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="05f9a-105">**Value**</span></span>|<span data-ttu-id="05f9a-106">**Тип**</span><span class="sxs-lookup"><span data-stu-id="05f9a-106">**Type**</span></span>|<span data-ttu-id="05f9a-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="05f9a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="05f9a-108">0</span><span class="sxs-lookup"><span data-stu-id="05f9a-108">0</span></span>  <br/> |<span data-ttu-id="05f9a-109">Рисунка</span><span class="sxs-lookup"><span data-stu-id="05f9a-109">Inward</span></span>  <br/> |<span data-ttu-id="05f9a-110">**visCnnctTypeInward**</span><span class="sxs-lookup"><span data-stu-id="05f9a-110">**visCnnctTypeInward**</span></span> <br/> |
|<span data-ttu-id="05f9a-111">1</span><span class="sxs-lookup"><span data-stu-id="05f9a-111">1</span></span>  <br/> |<span data-ttu-id="05f9a-112">Наружу</span><span class="sxs-lookup"><span data-stu-id="05f9a-112">Outward</span></span>  <br/> |<span data-ttu-id="05f9a-113">**visCnnctTypeOutward**</span><span class="sxs-lookup"><span data-stu-id="05f9a-113">**visCnnctTypeOutward**</span></span> <br/> |
|<span data-ttu-id="05f9a-114">2</span><span class="sxs-lookup"><span data-stu-id="05f9a-114">2</span></span>  <br/> |<span data-ttu-id="05f9a-115">Внутрь &amp; наружу</span><span class="sxs-lookup"><span data-stu-id="05f9a-115">Inward &amp; Outward</span></span>  <br/> |<span data-ttu-id="05f9a-116">**visCnnctTypeInwardOutward**</span><span class="sxs-lookup"><span data-stu-id="05f9a-116">**visCnnctTypeInwardOutward**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05f9a-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="05f9a-117">Remarks</span></span>

<span data-ttu-id="05f9a-118">Также можно задать тип точки подключения, Выбор средства **соединителя** , выбрав фигуры и затем щелкните правой кнопкой мыши точку подключения.</span><span class="sxs-lookup"><span data-stu-id="05f9a-118">You can also set the connection point type by choosing the **Connector** tool, selecting a shape, and then right-clicking a connection point.</span></span> <span data-ttu-id="05f9a-119">Для этого необходимо запустить в режиме [разработчика](run-in-developer-mode-display-the-developer-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="05f9a-119">To do this, you need to run in [developer](run-in-developer-mode-display-the-developer-tab.md) mode.</span></span> 
  
<span data-ttu-id="05f9a-120">Для получения ссылки на тип / C ячейка по имени из другой формулы или из файла с помощью свойства **CellsU** использования:</span><span class="sxs-lookup"><span data-stu-id="05f9a-120">To get a reference to the Type / C cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05f9a-121">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="05f9a-121">Cell name:</span></span>  <br/> |<span data-ttu-id="05f9a-122">Connections.Type [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="05f9a-122">Connections.Type[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="05f9a-123">Для получения ссылки на тип / C ячейки по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="05f9a-123">To get a reference to the Type / C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05f9a-124">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="05f9a-124">Section index:</span></span>  <br/> |<span data-ttu-id="05f9a-125">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="05f9a-125">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="05f9a-126">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="05f9a-126">Row index:</span></span>  <br/> |<span data-ttu-id="05f9a-127">**visRowConnectionPts** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="05f9a-127">**visRowConnectionPts** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="05f9a-128">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="05f9a-128">Cell index:</span></span>  <br/> |<span data-ttu-id="05f9a-129">**visCnnctType** (не только строк) **visCnnctC** (расширенные строк)</span><span class="sxs-lookup"><span data-stu-id="05f9a-129">**visCnnctType** (non-extended rows) **visCnnctC** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="05f9a-130">Сведения о не расширены и расширенного строк, в разделе точек подключения строки.</span><span class="sxs-lookup"><span data-stu-id="05f9a-130">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

