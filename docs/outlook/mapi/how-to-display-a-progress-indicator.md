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
 
**Относится к**: Outlook 2013 | Outlook 2016 
  
Чтобы отобразить индикатор хода выполнения, вызовите [IMAPIProgress::GetFlags,](imapiprogress-getflags.md) чтобы получить текущий параметр флагов. 
  
Если установлен MAPI_TOP_LEVEL флага, выполните следующие действия.
  
1. Установите переменную, равную общему числу элементов, которые необходимо обработать в операции. Например, если вы копируете содержимое папки, это значение будет равно числу вложенных папок в папке и количеству сообщений. 
    
2. Установите переменную равной 1000, разделенной на количество элементов. 
    
3. Если вы показываете ход выполнения для подобектов, вызовите метод [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) объекта progress и передав следующие значения для трех параметров: 
    
   - Установите для  _параметра lpulMin_ 0. 
    
   - Установите для  _параметра lpulMax_ параметр 1000. 
    
   - Установите для  _параметра lpulFlags_ MAPI_TOP_LEVEL. 
    
4. Для обработки каждого объекта выполните следующие действия:
    
   1. Вызовите **IMAPIProgress::SetLimits и передав** следующие значения для трех параметров: 
      
     - Установите для  _параметра lpulMin_ переменную, заданную на шаге 2, умноженную на текущий элемент минус 1. 
      
     - Установите для  _параметра lpulMax переменную,_ заданную на шаге 2, умноженную на текущий объект. 
      
     - Установите для  _параметра lpulFlags_ 0. 
      
   2. Выполните любую обработку, которая должна быть выполнена для этого объекта. Если это подобект и вы хотите отобразить ход выполнения в подобектах, передав указатель на объект хода выполнения в параметре  _lpProgress_ в метод. 
      
   3. Вызовите [IMAPIProgress::P и](imapiprogress-progress.md) передав следующие значения для трех параметров: 
      
     - Установите для  _параметра ulValue переменную,_ заданную на шаге 2, умноженную на текущий объект. 
      
     - Установите для  _параметра ulCount_ текущий объект. 
      
     - Установите для  _параметра ulTotal_ переменную, заданную на шаге 1, общее количество объектов. 
    
Если флаг MAPI_TOP_LEVEL не установлен, выполните следующие действия:
  
1. Вызовите метод [IMAPIProgress::GetMin](imapiprogress-getmin.md) объекта progress, чтобы получить минимальное значение для дисплея. 
    
2. Вызовите [IMAPIProgress::GetMax,](imapiprogress-getmax.md) чтобы получить максимальное значение для дисплея. 
    
3. Установите переменную, равную общему числу обрабатываемых объектов. 
    
4. Установите переменную, равную результату вычитания минимального значения из максимального значения и деления на общее число объектов.
    
5. Для обработки каждого объекта выполните следующие действия:
    
   1. Если поставщик показывает ход выполнения для подобектов, вызовите **IMAPIProgress::SetLimits и передайте** следующие значения для трех параметров: 
      
     - Установите для  _параметра lpulMin_ минимальное значение плюс текущий элемент минус 1, умноженный на переменную, заданную на шаге 4. 
      
     - Установите для  _параметра lpulMax минимальное_ значение плюс текущую единицу, умноженную на переменную, установленную на шаге 4. 
      
     - Установите для  _параметра lpulFlags_ 0. 
      
   2. Выполните любую обработку, которая должна быть выполнена для этого объекта. Если объект является подобектом и поставщик отображает ход выполнения для подобектов, передайте указатель на объект progress в параметре  _lpProgress_ методу. 
      
   3. Вызовите [IMAPIProgress::P и](imapiprogress-progress.md) передав следующие значения для трех параметров: 
      
     - Установите для  _параметра ulValue переменную,_ заданную на шаге 2, умноженную на текущий объект. 
      
     - Установите для  _параметра ulCount_ 0. 
      
     - Установите  _для параметра ulTotal_ 0. 
    
В следующем примере кода иллюстрируется логика, необходимая для демонстрации хода выполнения на всех уровнях операции, копирующие содержимое папки, которая содержит пять вложенных папок. 
  
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

- [Индикаторы хода выполнения MAPI](mapi-progress-indicators.md)

