---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- Функция кслжетинст [Excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e113ddbf55e2b4651d578549802c44e2c6413a18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303852"
---
# <a name="xlgetinst"></a>xlGetInst

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает дескриптор экземпляра Microsoft Excel, который в данный момент вызывает БИБЛИОТЕКУ DLL.
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Параметры

У этой функции нет аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Дескриптор экземпляра (**кслтипеинт**) будет указан в поле **Val. w** . 
  
## <a name="remarks"></a>Замечания

Эту функцию можно использовать для различения нескольких запущенных экземпляров Excel, вызывающих БИБЛИОТЕКУ DLL.
  
При вызове этой функции с помощью [Excel4](excel4-excel12.md) или [Excel4v](excel4v-excel12v.md)возвращенная целочисленная переменная XLOPER имеет знак 16-bit short int. Это может быть только в том случае, если он содержит младшие 16 разрядов для дескриптора Windows 32-bit. Начиная с версии Excel 2007, целочисленная переменная **XLOPER12** — это подписанное 32-разрядное целое число, поэтому он содержит весь дескриптор, устраняя необходимость в итерации всех открытых окон. 
  
> [!IMPORTANT]
> Если функция **кслжетинст** используется с 64-разрядной версией Microsoft Excel, функция завершится с ошибками. Это обусловлено тем, что тип значения **кслтипеинт** недостаточно широк для хранения 64-разрядных дескрипторов, возвращенНых приложением Excel в данном случае. Для этой цели в Excel 2010 появилась новая функция с именем [кслжетинстптр](xlgetinstptr.md), которая правильно работает как с 32ом, так и с 64 – разрядной версией Excel. 
  
## <a name="example"></a>Пример

В следующем примере сравнивается экземпляр последней копии Excel, вызвавшей ее с текущей копией Excel. Если они одинаковы, возвращается 1; в противном случае возвращается значение 0; Если функция завершается со сбоем, возвращается значение "– 1".
  
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

