---
title: Вызов пользовательских функций из библиотек DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- udfs [Excel 2007], вызовы из dlls,пользовательских функций [Excel 2007], вызов из DLLs,DLLs [Excel 2007], вызов UDFs
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
# <a name="calling-user-defined-functions-from-dlls"></a><span data-ttu-id="ce2f3-104">Вызов пользовательских функций из библиотек DLL</span><span class="sxs-lookup"><span data-stu-id="ce2f3-104">Calling user-defined functions from DLLs</span></span>

<span data-ttu-id="ce2f3-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ce2f3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ce2f3-106">Вызов пользовательских функций (UDF) из таблицы так же прост, как вызов встроенных функций: вы вводите функцию с помощью формулы ячейки.</span><span class="sxs-lookup"><span data-stu-id="ce2f3-106">Calling user-defined functions (UDFs) from a worksheet is as simple as calling built-in functions: You enter the function via a cell formula.</span></span> <span data-ttu-id="ce2f3-107">Однако из API C не существует заранее определенных кодов функций, которые можно использовать с обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ce2f3-107">However, from the C API, there are no pre-defined function codes to use with the call-backs.</span></span> <span data-ttu-id="ce2f3-108">Чтобы вы могли вызывать UDF, API C экспортирует функцию только XLL — [функцию xlUDF.](xludf.md)</span><span class="sxs-lookup"><span data-stu-id="ce2f3-108">To enable you to call UDFs, the C API exports an XLL-only function, the [xlUDF ](xludf.md) function.</span></span> <span data-ttu-id="ce2f3-109">Первым аргументом функции является имя функции в качестве строки, а последующие аргументы — те, которые обычно ожидаются UDF.</span><span class="sxs-lookup"><span data-stu-id="ce2f3-109">The function's first argument is the function name as a string, and subsequent arguments are those that the UDF would normally expect.</span></span> 
  
<span data-ttu-id="ce2f3-110">Список зарегистрированных в настоящее время функций и команд надстройки XLL можно получить с помощью **функции xlfGetWorkspace** с аргументом 44.</span><span class="sxs-lookup"><span data-stu-id="ce2f3-110">You can obtain a list of the currently registered XLL add-in functions and commands by using the **xlfGetWorkspace** function with the argument 44.</span></span> <span data-ttu-id="ce2f3-111">Это возвращает массив из трех столбцов, в котором столбцы представляют следующие:</span><span class="sxs-lookup"><span data-stu-id="ce2f3-111">This returns a three-column array where the columns represent the following:</span></span> 
  
- <span data-ttu-id="ce2f3-112">Полный путь и имя XLL</span><span class="sxs-lookup"><span data-stu-id="ce2f3-112">The full path and name of the XLL</span></span>
    
- <span data-ttu-id="ce2f3-113">Имя UDF или команды, экспортируемой из XLL</span><span class="sxs-lookup"><span data-stu-id="ce2f3-113">The name of the UDF or command as exported from the XLL</span></span>
    
- <span data-ttu-id="ce2f3-114">Строка кода возврата и аргументов</span><span class="sxs-lookup"><span data-stu-id="ce2f3-114">The return and argument code string</span></span>
    
> [!NOTE]
> <span data-ttu-id="ce2f3-115">Имя, экспортируемая из XLL, может быть не таким, как зарегистрированное имя, Excel знает UDF или команду.</span><span class="sxs-lookup"><span data-stu-id="ce2f3-115">The name as exported from the XLL might not be the same as the registered name by which Excel knows the UDF or command.</span></span> 
  
<span data-ttu-id="ce2f3-116">Начиная с Excel 2007 г. функции Analysis Toolpak (ATP) полностью интегрированы, а API C имеет свои собственные перемеры для таких функций, как PRICE, **xlfPrice**.</span><span class="sxs-lookup"><span data-stu-id="ce2f3-116">Starting in Excel 2007, the Analysis Toolpak (ATP) functions are fully integrated, and the C API has its own enumerations for functions such as PRICE, **xlfPrice**.</span></span> <span data-ttu-id="ce2f3-117">В более ранних версиях для вызова этих функций приходилось использовать **xlUDF.**</span><span class="sxs-lookup"><span data-stu-id="ce2f3-117">In earlier versions, you had to use **xlUDF** to call these functions.</span></span> <span data-ttu-id="ce2f3-118">Если надстройка должна работать с Excel 2003 и Excel 2007 или более поздних версий, и она использует эти функции, необходимо определить текущую версию и вызвать функцию соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="ce2f3-118">If your add-in needs to work with Excel 2003 and Excel 2007 or later versions, and it uses these functions, you should detect the current version and call the function in the appropriate way.</span></span> 
  
