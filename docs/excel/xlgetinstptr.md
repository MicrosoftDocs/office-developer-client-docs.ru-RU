---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7cc07093e5db335d01fe85527746594d34d4d938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807371"
---
# <a name="xlgetinstptr"></a>xlGetInstPtr

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает экземпляр обработчика экземпляра Microsoft Excel, которые в настоящее время звонит библиотеки DLL.
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameters

Эта функция не содержит аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

В поле **val.bigdata.h.hdata** будет дескриптор экземпляра (**xltypeBigData**). 
  
## <a name="remarks"></a>Замечания

Эта функция используется для различения нескольким экземплярам Excel, которые вызывают библиотеку DLL.
  
Эта функция возвращает правильное значение с 32-разрядной и 64-разрядных версиях Excel. Она была введена в Excel 2010 как расширение в функцию [xlGetInst](xlgetinst.md) , которая правильно работает только с 32-разрядных версиях Excel. 
  
Эта функция работает правильно при вызове с помощью [Excel4 и Excel12](excel4-excel12.md) видов функции обратного вызова API, поскольку **XLOPER** и **XLOPER12** имеют ту же структуру, которая поддерживает значение **xltypeBigData** тип. 
  
## <a name="example"></a>Пример

В следующем примере сравниваются экземпляра последнюю копию Excel, которое вызывается для текущей копии Excel, который вызвал ее. Если это так же, он возвращает 1; в противном случае возвращается значение 0; Если происходит сбой функции, возвращается значение -1. В этом примере для работы с 32-разрядной и 64-разрядных версиях Excel.
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstPtrExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInstPtr, &xRes, 0) != xlretSuccess)
    iRet = -1;
    else
    {
    HANDLE hNew;
    hNew =  xRes.val.bigdata.h.hdata;
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

- [xlGetHwnd](xlgethwnd.md)
- [xlGetInst](xlgetinst.md)
- [Функции интерфейса API для C, которые могут вызываться только из DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

