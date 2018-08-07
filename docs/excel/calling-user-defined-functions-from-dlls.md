---
title: Вызов пользовательских функций из библиотек DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- пользовательские функции [excel 2007], вызов из библиотеки DLL, определяемых пользователем функций [Excel 2007], вызов из библиотеки DLL, вызов пользовательских функций библиотеки DLL [Excel 2007]
localization_priority: Normal
ms.assetid: 99a37108-0083-4240-9c6a-3afa8d7a04f6
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4e893cf1e54489610315dd5c5d57bd78c3c936d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807153"
---
# <a name="calling-user-defined-functions-from-dlls"></a>Вызов пользовательских функций из библиотек DLL

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Вызов пользовательских функций (UDF) из листа сложнее, чем вызов встроенных функций: введите функцию через Формула ячейки. Однако из интерфейса API C, ни один из кодов предварительно определенные функции для использования с ответных звонков. Чтобы можно было вызывать пользовательские функции, интерфейса API для C экспортирует функцию только XLL, функция [xlUDF](xludf.md) . Первый аргумент функции — это имя функции как строку и последующие аргументы — это списки, будет выполняться пользовательские функции. 
  
Список зарегистрированных в настоящее время функции XLL и команды можно получить с помощью функции **xlfGetWorkspace** с аргументом 44. Возвращает массив трех столбцов которых представлены следующие столбцы: 
  
- Полный путь и имя XLL
    
- Имя UDF или команды, как экспортировать из XLL
    
- Строка кода возврата и аргумент
    
> [!NOTE]
> Имя, экспортированные из XLL не может совпадать зарегистрированное имя, с помощью которого Excel знает команду или пользовательских Функций. 
  
Начиная с версии Excel 2007, полностью интегрированы функции анализа ПАКЕТА и интерфейса API для C имеет свой собственный перечисления для функции, такие как цена, **xlfPrice**. В более ранних версиях приходилось использовать **xlUDF** для вызова этих функций. Если надстройка необходим для работы с Excel 2003 и Excel 2007 или более поздней версии, и использует эти функции, следует определить текущую версию и вызовите функцию, как соответствующий. 
  
## <a name="examples"></a>Примеры

Следующий пример показывает функцию **xlUDF** используется для вызова функции анализа **Цена** при используемой версии Excel 2003 или более ранних версий. Сведения о настройке глобальных версия переменной, такие как **gExcelVersion12plus** в этом примере [Обратной совместимости](backward-compatibility.md)см.
  
> [!NOTE]
> В этом примере с помощью функции Framework **TempNum** **TempStrConst** для настройки аргументов и Excel для вызова интерфейса API для C. 
  
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

Где вызов функции XLL, которое возвращает значение путем изменения аргумента на месте, функция **xlUDF** по-прежнему возвращает значение по адресу результатов **XLOPER и XLOPER12**. Другими словами как если бы через обычный оператор return возвращается результат. **XLOPER и XLOPER12** , соответствующий аргумент, который используется для возврата значения не изменяется. Например рассмотрим следующие два пользовательских функций. 
  
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

При **UDF\_2** вызовы **UDF\_1**, значение **pxArg** не изменяется после вызова **Excel12**и значение, возвращаемое **UDF_1** содержится в **xRetVal**.
  
При создании большое число звонков на пользовательской функции таким образом, можно оценить имя функции с помощью [функции xlfEvaluate](xlfevaluate.md). Итоговый номер, который имеет то же, что код регистрации, который возвращается функцией **xlfRegister** , может быть передан вместо имени функции в качестве первого аргумента функции **xlUDF** . Это позволяет Excel для поиска и быстрее, чем если есть для поиска имени функции каждый раз при вызове функции. 
  
## <a name="see-also"></a>См. также

- [Разрешение прерывания длительных операций пользователем](permitting-user-breaks-in-lengthy-operations.md)
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [Начало работы с пакетом SDK XLL для Excel](getting-started-with-the-excel-xll-sdk.md)

