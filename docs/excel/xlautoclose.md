---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- функция xlAutoClose [excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3cbe1cd879fb5a91d14b38f8a659a7f77d943fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807354"
---
# <a name="xlautoclose"></a>xlAutoClose

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
При отключении XLL вызывается Microsoft Excel. Надстройка отключается при завершении сеанса Excel обычно. Надстройка может быть отключена пользователем во время сеанса обмена Excel, и эта функция будет вызываться в этом случае.
  
Excel не требуется XLL внедрение и экспорт этой функции, хотя рекомендуется, чтобы вашей XLL можно отменить регистрацию функций и команд, освобождения ресурсов, отменить настроек и т.д. Если функции и команды не отменена явным образом, XLL, Excel выполняется после вызова функции **xlAutoClose** . 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a>Parameters

Эта функция не имеет аргументов.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Реализация этой функции необходимо вернуть 1 (**int**).
  
## <a name="remarks"></a>Замечания

Excel вызывает функцию **xlAutoClose** при XLL отключена, то есть, выгружать из памяти. XLL деактивирован в следующих ситуациях: 
  
- В конце обычный сеанс Excel при активной во время этого сеанса.
    
- Если явно выгружен во время сеанса обмена Excel.
    
- XLL-модуль можно выгрузить несколькими способами:
    
- Использование диспетчера надстроек.
    
- Из другой XLL, который вызывает [xlfUnregister](xlfunregister-form-1.md) с именем Эта DLL-Библиотека только в качестве аргумента. 
    
- Из таблицы макросов XLM, который вызывает [Отменить РЕГИСТРАЦИЮ](xlfunregister-form-1.md) с именем Эта DLL-Библиотека только в качестве аргумента. 
    
Эта функция должна выполните следующее:
  
- Удалите все меню и пунктов меню, которые были добавлены, XLL.
    
- Выполните необходимую очистку глобальные.
    
- Удалите имена, которые были созданы, особенно имена экспортированных функций. Имейте в виду, что регистрация функций может стать причиной некоторые имена, чтобы создать, если присутствует аргумент четвертая для **регистрации** . 
    
## <a name="example"></a>Пример

Файлы `SAMPLES\EXAMPLE\EXAMPLE.C` и `SAMPLES\GENERIC\GENERIC.C` для примера реализации этой функции. Следующий код является из `SAMPLES\GENERIC\GENERIC.C`.
  
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


[Диспетчер надстроек и функции XLL интерфейса](add-in-manager-and-xll-interface-functions.md)

