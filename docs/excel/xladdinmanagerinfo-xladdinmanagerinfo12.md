---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- Функция xladdinmanagerinfo [Excel 2007]
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
  
Вызывается Microsoft Excel, когда диспетчер надстроек вызывается в первый раз в сеансе Excel. Эта функция используется для предоставления диспетчеру надстроек сведений о надстройке.
  
Excel 2007 и более поздние версии вызывают **xlAddInManagerInfo12** в предпочтение **xlAddInManagerInfo** , если экспортировано XLL. Функция **xlAddInManagerInfo12** должна работать так же, как и **xlAddInManagerInfo** , чтобы избежать отличий, связанных с ВЕРСИЯМИ, в работе XLL. Excel ожидает, что **xlAddInManagerInfo12** Возвращает тип данных **XLOPER12** , в то время как **xlAddInManagerInfo** должны возвращать **XLOPER**.
  
Функция **xlAddInManagerInfo12** не вызывается в версиях Excel, предшествующих Excel 2007, так как они не поддерживают **XLOPER12**.
  
В Excel не требуется XLL для реализации и экспорта любой из этих функций.
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a>Параметры

 _пксактион:_ Указатель на числовое значение **XLOPER/XLOPER12** (**кслтипеинт** или **кслтипенум**).
  
Сведения, которые Excel запрашивает.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Если _пксактион_ имеет значение, или его можно привести к числу 1, то ваша реализация этой функции должна вернуть строку, содержащую сведения о надстройке, обычно ее имя и, возможно, номер версии. В противном случае возвращается #VALUE!. 
  
Если вы не возвращаете строку, Excel пытается преобразовать возвращенное значение в строку.
  
## <a name="remarks"></a>Примечания

Если возвращаемая строка указывает на динамически выделенный буфер, необходимо убедиться, что этот буфер в конечном итоге освобождается. Если эта строка была выделена приложением Excel, то для этого необходимо установить **кслбиткслфри**. Если строка была выделена библиотекой DLL, это делается путем установки **кслбитдллфри**, а также необходимо реализовать в [xlAutoFree](xlautofree-xlautofree12.md) (при возврате **XLOPER**) или **xlAutoFree12** (если возвращается **XLOPER12**).
  
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

