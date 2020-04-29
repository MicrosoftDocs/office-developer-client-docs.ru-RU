---
title: Type Cell (Text Fields Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1060
localization_priority: Normal
ms.assetid: 69d64520-9a47-07ca-09c7-d1e5da620348
description: Задает тип данных для значения текстового поля.
ms.openlocfilehash: 91a2d60133d9a39e152656558f168742a5409883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407986"
---
# <a name="type-cell-text-fields-section"></a><span data-ttu-id="8ee18-103">Type Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="8ee18-103">Type Cell (Text Fields Section)</span></span>

<span data-ttu-id="8ee18-104">Задает тип данных для значения текстового поля.</span><span class="sxs-lookup"><span data-stu-id="8ee18-104">Specifies a data type for the text field value.</span></span>
  
|<span data-ttu-id="8ee18-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8ee18-105">**Value**</span></span>|<span data-ttu-id="8ee18-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8ee18-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8ee18-107">нуль</span><span class="sxs-lookup"><span data-stu-id="8ee18-107">0</span></span>  <br/> |<span data-ttu-id="8ee18-108">Строка.</span><span class="sxs-lookup"><span data-stu-id="8ee18-108">String.</span></span>  <br/> |
|<span data-ttu-id="8ee18-109">2</span><span class="sxs-lookup"><span data-stu-id="8ee18-109">2</span></span>  <br/> |<span data-ttu-id="8ee18-110">Значение.</span><span class="sxs-lookup"><span data-stu-id="8ee18-110">Number.</span></span> <span data-ttu-id="8ee18-111">Включает в себя даты, время, продолжительность и денежные значения, а также скаляры, измерения и углы.</span><span class="sxs-lookup"><span data-stu-id="8ee18-111">Includes date, time, duration, and currency values as well as scalars, dimensions, and angles.</span></span> <span data-ttu-id="8ee18-112">Укажите формат рисунка в ячейке Format (формат).</span><span class="sxs-lookup"><span data-stu-id="8ee18-112">Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="8ee18-113">5 </span><span class="sxs-lookup"><span data-stu-id="8ee18-113">5</span></span>  <br/> |<span data-ttu-id="8ee18-114">Значение даты или времени.</span><span class="sxs-lookup"><span data-stu-id="8ee18-114">Date or time value.</span></span> <span data-ttu-id="8ee18-115">Отображает дни, месяцы и годы, а также секунды, минуты и часы, а также объединенное значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="8ee18-115">Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value.</span></span> <span data-ttu-id="8ee18-116">Укажите формат рисунка в ячейке Format (формат).</span><span class="sxs-lookup"><span data-stu-id="8ee18-116">Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="8ee18-117">6 </span><span class="sxs-lookup"><span data-stu-id="8ee18-117">6</span></span>  <br/> |<span data-ttu-id="8ee18-118">Значение длительности.</span><span class="sxs-lookup"><span data-stu-id="8ee18-118">Duration value.</span></span> <span data-ttu-id="8ee18-119">Отображает затраченное время.</span><span class="sxs-lookup"><span data-stu-id="8ee18-119">Displays elapsed time.</span></span> <span data-ttu-id="8ee18-120">Укажите формат рисунка в ячейке Format (формат).</span><span class="sxs-lookup"><span data-stu-id="8ee18-120">Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="8ee18-121">7 </span><span class="sxs-lookup"><span data-stu-id="8ee18-121">7</span></span>  <br/> |<span data-ttu-id="8ee18-122">Денежное значение.</span><span class="sxs-lookup"><span data-stu-id="8ee18-122">Currency value.</span></span> <span data-ttu-id="8ee18-123">Использует текущие региональные параметры системы.</span><span class="sxs-lookup"><span data-stu-id="8ee18-123">Uses the system's current Regional Settings.</span></span> <span data-ttu-id="8ee18-124">Укажите формат рисунка в ячейке Format (формат).</span><span class="sxs-lookup"><span data-stu-id="8ee18-124">Specify a format picture in the Format cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ee18-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ee18-125">Remarks</span></span>

<span data-ttu-id="8ee18-126">Значение этой ячейки также можно задать с помощью диалогового окна " **поле** " (с выбранной фигурой на вкладке **Вставка** , в группе **текст** , щелкните **поле** ).</span><span class="sxs-lookup"><span data-stu-id="8ee18-126">You can also set the value of this cell using the **Field** dialog box (with a shape selected, on the **Insert** tab, in the **Text** group, click **Field** ).</span></span> 
  
<span data-ttu-id="8ee18-127">Чтобы получить ссылку на ячейку Type по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="8ee18-127">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ee18-128">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="8ee18-128">Cell name:</span></span>  <br/> |<span data-ttu-id="8ee18-129">Fields. Type [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8ee18-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8ee18-130">Чтобы получить ссылку на ячейку Type по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="8ee18-130">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ee18-131">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8ee18-131">Section index:</span></span>  <br/> |<span data-ttu-id="8ee18-132">**виссектионтекстфиелд**</span><span class="sxs-lookup"><span data-stu-id="8ee18-132">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="8ee18-133">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8ee18-133">Row index:</span></span>  <br/> |<span data-ttu-id="8ee18-134">**висровфиелд** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8ee18-134">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="8ee18-135">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8ee18-135">Cell index:</span></span>  <br/> |<span data-ttu-id="8ee18-136">**висфиелдтипе**</span><span class="sxs-lookup"><span data-stu-id="8ee18-136">**visFieldType**</span></span> <br/> |
   

