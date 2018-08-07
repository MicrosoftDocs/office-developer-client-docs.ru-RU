---
title: Отобразить индикатор выполнения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3c4c553a000dab233eb208c1222cc427c97b1e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808605"
---
# <a name="display-a-progress-indicator"></a><span data-ttu-id="ddb2b-103">Отобразить индикатор выполнения</span><span class="sxs-lookup"><span data-stu-id="ddb2b-103">Display a progress indicator</span></span>
 
<span data-ttu-id="ddb2b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ddb2b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ddb2b-105">Чтобы отобразить индикатор выполнения, вызовите [IMAPIProgress::GetFlags](imapiprogress-getflags.md) для получения текущего флаги параметру.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-105">To display a progress indicator, call [IMAPIProgress::GetFlags](imapiprogress-getflags.md) to retrieve the current flags setting.</span></span> 
  
<span data-ttu-id="ddb2b-106">Если значение флага MAPI_TOP_LEVEL, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ddb2b-106">If the MAPI_TOP_LEVEL flag is set, complete the following steps:</span></span>
  
1. <span data-ttu-id="ddb2b-107">Значение переменной равно общее число элементов для обработки в операции.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-107">Set a variable equal to the total number of items to process in the operation.</span></span> <span data-ttu-id="ddb2b-108">Например при копировании содержимого папки это значение будет равно количество вложенных папок в папке, а также количество сообщений.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-108">For example, if you are copying the contents of a folder, this value will be equal to the number of the subfolders in the folder plus the number of messages.</span></span> 
    
2. <span data-ttu-id="ddb2b-109">Значение переменной равно 1000, разделенная на число элементов.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-109">Set a variable equal to 1000 divided by the number of items.</span></span> 
    
3. <span data-ttu-id="ddb2b-110">Если отображается ход выполнения для вложенных объектов, вызовите метод [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) объекта о ходе выполнения и передает следующие значения для трех параметров:</span><span class="sxs-lookup"><span data-stu-id="ddb2b-110">If you are showing progress for subobjects, call the progress object's [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method and pass the following values for the three parameters:</span></span> 
    
   - <span data-ttu-id="ddb2b-111">Установите для параметра _lpulMin_ значение 0.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-111">Set the  _lpulMin_ parameter to 0.</span></span> 
    
   - <span data-ttu-id="ddb2b-112">Установите для параметра _lpulMax_ до 1000.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-112">Set the  _lpulMax_ parameter to 1000.</span></span> 
    
   - <span data-ttu-id="ddb2b-113">Установите для параметра _lpulFlags_ значение MAPI_TOP_LEVEL.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-113">Set the  _lpulFlags_ parameter to MAPI_TOP_LEVEL.</span></span> 
    
4. <span data-ttu-id="ddb2b-114">Для каждого объекта обработки выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ddb2b-114">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="ddb2b-115">Вызвать **IMAPIProgress::SetLimits** и передать следующие значения для трех параметров:</span><span class="sxs-lookup"><span data-stu-id="ddb2b-115">Call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="ddb2b-116">Установите для параметра _lpulMin_ в переменную, установленную на шаге 2, умноженное на текущем элементе минус 1.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-116">Set the  _lpulMin_ parameter to the variable set in step 2 multiplied by the current item minus 1.</span></span> 
      
     - <span data-ttu-id="ddb2b-117">Установите для параметра _lpulMax_ в переменную, установленную на шаге 2, умноженное на текущий объект.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-117">Set the  _lpulMax_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="ddb2b-118">Установите для параметра _lpulFlags_ значение 0.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-118">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="ddb2b-119">Выполните необходимые обработки должно выполняться на этот объект.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-119">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="ddb2b-120">Если это вложенные объекты и для отображения хода выполнения на вложенных объектов, передайте указатель на объект о ходе выполнения с помощью параметра _lpProgress_ методу.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-120">If this is a subobject and you want to display progress on subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="ddb2b-121">Вызвать [IMAPIProgress::Progress](imapiprogress-progress.md) и передать следующие значения для трех параметров:</span><span class="sxs-lookup"><span data-stu-id="ddb2b-121">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="ddb2b-122">Установите для параметра _ulValue_ в переменную, установленную на шаге 2, умноженное на текущий объект.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-122">Set the  _ulValue_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="ddb2b-123">Установите для параметра _инициализирует метод ulCount_ для текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-123">Set the  _ulCount_ parameter to the current object.</span></span> 
      
     - <span data-ttu-id="ddb2b-124">Установите для параметра _ulTotal_ в переменную, установленную на шаге 1, общее число объектов.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-124">Set the  _ulTotal_ parameter to the variable set in step 1, the total number of objects.</span></span> 
    
