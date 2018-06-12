---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- функция xlgetinst [excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9484f7bbc1f5e0fc5b0def17f2ce79ef226dcd17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807359"
---
# <a name="xlgetinst"></a>xlGetInst

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает экземпляр обработчика экземпляра Microsoft Excel, которые в настоящее время звонит библиотеки DLL.
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Parameters

Эта функция не содержит аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

В поле **val.w** будет дескриптор экземпляра (**xltypeInt**). 
  
## <a name="remarks"></a>Замечания

Эта функция используется для различения нескольким экземплярам Excel, которые вызывают библиотеку DLL.
  
При вызове этой функции, с помощью [Excel4](excel4-excel12.md) или [Excel4v](excel4v-excel12v.md)переменной целое число возвращаемых XLOPER является подписанных короткий внутреннего 16-разрядный Это только может содержать низкой 16 бит дескриптор 32-разрядная версия Windows. Начиная с версии Excel 2007, переменной integer **XLOPER12** является подписью int 32-разрядная версия и поэтому содержит весь дескриптор, нужно будет выполнять итерацию всех открытых окон. 
  
> [!IMPORTANT]
> Если функция **xlGetInst** используется в 64-разрядная версия Microsoft Excel, выберите функцию завершится с ошибкой. Это так, как тип значения **xltypeInt** ширины не хватает для хранения 64-разрядная версия длинный дескриптор, возвращенный Excel, в данном случае. Для этой цели Excel 2010 появились новые функции с именем [xlGetInstPtr](xlgetinstptr.md), который работает правильно с 32-разрядной и 64-разрядных версиях Excel. 
  
## <a name="example"></a>Пример

В следующем примере сравниваются экземпляра последнюю копию Excel, которое вызывается для текущей копии Excel, который вызвал ее. Если это так же, он возвращает 1; в противном случае возвращается значение 0; Если происходит сбой функции, возвращается значение -1.
  
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


[Функции интерфейса API для C, которые могут вызываться только из DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

