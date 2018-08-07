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
# <a name="calling-user-defined-functions-from-dlls"></a><span data-ttu-id="fe84c-104">Вызов пользовательских функций из библиотек DLL</span><span class="sxs-lookup"><span data-stu-id="fe84c-104">Calling user-defined functions from DLLs</span></span>

<span data-ttu-id="fe84c-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fe84c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fe84c-106">Вызов пользовательских функций (UDF) из листа сложнее, чем вызов встроенных функций: введите функцию через Формула ячейки.</span><span class="sxs-lookup"><span data-stu-id="fe84c-106">Calling user-defined functions (UDFs) from a worksheet is as simple as calling built-in functions: You enter the function via a cell formula.</span></span> <span data-ttu-id="fe84c-107">Однако из интерфейса API C, ни один из кодов предварительно определенные функции для использования с ответных звонков.</span><span class="sxs-lookup"><span data-stu-id="fe84c-107">However, from the C API, there are no pre-defined function codes to use with the call-backs.</span></span> <span data-ttu-id="fe84c-108">Чтобы можно было вызывать пользовательские функции, интерфейса API для C экспортирует функцию только XLL, функция [xlUDF](xludf.md) .</span><span class="sxs-lookup"><span data-stu-id="fe84c-108">To enable you to call UDFs, the C API exports an XLL-only function, the [xlUDF ](xludf.md) function.</span></span> <span data-ttu-id="fe84c-109">Первый аргумент функции — это имя функции как строку и последующие аргументы — это списки, будет выполняться пользовательские функции.</span><span class="sxs-lookup"><span data-stu-id="fe84c-109">The function's first argument is the function name as a string, and subsequent arguments are those that the UDF would normally expect.</span></span> 
  
<span data-ttu-id="fe84c-110">Список зарегистрированных в настоящее время функции XLL и команды можно получить с помощью функции **xlfGetWorkspace** с аргументом 44.</span><span class="sxs-lookup"><span data-stu-id="fe84c-110">You can obtain a list of the currently registered XLL add-in functions and commands by using the **xlfGetWorkspace** function with the argument 44.</span></span> <span data-ttu-id="fe84c-111">Возвращает массив трех столбцов которых представлены следующие столбцы:</span><span class="sxs-lookup"><span data-stu-id="fe84c-111">This returns a three-column array where the columns represent the following:</span></span> 
  
- <span data-ttu-id="fe84c-112">Полный путь и имя XLL</span><span class="sxs-lookup"><span data-stu-id="fe84c-112">The full path and name of the XLL</span></span>
    
- <span data-ttu-id="fe84c-113">Имя UDF или команды, как экспортировать из XLL</span><span class="sxs-lookup"><span data-stu-id="fe84c-113">The name of the UDF or command as exported from the XLL</span></span>
    
- <span data-ttu-id="fe84c-114">Строка кода возврата и аргумент</span><span class="sxs-lookup"><span data-stu-id="fe84c-114">The return and argument code string</span></span>
    
> [!NOTE]
> <span data-ttu-id="fe84c-115">Имя, экспортированные из XLL не может совпадать зарегистрированное имя, с помощью которого Excel знает команду или пользовательских Функций.</span><span class="sxs-lookup"><span data-stu-id="fe84c-115">The name as exported from the XLL might not be the same as the registered name by which Excel knows the UDF or command.</span></span> 
  
<span data-ttu-id="fe84c-116">Начиная с версии Excel 2007, полностью интегрированы функции анализа ПАКЕТА и интерфейса API для C имеет свой собственный перечисления для функции, такие как цена, **xlfPrice**.</span><span class="sxs-lookup"><span data-stu-id="fe84c-116">Starting in Excel 2007, the Analysis Toolpak (ATP) functions are fully integrated, and the C API has its own enumerations for functions such as PRICE, **xlfPrice**.</span></span> <span data-ttu-id="fe84c-117">В более ранних версиях приходилось использовать **xlUDF** для вызова этих функций.</span><span class="sxs-lookup"><span data-stu-id="fe84c-117">In earlier versions, you had to use **xlUDF** to call these functions.</span></span> <span data-ttu-id="fe84c-118">Если надстройка необходим для работы с Excel 2003 и Excel 2007 или более поздней версии, и использует эти функции, следует определить текущую версию и вызовите функцию, как соответствующий.</span><span class="sxs-lookup"><span data-stu-id="fe84c-118">If your add-in needs to work with Excel 2003 and Excel 2007 or later versions, and it uses these functions, you should detect the current version and call the function in the appropriate way.</span></span> 
  
