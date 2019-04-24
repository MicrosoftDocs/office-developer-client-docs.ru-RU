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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345131"
---
# <a name="display-a-progress-indicator"></a><span data-ttu-id="53919-103">Отображение индикатора хода выполнения</span><span class="sxs-lookup"><span data-stu-id="53919-103">Display a progress indicator</span></span>
 
<span data-ttu-id="53919-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53919-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53919-105">Чтобы отобразить индикатор хода выполнения, вызовите [IMAPIProgress::](imapiprogress-getflags.md) GetSetting, чтобы получить текущие параметры флагов.</span><span class="sxs-lookup"><span data-stu-id="53919-105">To display a progress indicator, call [IMAPIProgress::GetFlags](imapiprogress-getflags.md) to retrieve the current flags setting.</span></span> 
  
<span data-ttu-id="53919-106">Если установлен флаг МАПИ_ТОП_ЛЕВЕЛ, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="53919-106">If the MAPI_TOP_LEVEL flag is set, complete the following steps:</span></span>
  
1. <span data-ttu-id="53919-107">Задайте переменную, равную общему количеству элементов, обрабатываемых в операции.</span><span class="sxs-lookup"><span data-stu-id="53919-107">Set a variable equal to the total number of items to process in the operation.</span></span> <span data-ttu-id="53919-108">Например, если вы копируете содержимое папки, это значение будет равным числу вложенных папок в папке плюс количество сообщений.</span><span class="sxs-lookup"><span data-stu-id="53919-108">For example, if you are copying the contents of a folder, this value will be equal to the number of the subfolders in the folder plus the number of messages.</span></span> 
    
2. <span data-ttu-id="53919-109">Установите переменную равное 1000 на число элементов.</span><span class="sxs-lookup"><span data-stu-id="53919-109">Set a variable equal to 1000 divided by the number of items.</span></span> 
    
3. <span data-ttu-id="53919-110">Если отображается ход выполнения для подобъектов, вызовите метод [IMAPIProgress:: SetLimits](imapiprogress-setlimits.md) объекта Progress и передайте следующие значения для трех параметров:</span><span class="sxs-lookup"><span data-stu-id="53919-110">If you are showing progress for subobjects, call the progress object's [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method and pass the following values for the three parameters:</span></span> 
    
   - <span data-ttu-id="53919-111">Задайте для параметра _Лпулмин_ значение 0.</span><span class="sxs-lookup"><span data-stu-id="53919-111">Set the  _lpulMin_ parameter to 0.</span></span> 
    
   - <span data-ttu-id="53919-112">Установите для параметра _Лпулмакс_ значение 1000.</span><span class="sxs-lookup"><span data-stu-id="53919-112">Set the  _lpulMax_ parameter to 1000.</span></span> 
    
   - <span data-ttu-id="53919-113">ПриСвойте параметру _Лпулфлагс_ значение мапи_топ_левел.</span><span class="sxs-lookup"><span data-stu-id="53919-113">Set the  _lpulFlags_ parameter to MAPI_TOP_LEVEL.</span></span> 
    
4. <span data-ttu-id="53919-114">Для каждого объекта, который необходимо обработать, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="53919-114">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="53919-115">Call **IMAPIProgress:: SetLimits** и передайте следующие значения для трех параметров:</span><span class="sxs-lookup"><span data-stu-id="53919-115">Call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="53919-116">Задайте для параметра _лпулмин_ значение, заданное в пункте 2, умноженное на значение текущего элемента минус 1.</span><span class="sxs-lookup"><span data-stu-id="53919-116">Set the  _lpulMin_ parameter to the variable set in step 2 multiplied by the current item minus 1.</span></span> 
      
     - <span data-ttu-id="53919-117">Задайте для параметра _лпулмакс_ значение, заданное в пункте 2, умноженное на текущий объект.</span><span class="sxs-lookup"><span data-stu-id="53919-117">Set the  _lpulMax_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="53919-118">Задайте для параметра _Лпулфлагс_ значение 0.</span><span class="sxs-lookup"><span data-stu-id="53919-118">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="53919-119">Выполнение любой обработки, которую необходимо выполнить для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="53919-119">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="53919-120">Если это объект и требуется отображать ход выполнения для подобъектов, передайте указатель на объект Progress в параметре _лппрогресс_ в метод.</span><span class="sxs-lookup"><span data-stu-id="53919-120">If this is a subobject and you want to display progress on subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="53919-121">Call [IMAPIProgress::P рогресс](imapiprogress-progress.md) и передайте следующие значения для трех параметров:</span><span class="sxs-lookup"><span data-stu-id="53919-121">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="53919-122">Задайте для параметра _улвалуе_ значение, заданное в пункте 2, умноженное на текущий объект.</span><span class="sxs-lookup"><span data-stu-id="53919-122">Set the  _ulValue_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="53919-123">Установите для параметра _улкаунт_ текущий объект.</span><span class="sxs-lookup"><span data-stu-id="53919-123">Set the  _ulCount_ parameter to the current object.</span></span> 
      
     - <span data-ttu-id="53919-124">ПриСвойте параметру _ултотал_ значение, заданное на шаге 1, на общее число объектов.</span><span class="sxs-lookup"><span data-stu-id="53919-124">Set the  _ulTotal_ parameter to the variable set in step 1, the total number of objects.</span></span> 
    