<span data-ttu-id="ddb2b-125">Если флаг MAPI_TOP_LEVEL не установлен, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-125">If the MAPI_TOP_LEVEL flag is not set, complete the following steps:</span></span>
  
1. <span data-ttu-id="ddb2b-126">Вызов метода [IMAPIProgress::GetMin](imapiprogress-getmin.md) о ходе выполнения объектов для извлечения минимальное значение для отображения.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-126">Call the progress object's [IMAPIProgress::GetMin](imapiprogress-getmin.md) method to retrieve the minimum value for the display.</span></span> 
    
2. <span data-ttu-id="ddb2b-127">Вызов [IMAPIProgress::GetMax](imapiprogress-getmax.md) для получения максимального значения для отображения.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-127">Call [IMAPIProgress::GetMax](imapiprogress-getmax.md) to retrieve the maximum value for the display.</span></span> 
    
3. <span data-ttu-id="ddb2b-128">Значение переменной равно общее число объектов для обработки.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-128">Set a variable equal to the total number of objects to be processed.</span></span> 
    
4. <span data-ttu-id="ddb2b-129">Значение переменной равно результат вычитания минимальное значение из максимальное значение и затем разделив общее число объектов.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-129">Set a variable equal to the result of subtracting the minimum value from the maximum value and then dividing by the total number of objects.</span></span>
    
5. <span data-ttu-id="ddb2b-130">Для каждого объекта обработки выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ddb2b-130">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="ddb2b-131">Если ваш поставщик, на котором отображается ход выполнения для вложенных объектов, вызвать **IMAPIProgress::SetLimits** и передать следующие значения для трех параметров:</span><span class="sxs-lookup"><span data-stu-id="ddb2b-131">If your provider is showing progress for subobjects, call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="ddb2b-132">Установите для параметра _lpulMin_ минимальное значение, а также текущего элемента минус 1, умноженное на переменную, установленную на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-132">Set the  _lpulMin_ parameter to the minimum value plus the current item minus 1 multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="ddb2b-133">Установите для параметра _lpulMax_ минимальное значение, а также текущего подразделения, умноженное на переменную, установленную на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-133">Set the  _lpulMax_ parameter to the minimum value plus the current unit multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="ddb2b-134">Установите для параметра _lpulFlags_ значение 0.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-134">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="ddb2b-135">Выполните необходимые обработки должно выполняться на этот объект.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-135">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="ddb2b-136">Если объект является вложенные объекты и ваш поставщик отображается ход выполнения для вложенных объектов, передайте указатель на объект о ходе выполнения с помощью параметра _lpProgress_ методу.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-136">If the object is a subobject, and your provider displays progress for subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="ddb2b-137">Вызвать [IMAPIProgress::Progress](imapiprogress-progress.md) и передать следующие значения для трех параметров:</span><span class="sxs-lookup"><span data-stu-id="ddb2b-137">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="ddb2b-138">Установите для параметра _ulValue_ переменную, установленную на шаге 2, умноженное на текущий объект.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-138">Set the  _ulValue_ parameter to variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="ddb2b-139">Присвойте параметру _инициализирует метод ulCount_ значение 0.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-139">Set the  _ulCount_ parameter to 0.</span></span> 
      
     - <span data-ttu-id="ddb2b-140">Установите для параметра _ulTotal_ значение 0.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-140">Set the  _ulTotal_ parameter to 0.</span></span> 
    
<span data-ttu-id="ddb2b-141">В следующем примере кода показана логика, необходимые для отображения хода выполнения на всех уровнях операции, который копируется в папку, содержащую пять вложенных папок.</span><span class="sxs-lookup"><span data-stu-id="ddb2b-141">The following code example illustrates the logic required to show progress at all levels of an operation that copies the contents of a folder that contains five subfolders.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="ddb2b-142">См. также</span><span class="sxs-lookup"><span data-stu-id="ddb2b-142">See also</span></span>

- [<span data-ttu-id="ddb2b-143">Индикаторы выполнения MAPI</span><span class="sxs-lookup"><span data-stu-id="ddb2b-143">MAPI Progress Indicators</span></span>](mapi-progress-indicators.md)

