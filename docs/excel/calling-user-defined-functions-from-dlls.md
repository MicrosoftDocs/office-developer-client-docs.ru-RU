---
title: Вызов пользовательских функций из библиотек DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- UDF [Excel 2007], вызов из библиотек DLL, пользовательские функции [Excel 2007], вызов из библиотек DLL, библиотеки DLL [Excel 2007], вызов пользовательских функций
localization_priority: Normal
ms.assetid: 99a37108-0083-4240-9c6a-3afa8d7a04f6
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9e2ca3f4485fb41c5ab6a48f323b4c0093e747e4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301647"
---
# <a name="calling-user-defined-functions-from-dlls"></a>Вызов пользовательских функций из библиотек DLL

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Вызов пользовательских функций из листа выполняется так же, как вызов встроенных функций: вы вводите функцию с помощью формулы ячейки. Однако из API C нет предварительно определенных кодов функций, которые можно использовать для обратного вызова. Чтобы разрешить вызов пользовательских функций, API C экспортирует функцию-только XLL, функцию [xlUDF](xludf.md) . Первый аргумент функции — это имя функции в виде строки, а последующие аргументы — те, которые обычно задерживает UDF. 
  
Список зарегистрированных в настоящее время функций и команд XLL можно получить с помощью функции **кслфжетворкспаце** с аргументом 44. Возвращает массив из трех столбцов, в котором представлены следующие столбцы: 
  
- Полный путь и имя XLL
    
- Имя UDF или команды, экспортированные из XLL
    
- Строка кода возврата и аргумента
    
> [!NOTE]
> Имя, экспортированное из XLL, может отличаться от зарегистрированного имени, в соответствии с которым Excel знает команду UDF или команду. 
  
Начиная с Excel 2007, функции пакета анализа полностью интегрированы, а API C имеют собственные перечисления для таких функций, как PRICE, **кслфприце**. В более ранних версиях для вызова этих функций необходимо было использовать **xlUDF** . Если надстройка должна работать с Excel 2003 и Excel 2007 или более поздней версии, и использует эти функции, необходимо обнаружить текущую версию и вызвать функцию соответствующим образом. 
  
## <a name="examples"></a>Примеры

В приведенном ниже примере показана функция **xlUDF** , используемая для вызова **цены** функции ATP, когда запущенная версия Excel — 2003 или более ранняя. Сведения о параметрах глобальной переменной версии, например **gExcelVersion12plus** в этом примере, приведены в статье Обратная [Совместимость](backward-compatibility.md).
  
> [!NOTE]
> В этом примере используются функции платформы **темпнум**, **темпстрконст** для настройки аргументов и Excel для вызова API C. 
  
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

Когда вы вызываете функцию XLL, возвращающую значение, изменяя аргумент на месте, функция **xlUDF** по-прежнему возвращает значение через адрес результата **XLOPER/XLOPER12**. Другими словами, результат возвращается как если бы через обычный оператор return. **XLOPER/XLOPER12** , соответствующие аргументу, используемому для возвращаемого значения, не изменено. Например, рассмотрим следующие две функции UDF. 
  
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

Когда **UDF\_2** вызывает **UDF\_1**, значение **пксарг** не изменяется после вызова в **Excel12**, а возвращаемое значение **UDF_1** содержаться в **ксретвал**.
  
Когда вы выполняете большое количество вызовов в UDF таким образом, вы можете сначала оценить имя функции с помощью [функции xlfEvaluate](xlfevaluate.md). Полученный в результате этого номер, который совпадает с ИДЕНТИФИКАТОРом регистрации, возвращаемым функцией **xlfRegister** , можно передать вместо имени функции в качестве первого аргумента функции **xlUDF** . Это позволяет Excel находить и вызывать функцию быстрее, чем при каждом поиске имени функции. 
  
## <a name="see-also"></a>См. также

- [Разрешение прерывания длительных операций пользователем](permitting-user-breaks-in-lengthy-operations.md)
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [Начало работы с пакетом SDK XLL для Excel](getting-started-with-the-excel-xll-sdk.md)

