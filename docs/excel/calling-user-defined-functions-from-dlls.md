---
title: Вызов пользовательских функций из библиотек DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- udfs [excel 2007], вызовы из DLL, пользовательские функции [Excel 2007], вызовы из DLL,DLL [Excel 2007], вызов пользовательских функций
localization_priority: Normal
ms.assetid: 99a37108-0083-4240-9c6a-3afa8d7a04f6
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9e2ca3f4485fb41c5ab6a48f323b4c0093e747e4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417947"
---
# <a name="calling-user-defined-functions-from-dlls"></a>Вызов пользовательских функций из библиотек DLL

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Вызов пользовательских функций (UDF) с электронного таблицы так же прост, как вызов встроенных функций: вы вводите функцию с помощью формулы ячейки. Однако из API C не существует заранее определенных кодов функций для использования с ответными вызовами. Чтобы вы могли вызывать функции UDF, API C экспортирует функцию только XLL, [функцию xlUDF.](xludf.md) Первый аргумент функции — это имя функции в качестве строки, а последующие аргументы — это аргументы, которые обычно ожидаются UDF. 
  
Список зарегистрированных в настоящее время функций и команд надстройки XLL можно получить с помощью функции **xlfGetWorkspace** с аргументом 44. При этом возвращается массив из трех столбцов, в котором столбцы представляют следующее: 
  
- Полный путь и имя XLL
    
- Имя UDF или команды, экспортируемой из XLL
    
- Строка кода возврата и аргумента
    
> [!NOTE]
> Имя, экспортируемая из XLL, может быть не таким, как зарегистрированное имя, по которому Excel знает UDF или команду. 
  
Начиная с Excel 2007 функции анализа toolpak (ATP) полностью интегрированы, а API C имеет собственные нумерации для таких функций, как PRICE, **xlfPrice**. В более ранних версиях для вызова этих функций приходилось использовать **xlUDF.** Если надстройка должна работать с Excel 2003 и Excel 2007 или более поздними версиями и использует эти функции, следует определить текущую версию и вызвать функцию соответствующим образом. 
  
## <a name="examples"></a>Примеры

В следующем примере показана функция **xlUDF,** используемая для вызова функции ATP **PRICE,** если запущена версия Excel 2003 или более ранней. Сведения о настройке глобальной переменной версии, например **gExcelVersion12plus** в этом примере, см. в подразце ["Обратная совместимость".](backward-compatibility.md)
  
> [!NOTE]
> В этом примере используются функции **Framework TempNum**, **TempStrConst,** чтобы настроить аргументы, и Excel для вызова API C. 
  
```C
LPXLOPER TempNum(double d);
LPXLOPER TempStrConst(const LPSTR lpstr);
int cdecl Excel(int xlfn, LPXLOPER pxResult, int count, ...);
double call_ATP_example(void)
{
  XLOPER xPrice;
  int xl_ret_val;
  if(gExcelVersion12plus) // Starting in Excel 2007
  {
    xl_ret_val = Excel(xlfPrice, &xPrice, 7,
      TempNum(39084.0), // settlement date 2-Jan-2007
      TempNum(46706.0), // maturity date 15-Nov-2027
      TempNum(0.04), // Coupon
      TempNum(0.05), // Yield
      TempNum(1.0), // redemption value: 100% of face
      TempNum(1.0), // Annual coupons
      TempNum(1.0)); // Rate basis Act/Act
  }
  else // Excel 2003-
  {
    xl_ret_val = Excel(xlUDF, &xPrice, 8,
      TempStrConst("PRICE"),
      TempNum(39084.0), // settlement date 2-Jan-2007
      TempNum(46706.0), // maturity date 15-Nov-2027
      TempNum(0.04), // Coupon
      TempNum(0.05), // Yield
      TempNum(1.0), // redepmtion value: 100% of face
      TempNum(1.0), // Annual coupons
      TempNum(1.0)); // Rate basis Act/Act
  }
  if(xl_ret_val != xlretSuccess || xPrice.xltype != xltypeNum)
  {
// Even though PRICE is not expected to return a string, there
// is no harm in freeing the XLOPER to be safe
    Excel(xlFree, 0, 1, &xPrice);
    return -1.0; // an error value
  }
  return xPrice.val.num;
}
```

<br/>

При вызове функции XLL, которая возвращает значение путем изменения аргумента на месте, функция **xlUDF** по-прежнему возвращает значение через адрес результата **XLOPER/XLOPER12**. Другими словами, результат возвращается как если бы с помощью обычного возвращаемого утверждения. **XLOPER/XLOPER12, соответствующий** аргументу, который используется для возвращаемой величины, неизмен. Например, рассмотрим следующие две UDF. 
  
```C
// Registered as "1E". Returns its argument incremented by 1.
void WINAPI UDF_1(double *pArg)
{
  *pArg += 1.0;
}
// Registered as "QQ". Returns its argument unmodified
// unless it is a number, in which case it increments it
// by calling UDF_1.
LPXLOPER12 WINAPI UDF_2(LPXLOPER12 pxArg)
{
  static XLOPER12 xRetVal; // Not thread-safe
  XLOPER12 xFn;
  xFn.xltype = xltypeStr;
  xFn.val.str = L"\005UDF_1";
  Excel12(xlUDF, &xRetVal, 2, &xFn, pxArg);
  xRetVal.xltype |= xlbitXLFree;
  return &xRetVal;
}
```

Когда **UDF \_ 2** вызывает **UDF \_ 1,** значение **pxArg** не изменяется после вызова **Excel12,** а значение, возвращаемого UDF_1, содержится в **xRetVal**. 
  
При таком вызове большого количества вызовов UDF можно сначала оценить имя функции с помощью функции [xlfEvaluate.](xlfevaluate.md) Итоговая цифра, которая является таким же, как и ИД регистрации, возвращаемой функцией **xlfRegister,** может быть передана в качестве первого аргумента функции **xlUDF.** Это позволяет Excel быстрее находить и вызывать функцию, чем при каждом поиске имени функции. 
  
## <a name="see-also"></a>См. также

- [Разрешение прерывания длительных операций пользователем](permitting-user-breaks-in-lengthy-operations.md)
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [Начало работы с пакетом SDK XLL для Excel](getting-started-with-the-excel-xll-sdk.md)

