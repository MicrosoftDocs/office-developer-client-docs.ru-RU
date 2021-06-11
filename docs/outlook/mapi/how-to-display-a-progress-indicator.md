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
# <a name="display-a-progress-indicator"></a>Отображение индикатора хода выполнения
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Чтобы отобразить индикатор прогресса, позвоните [в IMAPIProgress::GetFlags,](imapiprogress-getflags.md) чтобы получить текущий параметр флагов. 
  
Если установлен MAPI_TOP_LEVEL флаг, выполните следующие действия:
  
1. Установите переменную, равную общему количеству элементов для обработки в операции. Например, если вы копируете содержимое папки, это значение будет равно числу подмостков в папке и количеству сообщений. 
    
2. Установите переменную, равную 1000, разделенную на количество элементов. 
    
3. Если вы показываете прогресс для подобектов, позвоните по методу [IMAPIProgress объекта progress::SetLimits](imapiprogress-setlimits.md) и передай следующие значения для трех параметров: 
    
   - Установите  _параметр lpulMin_ до 0. 
    
   - Установите  _параметр lpulMax_ до 1000. 
    
   - Установите  _параметр lpulFlags_ для MAPI_TOP_LEVEL. 
    
4. Чтобы каждый объект был обработан, выполните следующие действия:
    
   1. **Вызывай IMAPIProgress::SetLimits и передай** следующие значения для трех параметров: 
      
     - Установите  _параметр lpulMin к_ переменной, заданной на шаге 2, умноженной на текущий элемент минус 1. 
      
     - Установите  _параметр lpulMax к_ переменной, заданной на шаге 2, умноженной на текущий объект. 
      
     - Установите  _параметр lpulFlags до_ 0. 
      
   2. Выполните любую обработку, которая должна быть выполнена на этом объекте. Если это подобект, и необходимо отобразить прогресс в подобектах, передай указатель объекту прогресса в  _параметре lpProgress_ методу. 
      
   3. [Вызывай IMAPIProgress::P и](imapiprogress-progress.md) передай следующие значения для трех параметров: 
      
     - Установите  _параметр ulValue переменной,_ заданной на шаге 2, умноженной на текущий объект. 
      
     - Установите  _параметр ulCount_ текущему объекту. 
      
     - Установите  _параметр ulTotal к_ переменной, заданной на шаге 1, общему числу объектов. 
    
Если флаг MAPI_TOP_LEVEL не установлен, выполните следующие действия:
  
1. Чтобы получить минимальное значение для отображения, позвоните по методу [IMAPIProgress::GetMin](imapiprogress-getmin.md) объекта прогресса. 
    
2. Вызов [IMAPIProgress::GetMax,](imapiprogress-getmax.md) чтобы получить максимальное значение для отображения. 
    
3. Установите переменную, равную общему количеству обрабатываемых объектов. 
    
4. Установите переменную, равную результату вычитания минимального значения из максимального значения и деления на общее количество объектов.
    
5. Чтобы каждый объект был обработан, выполните следующие действия:
    
   1. Если поставщик показывает прогресс в подобектах, позвоните **в службу IMAPIProgress::SetLimits** и передайте следующие значения для трех параметров: 
      
     - Установите  _параметр lpulMin к_ минимальному значению плюс текущий элемент минус 1, умноженный на переменную, заданную на шаге 4. 
      
     - Установите параметр  _lpulMax к_ минимальному значению плюс текущее устройство, умноженное на переменную, заданную в шаге 4. 
      
     - Установите  _параметр lpulFlags до_ 0. 
      
   2. Выполните любую обработку, которая должна быть выполнена на этом объекте. Если объект — это подобект, а поставщик отображает прогресс для подобектов, передайте указатель объекту progress в  _параметре lpProgress_ методу. 
      
   3. [Вызывай IMAPIProgress::P и](imapiprogress-progress.md) передай следующие значения для трех параметров: 
      
     - Установите  _параметр ulValue для_ переменной, заданной в шаге 2, умноженной на текущий объект. 
      
     - Установите  _параметр ulCount_ до 0. 
      
     - Установите  _параметр ulTotal_ до 0. 
    
В следующем примере кода иллюстрируется логика, необходимая для демонстрации прогресса на всех уровнях операции, копирующих содержимое папки, содержаной пять подвещений. 
  
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

## <a name="see-also"></a>См. также

- [Индикаторы прогресса MAPI](mapi-progress-indicators.md)

