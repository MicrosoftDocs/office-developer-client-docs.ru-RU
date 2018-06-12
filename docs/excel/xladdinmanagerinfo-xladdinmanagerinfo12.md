---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- функция xladdinmanagerinfo [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e42cca809c4426ddf9a98b3b275d08490d31c8db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807327"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Именем с Microsoft Excel, когда диспетчер надстроек вызывается в первый раз в сеансе Excel. Эта функция используется для предоставления сведений о надстройке Диспетчер надстроек.
  
Excel 2007 и более поздних версий вызовите **xlAddInManagerInfo12** вместо **xlAddInManagerInfo** при экспорте с XLL. Функция **xlAddInManagerInfo12** должны работать в так же, как **xlAddInManagerInfo** во избежание разных версий различия в поведении XLL. Предполагается, что **xlAddInManagerInfo12** возвращает тип данных **XLOPER12** , тогда как **xlAddInManagerInfo** должен возвращать **XLOPER**.
  
Функция **xlAddInManagerInfo12** не вызывается с версии Excel, предшествующие Excel 2007, как они не поддерживают **XLOPER12**.
  
Excel не требуется XLL внедрение и экспортировать любой из этих функций.
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a>Parameters

 _pxAction:_ Указатель на числовой **XLOPER и XLOPER12** (**xltypeInt** или **xltypeNum**).
  
Сведения о, запрашивает Excel.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Если _pxAction_ является или могут быть приведены к номер 1, реализация этой функции должен возвращать строку, содержащую сведения о надстройки, обычно его имя и может быть номер версии. В противном случае возвращается #VALUE!. 
  
Если строка не возвращают, Excel пытается преобразовать возвращаемое значение в строку.
  
## <a name="remarks"></a>Замечания

Если Возвращенная строка указывает динамически выделенный буфер, необходимо убедиться, что в конечном счете освобождается этот буфер. Если строка выделена в Excel, это можно сделать, задав **xlbitXLFree**. Если строка была выделена библиотеки DLL, для этого параметра **xlbitDLLFree**и также необходимо реализовать в [xlAutoFree](xlautofree-xlautofree12.md) (если, возвращают **XLOPER**) или **xlAutoFree12** (если, возвращают **XLOPER12**).
  
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



[Диспетчер надстроек и функции XLL интерфейса](add-in-manager-and-xll-interface-functions.md)

