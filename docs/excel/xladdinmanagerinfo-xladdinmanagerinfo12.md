---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- функция xladdinmanagerinfo [Excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66d2ac05b9603d6bb587a3898bde2545c1bb844a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407797"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Вызывается Microsoft Excel при первом вызове диспетчера надстройки в Excel сеансе. Эта функция используется для предоставления Add-In менеджеру сведений о вашей надстройки.
  
Excel 2007 и более поздних версиях вызов **xlAddInManagerInfo12** в предпочтение **xlAddInManagerInfo,** если экспортируется XLL. Функция **xlAddInManagerInfo12** должна работать так же, как **xlAddInManagerInfo,** чтобы избежать различий в поведении XLL. Excel **xlAddInManagerInfo12** возвращает тип данных **XLOPER12,** в то время как **xlAddInManagerInfo** должен возвращать **XLOPER**.
  
Функция **xlAddInManagerInfo12** не вызвана версиями Excel раньше Excel 2007 г., так как они не поддерживают **XLOPER12**.
  
Excel XLL не требуется для реализации и экспорта этих функций.
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a>Parameters

 _pxAction:_ Указатель на числовые **XLOPER/XLOPER12** **(xltypeInt** или **xltypeNum).**
  
Сведения, которые Excel запрашивается.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Если  _pxAction_ является или может быть принужден к номеру 1, то при реализации этой функции должна быть возвращена строка, содержащая некоторые сведения о надстройке, как правило, ее имя и, возможно, номер версии. В противном случае он должен #VALUE!. 
  
Если строка не возвращается, Excel пытается преобразовать возвращенные значения в строку.
  
## <a name="remarks"></a>Примечания

Если возвращенная строка указывает на динамически выделенный буфер, необходимо убедиться, что этот буфер в конечном итоге будет освобожден. Если строка была выделена Excel, для этого необходимо установить **xlbitXLFree.** Если строка была выделена DLL, для этого необходимо установить **xlbitDLLFree,** а также реализовать ее в [xlAutoFree](xlautofree-xlautofree12.md) (если вы возвращаете **XLOPER)** или **xlAutoFree12** (если вы возвращаете **XLOPER12).**
  
## <a name="example"></a>Пример

 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 xAction)
{
    static XLOPER12 xInfo, xIntAction;
/*
** This code coerces the passed-in value to an integer. This is how the
** code determines what is being requested. If it receives a 1, it returns a
** string representing the long name. If it receives anything else, it
** returns a #VALUE! error.
*/
    Excel12f(xlCoerce, &xIntAction, 2, xAction, TempInt12(xltypeInt));
    if(xIntAction.val.w == 1) 
    {
        xInfo.xltype = xltypeStr;
        xInfo.val.str = L"\026Example Standalone DLL";
    }
    else 
    {
        xInfo.xltype = xltypeErr;
        xInfo.val.err = xlerrValue;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe. Use alternate memory allocation mechanisms.
    return (LPXLOPER12)&xInfo;
} 

```

## <a name="see-also"></a>См. также



[Функции диспетчера надстроек и интерфейса XLL](add-in-manager-and-xll-interface-functions.md)

