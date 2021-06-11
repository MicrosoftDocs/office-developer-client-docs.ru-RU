---
title: Отображение индикатора хода выполнения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7b0ce0ab75ffdce045ccde5bf6ea8a7da046f463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408029"
---
# <a name="display-a-progress-indicator"></a><span data-ttu-id="09823-103">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="09823-103">Display a progress indicator</span></span>
 
<span data-ttu-id="09823-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09823-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09823-105">Чтобы отобразить индикатор прогресса, позвоните [в IMAPIProgress::GetFlags,](imapiprogress-getflags.md) чтобы получить текущий параметр флагов.</span><span class="sxs-lookup"><span data-stu-id="09823-105">To display a progress indicator, call [IMAPIProgress::GetFlags](imapiprogress-getflags.md) to retrieve the current flags setting.</span></span> 
  
<span data-ttu-id="09823-106">Если установлен MAPI_TOP_LEVEL флаг, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="09823-106">If the MAPI_TOP_LEVEL flag is set, complete the following steps:</span></span>
  
1. <span data-ttu-id="09823-107">Установите переменную, равную общему количеству элементов для обработки в операции.</span><span class="sxs-lookup"><span data-stu-id="09823-107">Set a variable equal to the total number of items to process in the operation.</span></span> <span data-ttu-id="09823-108">Например, если вы копируете содержимое папки, это значение будет равно числу подмостков в папке и количеству сообщений.</span><span class="sxs-lookup"><span data-stu-id="09823-108">For example, if you are copying the contents of a folder, this value will be equal to the number of the subfolders in the folder plus the number of messages.</span></span> 
    
2. <span data-ttu-id="09823-109">Установите переменную, равную 1000, разделенную на количество элементов.</span><span class="sxs-lookup"><span data-stu-id="09823-109">Set a variable equal to 1000 divided by the number of items.</span></span> 
    
3. <span data-ttu-id="09823-110">Если вы показываете прогресс для подобектов, позвоните по методу [IMAPIProgress объекта progress::SetLimits](imapiprogress-setlimits.md) и передай следующие значения для трех параметров:</span><span class="sxs-lookup"><span data-stu-id="09823-110">If you are showing progress for subobjects, call the progress object's [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method and pass the following values for the three parameters:</span></span> 
    
   - <span data-ttu-id="09823-111">Установите  _параметр lpulMin_ до 0.</span><span class="sxs-lookup"><span data-stu-id="09823-111">Set the  _lpulMin_ parameter to 0.</span></span> 
    
   - <span data-ttu-id="09823-112">Установите  _параметр lpulMax_ до 1000.</span><span class="sxs-lookup"><span data-stu-id="09823-112">Set the  _lpulMax_ parameter to 1000.</span></span> 
    
   - <span data-ttu-id="09823-113">Установите  _параметр lpulFlags_ для MAPI_TOP_LEVEL.</span><span class="sxs-lookup"><span data-stu-id="09823-113">Set the  _lpulFlags_ parameter to MAPI_TOP_LEVEL.</span></span> 
    
4. <span data-ttu-id="09823-114">Чтобы каждый объект был обработан, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="09823-114">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="09823-115">**Вызывай IMAPIProgress::SetLimits и передай** следующие значения для трех параметров:</span><span class="sxs-lookup"><span data-stu-id="09823-115">Call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="09823-116">Установите  _параметр lpulMin к_ переменной, заданной на шаге 2, умноженной на текущий элемент минус 1.</span><span class="sxs-lookup"><span data-stu-id="09823-116">Set the  _lpulMin_ parameter to the variable set in step 2 multiplied by the current item minus 1.</span></span> 
      
     - <span data-ttu-id="09823-117">Установите  _параметр lpulMax к_ переменной, заданной на шаге 2, умноженной на текущий объект.</span><span class="sxs-lookup"><span data-stu-id="09823-117">Set the  _lpulMax_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="09823-118">Установите  _параметр lpulFlags до_ 0.</span><span class="sxs-lookup"><span data-stu-id="09823-118">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="09823-119">Выполните любую обработку, которая должна быть выполнена на этом объекте.</span><span class="sxs-lookup"><span data-stu-id="09823-119">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="09823-120">Если это подобект, и необходимо отобразить прогресс в подобектах, передай указатель объекту прогресса в  _параметре lpProgress_ методу.</span><span class="sxs-lookup"><span data-stu-id="09823-120">If this is a subobject and you want to display progress on subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="09823-121">[Вызывай IMAPIProgress::P и](imapiprogress-progress.md) передай следующие значения для трех параметров:</span><span class="sxs-lookup"><span data-stu-id="09823-121">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="09823-122">Установите  _параметр ulValue переменной,_ заданной на шаге 2, умноженной на текущий объект.</span><span class="sxs-lookup"><span data-stu-id="09823-122">Set the  _ulValue_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="09823-123">Установите  _параметр ulCount_ текущему объекту.</span><span class="sxs-lookup"><span data-stu-id="09823-123">Set the  _ulCount_ parameter to the current object.</span></span> 
      
     - <span data-ttu-id="09823-124">Установите  _параметр ulTotal к_ переменной, заданной на шаге 1, общему числу объектов.</span><span class="sxs-lookup"><span data-stu-id="09823-124">Set the  _ulTotal_ parameter to the variable set in step 1, the total number of objects.</span></span> 
    
<span data-ttu-id="09823-125">Если флаг MAPI_TOP_LEVEL не установлен, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="09823-125">If the MAPI_TOP_LEVEL flag is not set, complete the following steps:</span></span>
  
