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
  
Возвращает handle экземпляра Microsoft Excel, который в настоящее время вызывает DLL.
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Параметры

Эта функция не имеет аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Handle экземпляра (**xltypeBigData)** будет в **поле val.bigdata.h.hdata.** 
  
## <a name="remarks"></a>Примечания

Эту функцию можно использовать для различия между несколькими запущенными экземплярами Excel, которые вызывает DLL.
  
Эта функция возвращает правильное значение для 32- и 64-битных версий Excel. Она была представлена в Excel 2010 как расширение функции [xlGetInst,](xlgetinst.md) которая правильно работает только с 32-битными версиями Excel. 
  
Эта функция работает правильно при вызове с помощью вариантов Функции вызова API Excel4 и [Excel12,](excel4-excel12.md) так как **XLOPER** и **XLOPER12** имеют ту же структуру, которая поддерживает тип значения **xltypeBigData.** 
  
## <a name="example"></a>Пример

В следующем примере сравнивается экземпляр последней копии Excel, которая вызвала его, с текущей копией Excel, которая ее вызвала. Если они одинаковы, возвращается 1; Если нет, возвращается 0; если функция не работает, она возвращает -1. Этот пример работает как с 32-, так и с 64-битными версиями Excel.
  
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

