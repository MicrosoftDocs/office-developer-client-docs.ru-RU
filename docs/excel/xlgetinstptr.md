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
  
Возвращает ручку экземпляра экземпляра Microsoft Excel, который в настоящее время вызывает DLL.
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parameters

Эта функция не имеет аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Ручка экземпляра **(xltypeBigData)** будет в **поле val.bigdata.h.hdata.** 
  
## <a name="remarks"></a>Примечания

Эта функция может использоваться для различия между несколькими запущенными экземплярами Excel, вызываемой DLL.
  
Эта функция возвращает правильное значение с 32-битными и 64-битными версиями Excel. Она была представлена Excel 2010 г. в качестве расширения функции [xlGetInst,](xlgetinst.md) которая работает правильно только с 32-битными версиями Excel. 
  
Эта функция работает правильно, если она вызвана с помощью вариантов Excel4 и [Excel12](excel4-excel12.md) функций вызова API, так как оба **XLOPER** и **XLOPER12** имеют ту же структуру, которая поддерживает тип **значения xltypeBigData.** 
  
## <a name="example"></a>Пример

В следующем примере сравнивает экземпляр последней копии Excel, назвавшей его текущей копией Excel, назвавшей его. Если они одинаковы, возвращается 1; если нет, он возвращает 0; если функция не работает, она возвращает -1. Этот пример работает с 32-битными и 64-битными версиями Excel.
  
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