## <a name="examples"></a><span data-ttu-id="ce2f3-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="ce2f3-119">Examples</span></span>

<span data-ttu-id="ce2f3-120">В следующем примере показана функция **xlUDF,**  используемая для вызова цены функции ATP, когда запущенная версия Excel 2003 или более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="ce2f3-120">The following example shows the **xlUDF** function being used to call the ATP function **PRICE** when the running version of Excel is 2003 or earlier.</span></span> <span data-ttu-id="ce2f3-121">Сведения о настройке глобальной переменной версии, например **gExcelVersion12plus** в этом примере, см. в таблице [Backward Compatibility.](backward-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="ce2f3-121">For information about the setting of a global version variable, such as **gExcelVersion12plus** in this example, see [Backward Compatibility](backward-compatibility.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="ce2f3-122">В этом примере используются функции **Framework TempNum** и **TempStrConst,** чтобы настроить аргументы и Excel для вызова API C.</span><span class="sxs-lookup"><span data-stu-id="ce2f3-122">This example uses the Framework functions **TempNum**, **TempStrConst** to set up the arguments and Excel to call the C API.</span></span> 
  
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

<span data-ttu-id="ce2f3-123">Если вы вызываете функцию XLL, возвращаемую значение путем изменения аргумента на месте, функция **xlUDF** по-прежнему возвращает значение по адресу **результатов XLOPER/XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="ce2f3-123">Where you are calling an XLL function that returns a value by modifying an argument in place, the **xlUDF** function still returns the value via the address of the result **XLOPER/XLOPER12**.</span></span> <span data-ttu-id="ce2f3-124">Другими словами, результат возвращается как при обычном обратном заявлении.</span><span class="sxs-lookup"><span data-stu-id="ce2f3-124">In other words, the result is returned as if through a normal return statement.</span></span> <span data-ttu-id="ce2f3-125">**XLOPER/XLOPER12,** соответствующий аргументу, который используется для возврата, неизменен.</span><span class="sxs-lookup"><span data-stu-id="ce2f3-125">The **XLOPER/XLOPER12** that corresponds to the argument that is used for the return value is unmodified.</span></span> <span data-ttu-id="ce2f3-126">Например, рассмотрим следующие два UDF.</span><span class="sxs-lookup"><span data-stu-id="ce2f3-126">For example, consider the following two UDFs.</span></span> 
  
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

<span data-ttu-id="ce2f3-127">Когда **UDF \_ 2** вызывает **UDF \_ 1,** значение **pxArg** после вызова **в Excel12** не  меняется, а возвращаемая UDF_1 содержится в **xRetVal**.</span><span class="sxs-lookup"><span data-stu-id="ce2f3-127">When **UDF\_2** calls **UDF\_1**, the value of **pxArg** is unchanged after the call to **Excel12**, and the value returned by **UDF_1** is contained in **xRetVal**.</span></span>
  
<span data-ttu-id="ce2f3-128">При таком большом количестве вызовов в UDF можно сначала оценить имя функции с помощью [функции xlfEvaluate.](xlfevaluate.md)</span><span class="sxs-lookup"><span data-stu-id="ce2f3-128">When you are making a large number of calls to a UDF in this way, you can evaluate the function name first by using the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="ce2f3-129">В качестве первого аргумента в функцию xlUDF можно передать в качестве первого аргумента в пользу функции **xlUDF** результативный номер, который является таким же, как и регистрационный ID, возвращаемой функцией **xlfRegister.**</span><span class="sxs-lookup"><span data-stu-id="ce2f3-129">The resulting number, which is the same as the registration ID that is returned by the **xlfRegister** function, can be passed in place of the function name as the first argument to the **xlUDF** function.</span></span> <span data-ttu-id="ce2f3-130">Это позволяет Excel и вызывать функцию быстрее, чем при каждом поиске имени функции.</span><span class="sxs-lookup"><span data-stu-id="ce2f3-130">This enables Excel to find and call the function more quickly than if it has to look up the function name every time.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ce2f3-131">См. также</span><span class="sxs-lookup"><span data-stu-id="ce2f3-131">See also</span></span>

- [<span data-ttu-id="ce2f3-132">Разрешение прерывания длительных операций пользователем</span><span class="sxs-lookup"><span data-stu-id="ce2f3-132">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="ce2f3-133">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="ce2f3-133">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [<span data-ttu-id="ce2f3-134">Начало работы с пакетом SDK XLL для Excel</span><span class="sxs-lookup"><span data-stu-id="ce2f3-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

