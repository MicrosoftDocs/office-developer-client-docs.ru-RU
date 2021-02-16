---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- Функция xlgetinst [excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e113ddbf55e2b4651d578549802c44e2c6413a18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428132"
---
# <a name="xlgetinst"></a>xlGetInst

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает handle экземпляра Microsoft Excel, который в настоящее время вызывает DLL.
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Параметры

Эта функция не имеет аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Handle экземпляра **(xltypeInt)** будет в поле **val.w.** 
  
## <a name="remarks"></a>Примечания

Эту функцию можно использовать для различия между несколькими запущенными экземплярами Excel, которые вызывает DLL.
  
При вызове этой функции с помощью [Excel4](excel4-excel12.md) или [Excel4v](excel4v-excel12v.md)возвращаемая переменная XLOPER — это 16-битное короткое 16-битное int. Это может содержать только 16-битные 32-битные 32-битные точки Windows. Начиная с Excel 2007, целомерная переменная **XLOPER12** — это 32-битное целое значение, которое содержит весь лад, удаляя необходимость в итерации всех открытых окон. 
  
> [!IMPORTANT]
> Если функция **xlGetInst** используется с 64-битной версией Microsoft Excel, функция не будет работать. Это необходимо из-за того, что тип значения **xltypeInt** не является достаточно широким для удержания 64-битного длинного handle, возвращенного Excel в данном случае. Для этой цели в Excel 2010 представлена новая функция [xlGetInstPtr,](xlgetinstptr.md)которая правильно работает как в 32-, так и в 64-битных версиях Excel. 
  
## <a name="example"></a>Пример

В следующем примере сравнивается экземпляр последней копии Excel, которая вызвала его, с текущей копией Excel, которая ее вызвала. Если они одинаковы, возвращается 1; Если нет, возвращается 0; если функция не работает, она возвращает -1.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInst, &xRes, 0) != xlretSuccess)
        iRet = -1;
    else
    {
    HANDLE hNew;
    hNew = (HANDLE)xRes.val.w;
    if (hNew != hOld)
            iRet = 0;
    else
            iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a>См. также



[xlGetHwnd](xlgethwnd.md)
  
[xlGetInstPtr](xlgetinstptr.md)


[Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

