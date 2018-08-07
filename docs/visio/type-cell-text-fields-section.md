---
title: Ячейка Type (раздел "Текстовые поля")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1060
localization_priority: Normal
ms.assetid: 69d64520-9a47-07ca-09c7-d1e5da620348
description: Указывает тип данных для значения поля текст.
ms.openlocfilehash: 68bfa8a84adb0d46d9621e6fc5383f4b6606f542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815082"
---
# <a name="type-cell-text-fields-section"></a><span data-ttu-id="c26a9-103">Ячейка Type (раздел "Текстовые поля")</span><span class="sxs-lookup"><span data-stu-id="c26a9-103">Type Cell (Text Fields Section)</span></span>

<span data-ttu-id="c26a9-104">Указывает тип данных для значения поля текст.</span><span class="sxs-lookup"><span data-stu-id="c26a9-104">Specifies a data type for the text field value.</span></span>
  
|<span data-ttu-id="c26a9-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c26a9-105">**Value**</span></span>|<span data-ttu-id="c26a9-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c26a9-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c26a9-107">0</span><span class="sxs-lookup"><span data-stu-id="c26a9-107">0</span></span>  <br/> |<span data-ttu-id="c26a9-108">Строка.</span><span class="sxs-lookup"><span data-stu-id="c26a9-108">String.</span></span>  <br/> |
|<span data-ttu-id="c26a9-109">2</span><span class="sxs-lookup"><span data-stu-id="c26a9-109">2</span></span>  <br/> |<span data-ttu-id="c26a9-110">Номер.</span><span class="sxs-lookup"><span data-stu-id="c26a9-110">Number.</span></span> <span data-ttu-id="c26a9-111">Включает в себя дату, значения времени, продолжительность и валюты, а также скаляры, измерений и углы.</span><span class="sxs-lookup"><span data-stu-id="c26a9-111">Includes date, time, duration, and currency values as well as scalars, dimensions, and angles.</span></span> <span data-ttu-id="c26a9-112">Укажите изображение формата в формат ячейки.</span><span class="sxs-lookup"><span data-stu-id="c26a9-112">Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="c26a9-113">5</span><span class="sxs-lookup"><span data-stu-id="c26a9-113">5</span></span>  <br/> |<span data-ttu-id="c26a9-114">Значение даты или времени.</span><span class="sxs-lookup"><span data-stu-id="c26a9-114">Date or time value.</span></span> <span data-ttu-id="c26a9-115">Отображение дней, месяцев и лет или секунд, минут и часов, или объединены значения даты и времени.</span><span class="sxs-lookup"><span data-stu-id="c26a9-115">Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value.</span></span> <span data-ttu-id="c26a9-116">Укажите изображение формата в формат ячейки.</span><span class="sxs-lookup"><span data-stu-id="c26a9-116">Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="c26a9-117">6</span><span class="sxs-lookup"><span data-stu-id="c26a9-117">6</span></span>  <br/> |<span data-ttu-id="c26a9-118">Значения длительности.</span><span class="sxs-lookup"><span data-stu-id="c26a9-118">Duration value.</span></span> <span data-ttu-id="c26a9-119">Отображение времени, затраченного.</span><span class="sxs-lookup"><span data-stu-id="c26a9-119">Displays elapsed time.</span></span> <span data-ttu-id="c26a9-120">Укажите изображение формата в формат ячейки.</span><span class="sxs-lookup"><span data-stu-id="c26a9-120">Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="c26a9-121">7</span><span class="sxs-lookup"><span data-stu-id="c26a9-121">7</span></span>  <br/> |<span data-ttu-id="c26a9-122">Значение типа currency.</span><span class="sxs-lookup"><span data-stu-id="c26a9-122">Currency value.</span></span> <span data-ttu-id="c26a9-123">Использует текущих региональных параметров компьютера.</span><span class="sxs-lookup"><span data-stu-id="c26a9-123">Uses the system's current Regional Settings.</span></span> <span data-ttu-id="c26a9-124">Укажите изображение формата в формат ячейки.</span><span class="sxs-lookup"><span data-stu-id="c26a9-124">Specify a format picture in the Format cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c26a9-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="c26a9-125">Remarks</span></span>

<span data-ttu-id="c26a9-126">Также можно задать значение ячейки с помощью диалогового окна **поля** (фигуры, выбранной на вкладке **Вставка** в группе **текст** щелкните **поле** ).</span><span class="sxs-lookup"><span data-stu-id="c26a9-126">You can also set the value of this cell using the **Field** dialog box (with a shape selected, on the **Insert** tab, in the **Text** group, click **Field** ).</span></span> 
  
<span data-ttu-id="c26a9-127">Чтобы получить ссылку на ячейку тип по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="c26a9-127">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c26a9-128">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="c26a9-128">Cell name:</span></span>  <br/> |<span data-ttu-id="c26a9-129">Fields.Type [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c26a9-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c26a9-130">Для получения ссылки на ячейки типа по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="c26a9-130">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c26a9-131">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c26a9-131">Section index:</span></span>  <br/> |<span data-ttu-id="c26a9-132">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="c26a9-132">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="c26a9-133">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c26a9-133">Row index:</span></span>  <br/> |<span data-ttu-id="c26a9-134">**visRowField** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c26a9-134">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="c26a9-135">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c26a9-135">Cell index:</span></span>  <br/> |<span data-ttu-id="c26a9-136">**visFieldType**</span><span class="sxs-lookup"><span data-stu-id="c26a9-136">**visFieldType**</span></span> <br/> |
   

