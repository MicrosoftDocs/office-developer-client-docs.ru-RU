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
# <a name="display-a-progress-indicator"></a>Отобразить индикатор выполнения
 
**Относится к**: Outlook 
  
Чтобы отобразить индикатор выполнения, вызовите [IMAPIProgress::GetFlags](imapiprogress-getflags.md) для получения текущего флаги параметру. 
  
Если значение флага MAPI_TOP_LEVEL, выполните следующие действия:
  
1. Значение переменной равно общее число элементов для обработки в операции. Например при копировании содержимого папки это значение будет равно количество вложенных папок в папке, а также количество сообщений. 
    
2. Значение переменной равно 1000, разделенная на число элементов. 
    
3. Если отображается ход выполнения для вложенных объектов, вызовите метод [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) объекта о ходе выполнения и передает следующие значения для трех параметров: 
    
   - Установите для параметра _lpulMin_ значение 0. 
    
   - Установите для параметра _lpulMax_ до 1000. 
    
   - Установите для параметра _lpulFlags_ значение MAPI_TOP_LEVEL. 
    
4. Для каждого объекта обработки выполните следующие действия:
    
   1. Вызвать **IMAPIProgress::SetLimits** и передать следующие значения для трех параметров: 
      
     - Установите для параметра _lpulMin_ в переменную, установленную на шаге 2, умноженное на текущем элементе минус 1. 
      
     - Установите для параметра _lpulMax_ в переменную, установленную на шаге 2, умноженное на текущий объект. 
      
     - Установите для параметра _lpulFlags_ значение 0. 
      
   2. Выполните необходимые обработки должно выполняться на этот объект. Если это вложенные объекты и для отображения хода выполнения на вложенных объектов, передайте указатель на объект о ходе выполнения с помощью параметра _lpProgress_ методу. 
      
   3. Вызвать [IMAPIProgress::Progress](imapiprogress-progress.md) и передать следующие значения для трех параметров: 
      
     - Установите для параметра _ulValue_ в переменную, установленную на шаге 2, умноженное на текущий объект. 
      
     - Установите для параметра _инициализирует метод ulCount_ для текущего объекта. 
      
     - Установите для параметра _ulTotal_ в переменную, установленную на шаге 1, общее число объектов. 
    
Если флаг MAPI_TOP_LEVEL не установлен, выполните следующие действия.
  
1. Вызов метода [IMAPIProgress::GetMin](imapiprogress-getmin.md) о ходе выполнения объектов для извлечения минимальное значение для отображения. 
    
2. Вызов [IMAPIProgress::GetMax](imapiprogress-getmax.md) для получения максимального значения для отображения. 
    
3. Значение переменной равно общее число объектов для обработки. 
    
4. Значение переменной равно результат вычитания минимальное значение из максимальное значение и затем разделив общее число объектов.
    
5. Для каждого объекта обработки выполните следующие действия:
    
   1. Если ваш поставщик, на котором отображается ход выполнения для вложенных объектов, вызвать **IMAPIProgress::SetLimits** и передать следующие значения для трех параметров: 
      
     - Установите для параметра _lpulMin_ минимальное значение, а также текущего элемента минус 1, умноженное на переменную, установленную на шаге 4. 
      
     - Установите для параметра _lpulMax_ минимальное значение, а также текущего подразделения, умноженное на переменную, установленную на шаге 4. 
      
     - Установите для параметра _lpulFlags_ значение 0. 
      
   2. Выполните необходимые обработки должно выполняться на этот объект. Если объект является вложенные объекты и ваш поставщик отображается ход выполнения для вложенных объектов, передайте указатель на объект о ходе выполнения с помощью параметра _lpProgress_ методу. 
      
   3. Вызвать [IMAPIProgress::Progress](imapiprogress-progress.md) и передать следующие значения для трех параметров: 
      
     - Установите для параметра _ulValue_ переменную, установленную на шаге 2, умноженное на текущий объект. 
      
     - Присвойте параметру _инициализирует метод ulCount_ значение 0. 
      
     - Установите для параметра _ulTotal_ значение 0. 
    
В следующем примере кода показана логика, необходимые для отображения хода выполнения на всех уровнях операции, который копируется в папку, содержащую пять вложенных папок. 
  
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

- [Индикаторы выполнения MAPI](mapi-progress-indicators.md)

