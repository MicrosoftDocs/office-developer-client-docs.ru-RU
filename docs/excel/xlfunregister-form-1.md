---
title: xlfUnregister (форма 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- Функция xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3f5ebc08f89651331186990d8574e3150d4f484a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410086"
---
# <a name="xlfunregister-form-1"></a>xlfUnregister (форма 1)

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Может быть вызван из команды DLL или XLL, которая сама была вызвана Microsoft Excel. Это эквивалентно вызову **UNREGISTER** из листа макроса XLM Excel. 
  
**XlfUnregister** может быть вызван в двух формах: 
  
- Форма 1. Unregisters an individual command or function.
    
- Форма 2. Выгружает и деактивирует XLL.
    
Эта функция, вызванная в форме 1, уменьшает количество использования функции DLL или команды, которая ранее была зарегистрирована с помощью **xlfRegister** или **REGISTER.** Если количество использования уже нулевое, эта функция не действует. Когда количество использования всех функций в DLL достигает нуля, DLL выгружается из памяти.
  
**XlfRegister** (форма 1) также определяет скрытое имя, которое является текстовым аргументом функции  _pxFunctionText_ и оценивается как регистрационный ИД функции или команды. При отостановке регистрации функции это имя следует удалить с помощью **xlfSetName,** чтобы имя функции больше не было указано мастером функций. Дополнительные сведения см. в статье [Известные проблемы, возникающие при разработке XLL для Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a>Параметры

_pxRegisterId_ (**xltypeNum)**
  
ИД регистрации функции, которая должна быть отрегистрирована.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

В случае успеха **возвращается TRUE** (**xltypeBool),** в противном случае возвращается FALSE.
  
## <a name="remarks"></a>Примечания

ИД регистрации функции **возвращается xlfRegister** при первой регистрации функции. Его также можно получить, вызывая [функцию xlfRegisterId](xlfregisterid.md) или [функцию xlfEvaluate.](xlfevaluate.md) Обратите внимание, что xlfRegisterId пытается зарегистрировать функцию, если она еще не зарегистрирована. По этой причине, если вы пытаетесь получить только ИД, чтобы отозарегистрировать функцию, лучше получить ее, передав зарегистрированное имя **в xlfEvaluate**. Если функция не зарегистрирована, **xlfEvaluate** не работает с #NAME? error. 
  
## <a name="example"></a>Пример

См. код **функции fExit** в  `\SAMPLES\GENERIC\GENERIC.C` .
  
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