## <a name="examples"></a><span data-ttu-id="fe84c-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="fe84c-119">Examples</span></span>

<span data-ttu-id="fe84c-120">Следующий пример показывает функцию **xlUDF** используется для вызова функции анализа **Цена** при используемой версии Excel 2003 или более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="fe84c-120">The following example shows the **xlUDF** function being used to call the ATP function **PRICE** when the running version of Excel is 2003 or earlier.</span></span> <span data-ttu-id="fe84c-121">Сведения о настройке глобальных версия переменной, такие как **gExcelVersion12plus** в этом примере [Обратной совместимости](backward-compatibility.md)см.</span><span class="sxs-lookup"><span data-stu-id="fe84c-121">For information about the setting of a global version variable, such as **gExcelVersion12plus** in this example, see [Backward Compatibility](backward-compatibility.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="fe84c-122">В этом примере с помощью функции Framework **TempNum** **TempStrConst** для настройки аргументов и Excel для вызова интерфейса API для C.</span><span class="sxs-lookup"><span data-stu-id="fe84c-122">This example uses the Framework functions **TempNum**, **TempStrConst** to set up the arguments and Excel to call the C API.</span></span> 
  
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

<span data-ttu-id="fe84c-123">Где вызов функции XLL, которое возвращает значение путем изменения аргумента на месте, функция **xlUDF** по-прежнему возвращает значение по адресу результатов **XLOPER и XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="fe84c-123">Where you are calling an XLL function that returns a value by modifying an argument in place, the **xlUDF** function still returns the value via the address of the result **XLOPER/XLOPER12**.</span></span> <span data-ttu-id="fe84c-124">Другими словами как если бы через обычный оператор return возвращается результат.</span><span class="sxs-lookup"><span data-stu-id="fe84c-124">In other words, the result is returned as if through a normal return statement.</span></span> <span data-ttu-id="fe84c-125">**XLOPER и XLOPER12** , соответствующий аргумент, который используется для возврата значения не изменяется.</span><span class="sxs-lookup"><span data-stu-id="fe84c-125">The **XLOPER/XLOPER12** that corresponds to the argument that is used for the return value is unmodified.</span></span> <span data-ttu-id="fe84c-126">Например рассмотрим следующие два пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="fe84c-126">For example, consider the following two UDFs.</span></span> 
  
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

<span data-ttu-id="fe84c-127">При **UDF\_2** вызовы **UDF\_1**, значение **pxArg** не изменяется после вызова **Excel12**и значение, возвращаемое **UDF_1** содержится в **xRetVal**.</span><span class="sxs-lookup"><span data-stu-id="fe84c-127">When **UDF\_2** calls **UDF\_1**, the value of **pxArg** is unchanged after the call to **Excel12**, and the value returned by **UDF_1** is contained in **xRetVal**.</span></span>
  
<span data-ttu-id="fe84c-128">При создании большое число звонков на пользовательской функции таким образом, можно оценить имя функции с помощью [функции xlfEvaluate](xlfevaluate.md).</span><span class="sxs-lookup"><span data-stu-id="fe84c-128">When you are making a large number of calls to a UDF in this way, you can evaluate the function name first by using the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="fe84c-129">Итоговый номер, который имеет то же, что код регистрации, который возвращается функцией **xlfRegister** , может быть передан вместо имени функции в качестве первого аргумента функции **xlUDF** .</span><span class="sxs-lookup"><span data-stu-id="fe84c-129">The resulting number, which is the same as the registration ID that is returned by the **xlfRegister** function, can be passed in place of the function name as the first argument to the **xlUDF** function.</span></span> <span data-ttu-id="fe84c-130">Это позволяет Excel для поиска и быстрее, чем если есть для поиска имени функции каждый раз при вызове функции.</span><span class="sxs-lookup"><span data-stu-id="fe84c-130">This enables Excel to find and call the function more quickly than if it has to look up the function name every time.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fe84c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="fe84c-131">See also</span></span>

- [<span data-ttu-id="fe84c-132">Разрешение прерывания длительных операций пользователем</span><span class="sxs-lookup"><span data-stu-id="fe84c-132">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="fe84c-133">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="fe84c-133">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [<span data-ttu-id="fe84c-134">Начало работы с пакетом SDK XLL для Excel</span><span class="sxs-lookup"><span data-stu-id="fe84c-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