1. <span data-ttu-id="09823-126">Чтобы получить минимальное значение для отображения, позвоните по методу [IMAPIProgress::GetMin](imapiprogress-getmin.md) объекта прогресса.</span><span class="sxs-lookup"><span data-stu-id="09823-126">Call the progress object's [IMAPIProgress::GetMin](imapiprogress-getmin.md) method to retrieve the minimum value for the display.</span></span> 
    
2. <span data-ttu-id="09823-127">Вызов [IMAPIProgress::GetMax,](imapiprogress-getmax.md) чтобы получить максимальное значение для отображения.</span><span class="sxs-lookup"><span data-stu-id="09823-127">Call [IMAPIProgress::GetMax](imapiprogress-getmax.md) to retrieve the maximum value for the display.</span></span> 
    
3. <span data-ttu-id="09823-128">Установите переменную, равную общему количеству обрабатываемых объектов.</span><span class="sxs-lookup"><span data-stu-id="09823-128">Set a variable equal to the total number of objects to be processed.</span></span> 
    
4. <span data-ttu-id="09823-129">Установите переменную, равную результату вычитания минимального значения из максимального значения и деления на общее количество объектов.</span><span class="sxs-lookup"><span data-stu-id="09823-129">Set a variable equal to the result of subtracting the minimum value from the maximum value and then dividing by the total number of objects.</span></span>
    
5. <span data-ttu-id="09823-130">Чтобы каждый объект был обработан, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="09823-130">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="09823-131">Если поставщик показывает прогресс в подобектах, позвоните **в службу IMAPIProgress::SetLimits** и передайте следующие значения для трех параметров:</span><span class="sxs-lookup"><span data-stu-id="09823-131">If your provider is showing progress for subobjects, call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="09823-132">Установите  _параметр lpulMin к_ минимальному значению плюс текущий элемент минус 1, умноженный на переменную, заданную на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="09823-132">Set the  _lpulMin_ parameter to the minimum value plus the current item minus 1 multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="09823-133">Установите параметр  _lpulMax к_ минимальному значению плюс текущее устройство, умноженное на переменную, заданную в шаге 4.</span><span class="sxs-lookup"><span data-stu-id="09823-133">Set the  _lpulMax_ parameter to the minimum value plus the current unit multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="09823-134">Установите  _параметр lpulFlags до_ 0.</span><span class="sxs-lookup"><span data-stu-id="09823-134">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="09823-135">Выполните любую обработку, которая должна быть выполнена на этом объекте.</span><span class="sxs-lookup"><span data-stu-id="09823-135">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="09823-136">Если объект — это подобект, а поставщик отображает прогресс для подобектов, передайте указатель объекту progress в  _параметре lpProgress_ методу.</span><span class="sxs-lookup"><span data-stu-id="09823-136">If the object is a subobject, and your provider displays progress for subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="09823-137">[Вызывай IMAPIProgress::P и](imapiprogress-progress.md) передай следующие значения для трех параметров:</span><span class="sxs-lookup"><span data-stu-id="09823-137">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="09823-138">Установите  _параметр ulValue для_ переменной, заданной в шаге 2, умноженной на текущий объект.</span><span class="sxs-lookup"><span data-stu-id="09823-138">Set the  _ulValue_ parameter to variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="09823-139">Установите  _параметр ulCount_ до 0.</span><span class="sxs-lookup"><span data-stu-id="09823-139">Set the  _ulCount_ parameter to 0.</span></span> 
      
     - <span data-ttu-id="09823-140">Установите  _параметр ulTotal_ до 0.</span><span class="sxs-lookup"><span data-stu-id="09823-140">Set the  _ulTotal_ parameter to 0.</span></span> 
    
<span data-ttu-id="09823-141">В следующем примере кода иллюстрируется логика, необходимая для демонстрации прогресса на всех уровнях операции, копирующих содержимое папки, содержаной пять подвещений.</span><span class="sxs-lookup"><span data-stu-id="09823-141">The following code example illustrates the logic required to show progress at all levels of an operation that copies the contents of a folder that contains five subfolders.</span></span> 
  
```cpp
lpProgress->GetFlags (lpulFlags);
ulFlags = *lpulFlags;
/* The folder in charge of the display. It contains 5 subfolders. */
if (ulFlags & MAPI_TOP_LEVEL)
{
    ulItems = 5                         // 5 subfolders in this folder
    ulScale = (ulMax / ulItems)         // 200 because ulMax = 1000
    lpProgress->SetLimits(0, ulMax, MAPI_TOP_LEVEL)
    for (i = 1; i <= ulItems; i++)      // for each subfolder to copy
    {
        lpProgress->SetLimits( (i - 1) * ulScale, i * ulScale, 0)
        CopyOneFolder(lpFolder(i), lpProgress)
        lpProgress->Progress( i * ulScale, i, ulItems)
    }
}
else
/* One of the subfolders to be copied. It contains 3 messages. */
{
    lpProgress->GetMin(&ulMin);
    lpProgress->GetMax(&ulMax);
    ulItems = 3;
    ulDelta = (ulMax - ulMin) / ulItems;
    for (i = 1; i <= ulItems; i++)
    {
        lpProgress->SetLimits(ulMin + (i - 1) * ulDelta,
                              ulMin + i * ulDelta, 0)
        CopyOneFolder(lpFolder(i), lpProgress)
        /* Pass 0 for ulCount and ulTotal because this is not the */
        /* top-level display, and that information is unavailable  */
        lpProgress->Progress( i * ulDelta, 0, 0)
    }
}
 
```

## <a name="see-also"></a><span data-ttu-id="09823-142">См. также</span><span class="sxs-lookup"><span data-stu-id="09823-142">See also</span></span>

- [<span data-ttu-id="09823-143">Индикаторы прогресса MAPI</span><span class="sxs-lookup"><span data-stu-id="09823-143">MAPI Progress Indicators</span></span>](mapi-progress-indicators.md)

