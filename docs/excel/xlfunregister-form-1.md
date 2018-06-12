---
title: xlfUnregister (формы 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- функция xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 6077027a27c054c5a5e65a751373c41a87cb3836
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807358"
---
# <a name="xlfunregister-form-1"></a>xlfUnregister (формы 1)

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Может быть вызван из DLL или XLL команду, которая был вызван с Microsoft Excel. Это эквивалентно вызову **Отменить РЕГИСТРАЦИЮ** из таблицы Excel XLM макрос. 
  
**xlfUnregister** может быть вызван в двух вариантах: 
  
- Форма 1: Отменяет отдельные команды или функции.
    
- Форма 2: Выгрузка и деактивирует надстройке XLL.
    
Вызывает в виде 1, эта функция уменьшает число использования функции DLL или команды, которое ранее было зарегистрировано с помощью **xlfRegister** или **регистрации**. Если счетчик использования уже равно нулю, эта функция не оказывает влияния. По достижении нулевой счетчик использования всех функций в библиотеке DLL библиотеки DLL выгрузки из памяти.
  
**xlfRegister** (Форма 1) также определяет скрытые имя которого является аргумента функции текст, _pxFunctionText_и которая вычисляет функцию или идентификатор команды регистрации. После отмены регистрации функцию, это имя следует удалить с помощью **xlfSetName** , чтобы с помощью мастера функций, больше не отображается имя функции. Для получения дополнительных сведений см [Известные проблемы при разработке XLL для Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a>Parameters

_pxRegisterId_ (**xltypeNum**)
  
КОД регистрации функции для отмены регистрации.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

В случае успеха возвращает **значение TRUE** (**xltypeBool**), в противном случае возвращается значение FALSE.
  
## <a name="remarks"></a>Замечания

Зарегистрированные регистрации, код функции, возвращаемый **xlfRegister** при первом выполнении функции. Он также можно получить путем вызова [функции xlfRegisterId](xlfregisterid.md) или [xlfEvaluate функции](xlfevaluate.md). Обратите внимание, что этот xlfRegisterId пытается зарегистрировать функцию, если он еще не зарегистрирован. По этой причине если только вы пытаетесь получить идентификатор, поэтому можно отменить регистрацию функцию, лучше его можно получить, передав зарегистрированное имя **xlfEvaluate**. Если функция не зарегистрирована, **xlfEvaluate** происходит сбой с #NAME? Ошибка. 
  
## <a name="example"></a>Пример

Просмотр кода для функции **fExit** в `\SAMPLES\GENERIC\GENERIC.C`.
  
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

- [xlfRegister (����� 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (формы 2)](xlfunregister-form-2.md)
- [Функции API XLM важные и полезные C](essential-and-useful-c-api-xlm-functions.md)

