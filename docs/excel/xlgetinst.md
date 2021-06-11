---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- функция xlgetinst [Excel 2007]
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
  
Возвращает ручку экземпляра экземпляра Microsoft Excel, который в настоящее время вызывает DLL.
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Parameters

Эта функция не имеет аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Ручка экземпляра **(xltypeInt)** будет в **поле val.w.** 
  
## <a name="remarks"></a>Примечания

Эта функция может использоваться для различия между несколькими запущенными экземплярами Excel, вызываемой DLL.
  
При вызове этой функции с [помощью Excel4](excel4-excel12.md) или [Excel4v](excel4v-excel12v.md)возвращаемая переменная XLOPER является подписанной 16-битной короткой int. Это может содержать только 16-битную 32-Windows. Начиная с Excel 2007 г. целая переменная **XLOPER12** — это подписанный 32-битный int и, следовательно, содержит всю ручку, удаляя необходимость итерации всех открытых окон. 
  
> [!IMPORTANT]
> Если **функция xlGetInst** используется с 64-битной версией Microsoft Excel, функция не работает. Это потому, что тип **значения xltypeInt** недостаточно широк, чтобы удерживать 64-битную длинную ручку, возвращаемую Excel в этом случае. Для этого Excel 2010 г. представила новую функцию [xlGetInstPtr,](xlgetinstptr.md)которая работает правильно с 32-битными и 64-битными версиями Excel. 
  
## <a name="example"></a>Пример

В следующем примере сравнивает экземпляр последней копии Excel, назвавшей его текущей копией Excel, назвавшей его. Если они одинаковы, возвращается 1; если нет, он возвращает 0; если функция не работает, она возвращает -1.
  
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

