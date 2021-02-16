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
description: Указывает тип данных для значения текстового поля.
ms.openlocfilehash: 91a2d60133d9a39e152656558f168742a5409883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407986"
---
# <a name="type-cell-text-fields-section"></a><span data-ttu-id="32f30-103">Type Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="32f30-103">Type Cell (Text Fields Section)</span></span>

<span data-ttu-id="32f30-104">Указывает тип данных для значения текстового поля.</span><span class="sxs-lookup"><span data-stu-id="32f30-104">Specifies a data type for the text field value.</span></span>
  
|<span data-ttu-id="32f30-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="32f30-105">**Value**</span></span>|<span data-ttu-id="32f30-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="32f30-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32f30-107">0</span><span class="sxs-lookup"><span data-stu-id="32f30-107">0</span></span>  <br/> |<span data-ttu-id="32f30-108">Строка.</span><span class="sxs-lookup"><span data-stu-id="32f30-108">String.</span></span>  <br/> |
|<span data-ttu-id="32f30-109">2 </span><span class="sxs-lookup"><span data-stu-id="32f30-109">2</span></span>  <br/> |<span data-ttu-id="32f30-110">Номер.</span><span class="sxs-lookup"><span data-stu-id="32f30-110">Number.</span></span> <span data-ttu-id="32f30-111">Включает значения даты, времени, длительности и валюты, а также скаляры, измерения и углы.</span><span class="sxs-lookup"><span data-stu-id="32f30-111">Includes date, time, duration, and currency values as well as scalars, dimensions, and angles.</span></span> <span data-ttu-id="32f30-112">Укажите формат изображения в ячейке Format.</span><span class="sxs-lookup"><span data-stu-id="32f30-112">Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="32f30-113">5 </span><span class="sxs-lookup"><span data-stu-id="32f30-113">5</span></span>  <br/> |<span data-ttu-id="32f30-114">Значение даты или времени.</span><span class="sxs-lookup"><span data-stu-id="32f30-114">Date or time value.</span></span> <span data-ttu-id="32f30-115">Отображает дни, месяцы и годы, секунды, минуты и часы или объединенную дату и время.</span><span class="sxs-lookup"><span data-stu-id="32f30-115">Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value.</span></span> <span data-ttu-id="32f30-116">Укажите формат изображения в ячейке Format.</span><span class="sxs-lookup"><span data-stu-id="32f30-116">Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="32f30-117">6 </span><span class="sxs-lookup"><span data-stu-id="32f30-117">6</span></span>  <br/> |<span data-ttu-id="32f30-118">Значение длительности.</span><span class="sxs-lookup"><span data-stu-id="32f30-118">Duration value.</span></span> <span data-ttu-id="32f30-119">Отображает время, за который у вас есть время.</span><span class="sxs-lookup"><span data-stu-id="32f30-119">Displays elapsed time.</span></span> <span data-ttu-id="32f30-120">Укажите формат изображения в ячейке Format.</span><span class="sxs-lookup"><span data-stu-id="32f30-120">Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="32f30-121">7 </span><span class="sxs-lookup"><span data-stu-id="32f30-121">7</span></span>  <br/> |<span data-ttu-id="32f30-122">Значение валюты.</span><span class="sxs-lookup"><span data-stu-id="32f30-122">Currency value.</span></span> <span data-ttu-id="32f30-123">Использует текущие региональные параметры системы.</span><span class="sxs-lookup"><span data-stu-id="32f30-123">Uses the system's current Regional Settings.</span></span> <span data-ttu-id="32f30-124">Укажите формат изображения в ячейке Format.</span><span class="sxs-lookup"><span data-stu-id="32f30-124">Specify a format picture in the Format cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32f30-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="32f30-125">Remarks</span></span>

<span data-ttu-id="32f30-126">Вы также можете установить значение этой ячейки с помощью диалогового окна  **"Поле"** (с выбранной фигурой на вкладке "Вставка" в группе "Текст" щелкните  **"Поле").**</span><span class="sxs-lookup"><span data-stu-id="32f30-126">You can also set the value of this cell using the **Field** dialog box (with a shape selected, on the **Insert** tab, in the **Text** group, click **Field** ).</span></span> 
  
<span data-ttu-id="32f30-127">Чтобы получить ссылку на ячейку Type по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="32f30-127">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="32f30-128">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="32f30-128">Cell name:</span></span>  <br/> |<span data-ttu-id="32f30-129">Fields.Type[ *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="32f30-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="32f30-130">Чтобы получить ссылку на ячейку Type по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="32f30-130">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="32f30-131">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="32f30-131">Section index:</span></span>  <br/> |<span data-ttu-id="32f30-132">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="32f30-132">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="32f30-133">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="32f30-133">Row index:</span></span>  <br/> |<span data-ttu-id="32f30-134">**visRowField**  +   *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="32f30-134">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="32f30-135">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="32f30-135">Cell index:</span></span>  <br/> |<span data-ttu-id="32f30-136">**visFieldType**</span><span class="sxs-lookup"><span data-stu-id="32f30-136">**visFieldType**</span></span> <br/> |
   