<span data-ttu-id="53919-125">Если флаг МАПИ_ТОП_ЛЕВЕЛ не установлен, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="53919-125">If the MAPI_TOP_LEVEL flag is not set, complete the following steps:</span></span>
  
1. <span data-ttu-id="53919-126">ВыЗовите метод [IMAPIProgress:: GetMin](imapiprogress-getmin.md) объекта Progress, чтобы получить минимальное значение для отображения.</span><span class="sxs-lookup"><span data-stu-id="53919-126">Call the progress object's [IMAPIProgress::GetMin](imapiprogress-getmin.md) method to retrieve the minimum value for the display.</span></span> 
    
2. <span data-ttu-id="53919-127">Call [IMAPIProgress:: жетмакс](imapiprogress-getmax.md) , чтобы получить максимальное значение для отображения.</span><span class="sxs-lookup"><span data-stu-id="53919-127">Call [IMAPIProgress::GetMax](imapiprogress-getmax.md) to retrieve the maximum value for the display.</span></span> 
    
3. <span data-ttu-id="53919-128">Задайте переменную, равную общему количеству обрабатываемых объектов.</span><span class="sxs-lookup"><span data-stu-id="53919-128">Set a variable equal to the total number of objects to be processed.</span></span> 
    
4. <span data-ttu-id="53919-129">ПриСвойте переменной значение, равное результату вычитания минимума из максимального значения, а затем — по общему количеству объектов.</span><span class="sxs-lookup"><span data-stu-id="53919-129">Set a variable equal to the result of subtracting the minimum value from the maximum value and then dividing by the total number of objects.</span></span>
    
5. <span data-ttu-id="53919-130">Для каждого объекта, который необходимо обработать, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="53919-130">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="53919-131">Если поставщик показывает ход выполнения для подобъектов, вызовите метод **IMAPIProgress:: SetLimits** и передайте следующие значения для трех параметров:</span><span class="sxs-lookup"><span data-stu-id="53919-131">If your provider is showing progress for subobjects, call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="53919-132">Установите для параметра _лпулмин_ минимальное значение плюс текущий элемент минус 1, умноженное на значение, заданное на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="53919-132">Set the  _lpulMin_ parameter to the minimum value plus the current item minus 1 multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="53919-133">Установите для параметра _лпулмакс_ минимальное значение плюс текущее единицу измерения, умноженное на переменную, установленную на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="53919-133">Set the  _lpulMax_ parameter to the minimum value plus the current unit multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="53919-134">Задайте для параметра _Лпулфлагс_ значение 0.</span><span class="sxs-lookup"><span data-stu-id="53919-134">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="53919-135">Выполнение любой обработки, которую необходимо выполнить для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="53919-135">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="53919-136">Если объект является подобъектом, а поставщик отображает ход выполнения для подобъектов, передайте указатель на объект Progress в параметре _лппрогресс_ в метод.</span><span class="sxs-lookup"><span data-stu-id="53919-136">If the object is a subobject, and your provider displays progress for subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="53919-137">Call [IMAPIProgress::P рогресс](imapiprogress-progress.md) и передайте следующие значения для трех параметров:</span><span class="sxs-lookup"><span data-stu-id="53919-137">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="53919-138">Задайте для параметра _улвалуе_ значение переменная Set в шаге 2, умноженной на текущий объект.</span><span class="sxs-lookup"><span data-stu-id="53919-138">Set the  _ulValue_ parameter to variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="53919-139">Задайте для параметра _Улкаунт_ значение 0.</span><span class="sxs-lookup"><span data-stu-id="53919-139">Set the  _ulCount_ parameter to 0.</span></span> 
      
     - <span data-ttu-id="53919-140">Задайте для параметра _Ултотал_ значение 0.</span><span class="sxs-lookup"><span data-stu-id="53919-140">Set the  _ulTotal_ parameter to 0.</span></span> 
    
<span data-ttu-id="53919-141">В приведенном ниже примере кода показана логика, необходимая для отображения хода выполнения на всех уровнях операции, которая копирует содержимое папки, содержащей пять вложенных папок.</span><span class="sxs-lookup"><span data-stu-id="53919-141">The following code example illustrates the logic required to show progress at all levels of an operation that copies the contents of a folder that contains five subfolders.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="53919-142">См. также</span><span class="sxs-lookup"><span data-stu-id="53919-142">See also</span></span>

- [<span data-ttu-id="53919-143">Индикаторы хода выполнения MAPI</span><span class="sxs-lookup"><span data-stu-id="53919-143">MAPI Progress Indicators</span></span>](mapi-progress-indicators.md)

