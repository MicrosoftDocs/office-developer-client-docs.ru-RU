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
# <a name="type-cell-text-fields-section"></a><span data-ttu-id="0cfe5-103">Type Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="0cfe5-103">Type Cell (Text Fields Section)</span></span>

<span data-ttu-id="0cfe5-104">Указывает тип данных для значения текстового поля.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-104">Specifies a data type for the text field value.</span></span>
  
|<span data-ttu-id="0cfe5-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="0cfe5-105">**Value**</span></span>|<span data-ttu-id="0cfe5-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0cfe5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0cfe5-107">0</span><span class="sxs-lookup"><span data-stu-id="0cfe5-107">0</span></span>  <br/> |<span data-ttu-id="0cfe5-108">Строка.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-108">String.</span></span>  <br/> |
|<span data-ttu-id="0cfe5-109">2</span><span class="sxs-lookup"><span data-stu-id="0cfe5-109">2</span></span>  <br/> |<span data-ttu-id="0cfe5-110">Номер.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-110">Number.</span></span> <span data-ttu-id="0cfe5-111">Включает значения даты, времени, продолжительности и валюты, а также масштабы, размеры и углы.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-111">Includes date, time, duration, and currency values as well as scalars, dimensions, and angles.</span></span> <span data-ttu-id="0cfe5-112">Укажите изображение формата в ячейке Format.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-112">Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="0cfe5-113">5 </span><span class="sxs-lookup"><span data-stu-id="0cfe5-113">5</span></span>  <br/> |<span data-ttu-id="0cfe5-114">Значение даты или времени.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-114">Date or time value.</span></span> <span data-ttu-id="0cfe5-115">Отображает дни, месяцы и годы или секунды, минуты и часы или совокупное значение даты и времени.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-115">Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value.</span></span> <span data-ttu-id="0cfe5-116">Укажите изображение формата в ячейке Format.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-116">Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="0cfe5-117">6 </span><span class="sxs-lookup"><span data-stu-id="0cfe5-117">6</span></span>  <br/> |<span data-ttu-id="0cfe5-118">Значение продолжительности.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-118">Duration value.</span></span> <span data-ttu-id="0cfe5-119">Отображает по и сего времени.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-119">Displays elapsed time.</span></span> <span data-ttu-id="0cfe5-120">Укажите изображение формата в ячейке Format.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-120">Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="0cfe5-121">7 </span><span class="sxs-lookup"><span data-stu-id="0cfe5-121">7</span></span>  <br/> |<span data-ttu-id="0cfe5-122">Значение валюты.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-122">Currency value.</span></span> <span data-ttu-id="0cfe5-123">Использует текущую региональную Параметры.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-123">Uses the system's current Regional Settings.</span></span> <span data-ttu-id="0cfe5-124">Укажите изображение формата в ячейке Format.</span><span class="sxs-lookup"><span data-stu-id="0cfe5-124">Specify a format picture in the Format cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cfe5-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="0cfe5-125">Remarks</span></span>

<span data-ttu-id="0cfe5-126">Вы также можете установить значение этой ячейки с помощью диалогового окна **Field** (с выбранной фигурой на вкладке **Вставить** в группу **Текст** щелкните **Поле).**</span><span class="sxs-lookup"><span data-stu-id="0cfe5-126">You can also set the value of this cell using the **Field** dialog box (with a shape selected, on the **Insert** tab, in the **Text** group, click **Field** ).</span></span> 
  
<span data-ttu-id="0cfe5-127">Чтобы получить ссылку на ячейку Type по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="0cfe5-127">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0cfe5-128">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0cfe5-128">Cell name:</span></span>  <br/> |<span data-ttu-id="0cfe5-129">Fields.Type[i], где *i* = <1>, 2, 3... </span><span class="sxs-lookup"><span data-stu-id="0cfe5-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0cfe5-130">Чтобы получить ссылку на ячейку Type по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0cfe5-130">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0cfe5-131">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0cfe5-131">Section index:</span></span>  <br/> |<span data-ttu-id="0cfe5-132">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="0cfe5-132">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="0cfe5-133">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0cfe5-133">Row index:</span></span>  <br/> |<span data-ttu-id="0cfe5-134">**visRowField**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="0cfe5-134">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="0cfe5-135">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0cfe5-135">Cell index:</span></span>  <br/> |<span data-ttu-id="0cfe5-136">**visFieldType**</span><span class="sxs-lookup"><span data-stu-id="0cfe5-136">**visFieldType**</span></span> <br/> |
   

