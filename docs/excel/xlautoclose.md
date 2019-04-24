---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- функция xlautoclose [excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e27ac922c4ba53a30e8e485d3210acc62b7d4bd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310236"
---
# <a name="xlautoclose"></a>xlAutoClose

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Вызывается приложением Microsoft Excel при каждом отключении XLL. Надстройка отключается после нормального завершения сеанса Excel. Надстройку может отключить пользователь во время сеанса Excel, что также потянет за собой вызов этой функции.
  
Для внедрения и экспорта этой функции в приложении Excel надстройка XLL не обязательна, но рекомендована: с помощью XLL можно отключать функции и команды, освобождать ресурсы, отменять настройки и т. д. Если надстройка XLL не отключает функции и команды явным образом, это делает Excel после вызова функции **xlAutoClose**. 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a>Параметры

Эта функция не получает никаких аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Внедрении этой функции должно возвратить значение 1 (**int**).
  
## <a name="remarks"></a>Замечания

Excel вызывает функцию **xlAutoClose** каждый раз, когда надстройка XLL отключается (то есть выгружается из памяти). Надстройка XLL отключается в перечисленных ниже ситуациях: 
  
- При нормальном завершении сеанса Excel, во время которого она была активна.
    
- Если она была явным образом выгружена из памяти во время сеанса Excel.
    
- XLL может выгружаться несколькими способами:
    
- С помощью диспетчера надстроек.
    
- Из другой надстройки XLL, которая вызывает [xlfUnregister](xlfunregister-form-1.md), указывая имя этой библиотеки DLL в качестве единственного аргумента. 
    
- Из макроса XLM, который вызывает [UNREGISTER](xlfunregister-form-1.md), указывая имя этой библиотеки DLL в качестве единственного аргумента. 
    
Эта функция должна выполнять следующее:
  
- Удалять меню или элементы меню, которые были добавлены надстройкой XLL.
    
- В случае надобности выполнять любую глобальную очистку.
    
- Удалять какие-либо созданные имена, в частности имена экспортированных функций. Помните, что регистрация функций может привести к созданию некоторых имен, если присутствует четвертый аргумент для **РЕГИСТРАЦИИ**. 
    
## <a name="example"></a>Пример

В файлах `SAMPLES\EXAMPLE\EXAMPLE.C` и `SAMPLES\GENERIC\GENERIC.C` приведены примеры внедрения этой функции. Следующий код — из файла `SAMPLES\GENERIC\GENERIC.C`.
  
```cs
int WINAPI xlAutoClose(void)
{
   int i;
   XLOPER12 xRes;
//
// This block first deletes all names added by xlAutoOpen or
// xlAutoRegister12. Next, it checks if the drop-down menu Generic still
// exists. If it does, it is deleted using xlfDeleteMenu. It then checks
// if the Test toolbar still exists. If it is, xlfDeleteToolbar is
// used to delete it.
//
// The following code to delete the defined names
// does not work in the current version of Excel. 
// You cannot delete these names once they are Registered.
// The code is left here in case the functionality becomes 
// available in a future version.
//
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgWorksheetFuncs[i][2]));
   for (i = 0; i < g_rgCommandFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgCommandFuncs[i][2]));
//
// Everything else works as documented.
//
   Excel12f(xlfGetBar, &amp;xRes, 3, TempInt12(10), TempStr12(L"Generic"), TempInt12(0));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteMenu, 0, 2, TempNum12(10), TempStr12(L"Generic"));
      // Free the XLOPER12 returned by xlfGetBar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   Excel12f(xlfGetToolbar, &amp;xRes, 2, TempInt12(7), TempStr12(L"Test"));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteToolbar, 0, 1, TempStr12(L"Test"));
      // Free the XLOPER12 returned by xlfGetToolbar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   return 1;
}
```

## <a name="see-also"></a>См. также



[xlAutoOpen](xlautoopen.md)


[Функции диспетчера надстроек и интерфейса XLL](add-in-manager-and-xll-interface-functions.md)

