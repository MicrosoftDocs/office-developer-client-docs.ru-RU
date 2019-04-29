---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fd4b4ad5bf52f29384ef7e0ba738c350189f471e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405284"
---
# <a name="xlgetinstptr"></a>xlGetInstPtr

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает дескриптор экземпляра Microsoft Excel, который в данный момент вызывает БИБЛИОТЕКУ DLL.
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Параметры

У этой функции нет аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Дескриптор экземпляра (**кслтипебигдата**) будет указан в поле **Val. бигдата. h. хдата** . 
  
## <a name="remarks"></a>Примечания

Эту функцию можно использовать для различения нескольких запущенных экземпляров Excel, вызывающих БИБЛИОТЕКУ DLL.
  
Эта функция возвращает правильное значение как с 32, так и с 64 – разрядной версией Excel. Он появился в Excel 2010 как расширение функции [кслжетинст](xlgetinst.md) , которое правильно работает только с версиями Excel, поддерживающими только 32 бит. 
  
Эта функция работает правильно при вызове с использованием [Excel4 и Excel12](excel4-excel12.md) с использованием функций обратного вызова API, так как обе структуры **** и структуры **** , поддерживающие значение **кслтипебигдата** Тип. 
  
## <a name="example"></a>Пример

В следующем примере сравнивается экземпляр последней копии Excel, вызвавшей ее с текущей копией Excel. Если они одинаковы, возвращается 1; в противном случае возвращается значение 0; Если функция завершается со сбоем, возвращается значение "– 1". Этот пример работает как с 32, так и с 64 – разрядной версией Excel.
  
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
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

