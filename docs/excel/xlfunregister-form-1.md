---
title: xlfUnregister (форма 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- Функция xlfUnregister [Excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3f5ebc08f89651331186990d8574e3150d4f484a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303894"
---
# <a name="xlfunregister-form-1"></a>xlfUnregister (форма 1)

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Может вызываться из команды DLL или XLL, которая вызывается Microsoft Excel. Это эквивалентно вызову **Unregister** из листа макросов Excel XLM. 
  
**xlfUnregister** можно вызывать в двух формах: 
  
- Форма 1: Отмена регистрации отдельной команды или функции.
    
- Форма 2: выгрузка и деактивация XLL.
    
Эта функция уменьшает количество использований функции или команды DLL, которые были зарегистрированы с помощью **xlfRegister** или **Register**, в форме 1. Если число использований уже равно нулю, эта функция не оказывает никакого действия. Если счетчик использования всех функций в библиотеке DLL достигает нуля, Библиотека DLL выгружается из памяти.
  
**xlfRegister** (Форма 1) также определяет скрытое имя, которое представляет собой аргумент text функции, _пксфунктионтекст_, и который определяет идентификатор регистрации функции или команды. При отмене регистрации функции это имя должно быть удалено с помощью **xlfSetName** , чтобы имя функции больше не переЧислено мастером функций. Дополнительные сведения см. в статье [Известные проблемы, возникающие при разработке XLL для Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a>Параметры

_пксрегистерид_ (**кслтипенум**)
  
ИДЕНТИФИКАТОР регистрации функции, которая будет отменена.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

В случае успеха возвращает **значение true** (**кслтипебул**), в противном случае возвращает значение false.
  
## <a name="remarks"></a>Замечания

ИДЕНТИФИКАТОР регистрации функции возвращается **xlfRegister** при первой регистрации функции. Его также можно получить, вызвав [функцию кслфрегистерид](xlfregisterid.md) или [функцию xlfEvaluate](xlfevaluate.md). Обратите внимание, что Кслфрегистерид пытается зарегистрировать функцию, если она еще не зарегистрирована. По этой причине, если вы пытаетесь получить идентификатор только для того, чтобы можно было отменить регистрацию функции, ее лучше получить, передав зарегистрированное имя в **xlfEvaluate**. Если функция не была зарегистрирована, **xlfEvaluate** завершается с ошибкой #NAME? ошибкой. 
  
## <a name="example"></a>Пример

Обратитесь к коду функции **фексит** в `\SAMPLES\GENERIC\GENERIC.C`файле.
  
```cs
int WINAPI fExit(void)
{
   XLOPER12  xDLL,    // The name of this DLL //
   xFunc,             // The name of the function //
   xRegId;            // The registration ID //
   int i;
//
// This code gets the DLL name. It then uses this along with information
// from g_rgFuncs[] to obtain a REGISTER.ID() for each function. The
// register ID is then used to unregister each function. Then the code
// frees the DLL name and calls xlAutoClose.
//
   // Make xFunc a string //
   xFunc.xltype = xltypeStr;
   Excel12f(xlGetName, &xDLL, 0);
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgWorksheetFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   for (i = 0; i < g_rgCommandFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgCommandFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   Excel12f(xlFree, 0, 1,  (LPXLOPER12) &xDLL);
   return xlAutoClose();
}
```

## <a name="see-also"></a>См. также

- [xlfRegister (форма 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (форма 2)](xlfunregister-form-2.md)
- [Необходимые и полезные функции XLM из API C](essential-and-useful-c-api-xlm-functions.md)

