---
title: Вызов Excel из библиотеки DLL или XLL
manager: soliver
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- диалоговые окна [excel 2007], вызов команд excel, библиотеки DLL [Excel 2007], вызов Excel, передача аргументов функции API C [Excel 2007], команды [Excel 2007], вызов в диалоговых окнах, команды [Excel 2007], предоставление доступа из DLL или XLL, функция Excel4, функция Excel12 [Excel 2007], функция XLCallVer [Excel 2007], аргумент operRes [Excel 2007], [Excel 2007], функции [Excel 2007], доступ из DLL или XLL, функция Excel12v [Excel 2007], функции только для DLL [Excel 2007], API C [Excel 2007], передача аргументов, аргумент счета [Excel 2007], команды [Excel 2007], вызовы в международных версиях, команды только для DLL [Excel 2007], международные версии [Excel 2007], вызовы функций и команд, XLL [Excel 2007], вызовы в Excel, функция 4v Excel [Excel 2007], аргумент xlfn [Excel 2007], функции [Excel 2007], вызовы в международных версиях
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 8f2b63ba84b0a78bbf317c284913a8ec0986436f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726122"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a><span data-ttu-id="dc954-104">Вызов Excel из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="dc954-104">Calling into Excel from the DLL or XLL</span></span>

<span data-ttu-id="dc954-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="dc954-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="dc954-106">Microsoft Excel позволяет DLL получить доступ к встроенным командам Excel, функциям листов и функциям листа макросов.</span><span class="sxs-lookup"><span data-stu-id="dc954-106">Microsoft Excel enables your DLL to access built-in Excel commands, worksheet functions, and macro sheet functions.</span></span> <span data-ttu-id="dc954-107">Они доступны как из команд и функций DLL, вызываемых из Visual Basic для приложений (VBA), так и из зарегистрированных команд и функций XLL, вызываемых непосредственно в Excel.</span><span class="sxs-lookup"><span data-stu-id="dc954-107">These are available both from DLL commands and functions called from Visual Basic for Applications (VBA), and from registered XLL commands and functions called directly by Excel.</span></span>
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a><span data-ttu-id="dc954-108">Функции Excel4, Excel4v, Excel12 и Excel12v</span><span class="sxs-lookup"><span data-stu-id="dc954-108">Excel4, Excel4v, Excel12, and Excel12v Functions</span></span>

<span data-ttu-id="dc954-109">Excel позволяет DLL получать доступ к командам и функциям через функции обратного вызова [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md) и [Excel12v](excel4v-excel12v.md).</span><span class="sxs-lookup"><span data-stu-id="dc954-109">Excel enables your DLL to access the commands and functions through the callback functions [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), and [Excel12v](excel4v-excel12v.md).</span></span>
  
<span data-ttu-id="dc954-110">Функции **Excel4** и **Excel4v** появились в версии Excel версии 4.</span><span class="sxs-lookup"><span data-stu-id="dc954-110">The **Excel4** and **Excel4v** functions were introduced in Excel version 4.</span></span> <span data-ttu-id="dc954-111">Они работают со структурой данных **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="dc954-111">They work with the **XLOPER** data structure.</span></span> <span data-ttu-id="dc954-112">В Excel 2007 появились две новые функции обратного вызова, **Excel12** и **Excel12v**, которые работают со структурой данных **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="dc954-112">Excel 2007 introduced two new callback functions, **Excel12** and **Excel12v**, which work with the **XLOPER12** data structure.</span></span> <span data-ttu-id="dc954-113">Функции **Excel4** и **Excel4v** экспортируются библиотекой Xlcall32.lib, которая должна быть включена в проект DLL или XLL.</span><span class="sxs-lookup"><span data-stu-id="dc954-113">The **Excel4** and **Excel4v** functions are exported by the library Xlcall32.lib, which must be included in your DLL or XLL project.</span></span> <span data-ttu-id="dc954-114">**Excel12** и **Excel12v** включены в исходный файл SDK C++ Xlcall.cpp, который должен быть в проекте, если вам нужен доступ к функциональным возможностям Excel с помощью структур **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="dc954-114">**Excel12** and **Excel12v** are included in the SDK C++ source file Xlcall.cpp, which must be included in your project if you want to access Excel functionality by using **XLOPER12** structures.</span></span> 
  
<span data-ttu-id="dc954-115">Приведенный ниже код отображает прототипы для этих четырех функций.</span><span class="sxs-lookup"><span data-stu-id="dc954-115">The following code shows the function prototypes for these four functions.</span></span> <span data-ttu-id="dc954-116">Первые три аргумента одинаковы с тем исключением, что второй аргумент является указателем на **XLOPER** в первой паре и указателем на **XLOPER12** во второй.</span><span class="sxs-lookup"><span data-stu-id="dc954-116">The first three arguments are the same except that the second argument is a pointer to an **XLOPER** in the first pair and a pointer to an **XLOPER12** in the second pair.</span></span> <span data-ttu-id="dc954-117">Соглашение о вызовах — **_cdecl** в **Excel4** и **Excel12** для разрешения списков переменных аргументов.</span><span class="sxs-lookup"><span data-stu-id="dc954-117">The calling convention is **_cdecl** in **Excel4** and **Excel12** to permit the variable argument lists.</span></span> <span data-ttu-id="dc954-118">Многоточие представляет указатели на значения **XLOPER** для **Excel4** и значения **XLOPER12** для **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="dc954-118">The ellipsis represents pointers to **XLOPER** values for **Excel4** and **XLOPER12** values for **Excel12**.</span></span> <span data-ttu-id="dc954-119">Количество указателей равно значению параметра _count_.</span><span class="sxs-lookup"><span data-stu-id="dc954-119">The number of pointers equals the value of the  _count_ parameter.</span></span> 
  
<span data-ttu-id="dc954-120">**Все версии Excel**</span><span class="sxs-lookup"><span data-stu-id="dc954-120">**All versions of Excel:**</span></span>
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
<span data-ttu-id="dc954-121">**Начиная с Excel 2007**</span><span class="sxs-lookup"><span data-stu-id="dc954-121">**(starting in Excel 2007)**</span></span>
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
<span data-ttu-id="dc954-122">Чтобы DLL могла вызвать **Excel4**, **Excel4v**, **Excel12** или **Excel12v**, приложение Excel должно передать управление библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="dc954-122">For the DLL to be able to call **Excel4**, **Excel4v**, **Excel12**, or **Excel12v**, Excel must pass control to the DLL.</span></span> <span data-ttu-id="dc954-123">Это означает, что обратные вызовы API C возможны только в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="dc954-123">This means that these C API callbacks can be called only in the following scenarios:</span></span>
  
- <span data-ttu-id="dc954-124">Из команды XLL, которую приложение Excel вызвало непосредственно или с помощью VBA.</span><span class="sxs-lookup"><span data-stu-id="dc954-124">From within an XLL command that Excel has called directly or via VBA.</span></span>
    
- <span data-ttu-id="dc954-125">Из листа XLL функции листа макросов, который приложение Excel вызвало непосредственно или с помощью VBA.</span><span class="sxs-lookup"><span data-stu-id="dc954-125">From within an XLL worksheet or macro sheet function that Excel has called directly or via VBA.</span></span>
    
<span data-ttu-id="dc954-126">Невозможно вызвать API C Excel в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="dc954-126">You cannot call the Excel C API in the following scenarios:</span></span>
  
- <span data-ttu-id="dc954-127">Из события операционной системы (например, из функции [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain)).</span><span class="sxs-lookup"><span data-stu-id="dc954-127">From an operating system event (for example, from the [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) function).</span></span> 
    
- <span data-ttu-id="dc954-128">Из фонового потока, созданного вашей DLL.</span><span class="sxs-lookup"><span data-stu-id="dc954-128">From a background thread that your DLL created.</span></span>
    
### <a name="return-values"></a><span data-ttu-id="dc954-129">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="dc954-129">Return values</span></span>

<span data-ttu-id="dc954-130">Все эти четыре функции возвращают целочисленное значение, которое уведомляет вызывающего о том, была ли функция или команда вызвана успешно.</span><span class="sxs-lookup"><span data-stu-id="dc954-130">All four of these functions return an integer value that informs the caller whether the function or command was called successfully.</span></span> <span data-ttu-id="dc954-131">Могут возвращаться любые значения из указанных ниже.</span><span class="sxs-lookup"><span data-stu-id="dc954-131">The returned string can be one of the following values: , , or .</span></span>
  
|<span data-ttu-id="dc954-132">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="dc954-132">**Return value**</span></span>|<span data-ttu-id="dc954-133">**Как определено в Xlcall.h**</span><span class="sxs-lookup"><span data-stu-id="dc954-133">**Defined in Xlcall.h as**</span></span>|<span data-ttu-id="dc954-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dc954-134">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dc954-135">0</span><span class="sxs-lookup"><span data-stu-id="dc954-135">(0)</span></span>  <br/> |<span data-ttu-id="dc954-136">**xlretSuccess**</span><span class="sxs-lookup"><span data-stu-id="dc954-136">**xlretSuccess**</span></span> <br/> |<span data-ttu-id="dc954-137">Функция или команда успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="dc954-137">The function or command executed successfully.</span></span> <span data-ttu-id="dc954-138">Это не означает, что выполнение прошло без ошибок.</span><span class="sxs-lookup"><span data-stu-id="dc954-138">This does not mean that the execution was error free.</span></span> <span data-ttu-id="dc954-139">Например, **Excel4** может возвратить **xlretSuccess** при вызове функции **FIND** даже при оценке **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="dc954-139">For example, **Excel4** could return **xlretSuccess** when calling the function **FIND**, even though it evaluated to **#VALUE!**</span></span> <span data-ttu-id="dc954-140">из-за того, что найти искомый текст не удалось.</span><span class="sxs-lookup"><span data-stu-id="dc954-140">because the search text could not be found.</span></span> <span data-ttu-id="dc954-141">Проверьте тип и возвращаемое значение **XLOPER/XLOPER12**, если есть такая возможность.</span><span class="sxs-lookup"><span data-stu-id="dc954-141">You should inspect the type and value of the returned **XLOPER/XLOPER12** where this is a possibility.</span></span>  <br/> |
|<span data-ttu-id="dc954-142">1</span><span class="sxs-lookup"><span data-stu-id="dc954-142">-1</span></span>  <br/> |<span data-ttu-id="dc954-143">**xlretAbort**</span><span class="sxs-lookup"><span data-stu-id="dc954-143">**xlretAbort**</span></span> <br/> |<span data-ttu-id="dc954-144">Макрос команд остановлен пользователем, который нажал кнопку **ОТМЕНА** кнопку или клавишу ESC.</span><span class="sxs-lookup"><span data-stu-id="dc954-144">A command macro was stopped by the user clicking the **CANCEL** button or pressing the ESC key.</span></span>  <br/> |
|<span data-ttu-id="dc954-145">2</span><span class="sxs-lookup"><span data-stu-id="dc954-145">-2</span></span>  <br/> |<span data-ttu-id="dc954-146">**xlretInvXlfn**</span><span class="sxs-lookup"><span data-stu-id="dc954-146">**xlretInvXlfn**</span></span> <br/> |<span data-ttu-id="dc954-147">Предоставленная функция или код команды недействительны.</span><span class="sxs-lookup"><span data-stu-id="dc954-147">The supplied function or command code is not valid.</span></span> <span data-ttu-id="dc954-148">Эта ошибка может возникнуть, если у функции вызова нет разрешения для вызова функции или команды.</span><span class="sxs-lookup"><span data-stu-id="dc954-148">This error can occur when the calling function does not have permission to call the function or command.</span></span> <span data-ttu-id="dc954-149">Например, функция листа не может вызвать функцию информации листа макросов или функцию команды.</span><span class="sxs-lookup"><span data-stu-id="dc954-149">For example, a worksheet function cannot call a macro sheet information function or a command function.</span></span>  <br/> |
|<span data-ttu-id="dc954-150">4</span><span class="sxs-lookup"><span data-stu-id="dc954-150">4</span></span>  <br/> |<span data-ttu-id="dc954-151">**xlretInvCount**</span><span class="sxs-lookup"><span data-stu-id="dc954-151">**xlretInvCount**</span></span> <br/> |<span data-ttu-id="dc954-152">Число аргументов, передаваемых в вызове, неправильно.</span><span class="sxs-lookup"><span data-stu-id="dc954-152">The number of arguments supplied in the call is not correct.</span></span>  <br/> |
|<span data-ttu-id="dc954-153">8</span><span class="sxs-lookup"><span data-stu-id="dc954-153"> :=8</span></span>  <br/> |<span data-ttu-id="dc954-154">**xlretInvXloper**</span><span class="sxs-lookup"><span data-stu-id="dc954-154">**xlretInvXloper**</span></span> <br/> |<span data-ttu-id="dc954-155">Одно или несколько значений аргумента **XLOPER** или **XLOPER12** не сформировано должным образом или не заполнено.</span><span class="sxs-lookup"><span data-stu-id="dc954-155">One or more of the argument **XLOPER** or **XLOPER12** values are not properly formed or populated.</span></span>  <br/> |
|<span data-ttu-id="dc954-156">16</span><span class="sxs-lookup"><span data-stu-id="dc954-156">1.6</span></span>  <br/> |<span data-ttu-id="dc954-157">**xlretStackOvfl**</span><span class="sxs-lookup"><span data-stu-id="dc954-157">**xlretStackOvfl**</span></span> <br/> |<span data-ttu-id="dc954-158">Приложение Excel обнаружило риск того, что операция могла переполнить стек и не вызвать функцию.</span><span class="sxs-lookup"><span data-stu-id="dc954-158">Excel detected a risk that the operation might overflow its stack and, therefore, did not call the function.</span></span>  <br/> |
|<span data-ttu-id="dc954-159">32</span><span class="sxs-lookup"><span data-stu-id="dc954-159">3.2</span></span>  <br/> |<span data-ttu-id="dc954-160">**xlretFailed**</span><span class="sxs-lookup"><span data-stu-id="dc954-160">**xlretFailed**</span></span> <br/> |<span data-ttu-id="dc954-161">Команда или функция не выполнена по причине, которая не описана одним из других значений возврата.</span><span class="sxs-lookup"><span data-stu-id="dc954-161">The command or function failed for a reason not described by one of the other return values.</span></span> <span data-ttu-id="dc954-162">Например, операция, для которой нужно слишком много памяти, может быть не выполнена с такой ошибкой.</span><span class="sxs-lookup"><span data-stu-id="dc954-162">An operation that would require too much memory, for example, would fail with this error.</span></span> <span data-ttu-id="dc954-163">Это может произойти при попытке преобразовать очень большую ссылку на массив **xltypeMulti** с помощью функции [xlCoerce](xlcoerce.md).</span><span class="sxs-lookup"><span data-stu-id="dc954-163">This could happen during an attempt to convert a very large reference to an **xltypeMulti** array by using the [xlCoerce](xlcoerce.md) function.</span></span>  <br/> |
|<span data-ttu-id="dc954-164">64</span><span class="sxs-lookup"><span data-stu-id="dc954-164">6.4</span></span>  <br/> |<span data-ttu-id="dc954-165">**xlretUncalced**</span><span class="sxs-lookup"><span data-stu-id="dc954-165">**xlretUncalced**</span></span> <br/> |<span data-ttu-id="dc954-166">Операция попыталась получить значение элемента ячейки, вычисление для которой не выполнено.</span><span class="sxs-lookup"><span data-stu-id="dc954-166">The operation attempted to retrieve the value of an uncalculated cell.</span></span> <span data-ttu-id="dc954-167">Для сохранения целостности повторного расчета в Excel функциям листов запрещено выполнять такую операцию.</span><span class="sxs-lookup"><span data-stu-id="dc954-167">To preserve recalculation integrity in Excel, worksheet functions are not permitted to do this.</span></span> <span data-ttu-id="dc954-168">Однако командам и функциям XLL, зарегистрированным как функции листа макросов, разрешен доступ к значениям ячеек, вычисление для которых не выполнено.</span><span class="sxs-lookup"><span data-stu-id="dc954-168">However, XLL commands and functions registered as macro sheet functions are permitted to access uncalculated cell values.</span></span>  <br/> |
|<span data-ttu-id="dc954-169">128</span><span class="sxs-lookup"><span data-stu-id="dc954-169">128</span></span>  <br/> |<span data-ttu-id="dc954-170">**xlretNotThreadSafe**</span><span class="sxs-lookup"><span data-stu-id="dc954-170">**xlretNotThreadSafe**</span></span> <br/> |<span data-ttu-id="dc954-171">(Начиная с Excel 2007.) Функция листа XLL, зарегистрированная как потокобезопасная, попыталась вызвать не потокобезопасную функцию API C.</span><span class="sxs-lookup"><span data-stu-id="dc954-171">(Starting in Excel 2007) An XLL worksheet function registered as thread safe attempted to call a C API function that is not thread safe.</span></span> <span data-ttu-id="dc954-172">Например, потокобезопасная функция не может вызвать функцию XLM **xlfGetCell**.</span><span class="sxs-lookup"><span data-stu-id="dc954-172">For example, a thread-safe function cannot call the XLM function **xlfGetCell**.</span></span>  <br/> |
|<span data-ttu-id="dc954-173">256</span><span class="sxs-lookup"><span data-stu-id="dc954-173">256</span></span>  <br/> |<span data-ttu-id="dc954-174">**xlRetInvAsynchronousContext**</span><span class="sxs-lookup"><span data-stu-id="dc954-174">**xlRetInvAsynchronousContext**</span></span> <br/> |<span data-ttu-id="dc954-175">(Начиная с Excel 2010.) Асинхронный дескриптор функции недопустим.</span><span class="sxs-lookup"><span data-stu-id="dc954-175">(Starting in Excel 2010) The asynchronous function handle is invalid.</span></span>  <br/> |
|<span data-ttu-id="dc954-176">512</span><span class="sxs-lookup"><span data-stu-id="dc954-176">5.12</span></span>  <br/> |<span data-ttu-id="dc954-177">**xlretNotClusterSafe**</span><span class="sxs-lookup"><span data-stu-id="dc954-177">**xlretNotClusterSafe**</span></span> <br/> |<span data-ttu-id="dc954-178">(Начиная с Excel 2010.) Вызов на кластерах не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dc954-178">(Starting in Excel 2010) The call is not supported on clusters.</span></span>  <br/> |
   
<span data-ttu-id="dc954-179">Если функция возвращает одно из значений сбоя в таблице (иными словами, не возвращает **xlretSuccess**), значение возврата **XLOPER** или **XLOPER12** будет также задано как **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="dc954-179">If the function returns one of the failure values in the table (that is, it does not return **xlretSuccess**), the **XLOPER** or **XLOPER12** return value will also be set to **#VALUE!**.</span></span> <span data-ttu-id="dc954-180">В некоторых случаях такой проверки может быть достаточно для тестирования успешного выполнения, но следует помнить, что вызов может возвратить **xlretSuccess** и **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="dc954-180">In certain circumstances, checking for this might be a sufficient test of success, but you should note that a call can return both **xlretSuccess** and **#VALUE!**.</span></span>
  
<span data-ttu-id="dc954-181">Если вызов API C приносит результат либо **xlretUncalced**, либо **xlretAbort**, код DLL или XLL должен возвратить управление приложению Excel, прежде чем создавать другие вызовы API C (кроме вызовов функции [xlfree ](xlfree.md), чтобы высвободить ресурсы памяти, выделенные приложению Excel, в значениях **XLOPER** и **XLOPER12**).</span><span class="sxs-lookup"><span data-stu-id="dc954-181">If a call to the C API results in either **xlretUncalced** or **xlretAbort**, your DLL or XLL code should return control to Excel before making any other C API calls (other than calls to the [xlfree](xlfree.md) function to release Excel-allocated memory resources in **XLOPER** and **XLOPER12** values).</span></span> 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a><span data-ttu-id="dc954-182">Аргумент перечисления команды или функции: xlfn</span><span class="sxs-lookup"><span data-stu-id="dc954-182">Command or Function Enumeration Argument: xlfn</span></span>

<span data-ttu-id="dc954-183">Аргумент _xlfn_ — это первый аргумент для функций обратного вызова, он представляет собой 32-разрядное подписанное целое число.</span><span class="sxs-lookup"><span data-stu-id="dc954-183">The  _xlfn_ argument is the first argument to the callback functions and is a 32-bit signed integer.</span></span> <span data-ttu-id="dc954-184">Его значение должно быть одним из перечислений функции или команды, определенным в файле заголовка SDK Xlcall.h, как показано в приведенном ниже примере.</span><span class="sxs-lookup"><span data-stu-id="dc954-184">Its value should be one of the function or command enumerations defined in the SDK header file Xlcall.h, as shown in the following example.</span></span> 
  
```cs
// Excel function numbers. 
#define xlfCount 0
#define xlfIsna 2
#define xlfIserror 3
#define xlfSum 4
#define xlfAverage 5
#define xlfMin 6
#define xlfMax 7
#define xlfRow 8
#define xlfColumn 9
#define xlfNa 10
...
// Excel command numbers. 
#define xlcBeep (0 | xlCommand)
#define xlcOpen (1 | xlCommand)
#define xlcOpenLinks (2 | xlCommand)
#define xlcCloseAll (3 | xlCommand)
#define xlcSave (4 | xlCommand)
#define xlcSaveAs (5 | xlCommand)
#define xlcFileDelete (6 | xlCommand)
#define xlcPageSetup (7 | xlCommand)
#define xlcPrint (8 | xlCommand)
#define xlcPrinterSetup (9 | xlCommand)
...
```

<span data-ttu-id="dc954-185">Все функции листа и листа макросов находятся в диапазоне шестнадцатеричных чисел от 0 (**xlfCount**) до 0x0fff, хотя максимальное назначенное число в Excel 2013 является десятичным 547, шестнадцатеричным 0x0223 (**xlfFloor_precise**).</span><span class="sxs-lookup"><span data-stu-id="dc954-185">All worksheet and macro sheet functions are in the range from 0 (**xlfCount**) through 0x0fff hexadecimal, although the highest assigned number in Excel 2013 is 547 decimal, 0x0223 hexadecimal (**xlfFloor_precise**).</span></span>
  
<span data-ttu-id="dc954-186">Все функции команды находятся в диапазоне шестнадцатеричных чисел от 0x8000 (**xlcBeep**) до 0x8fff, хотя максимальное назначенное число в Excel 2013 — шестнадцатеричное 0x8328 (**xlcHideallInkannots**).</span><span class="sxs-lookup"><span data-stu-id="dc954-186">All command functions are in the range from 0x8000 hexadecimal (**xlcBeep**) through 0x8fff hexadecimal, although the highest assigned number in Excel 2013 is 0x8328 hexadecimal (**xlcHideallInkannots**).</span></span> <span data-ttu-id="dc954-187">Они определяются в файле заголовка как `(n | xlCommand)`, где `n` — это десятичное число не меньше 0, а **xlCommand** определено как шестнадцатеричное число 0x8000.</span><span class="sxs-lookup"><span data-stu-id="dc954-187">These are defined in the header file as  `(n | xlCommand)` where  `n` is a decimal number greater than or equal to 0 and **xlCommand** is defined as 0x8000 hexadecimal.</span></span> 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a><span data-ttu-id="dc954-188">Вызов команд Excel, которые работают с диалоговыми окнами</span><span class="sxs-lookup"><span data-stu-id="dc954-188">Invoking Excel Commands that Use Dialog Boxes</span></span>

<span data-ttu-id="dc954-189">Некоторые коды команд соответствуют действиям в Excel, в которых используются диалоговые окна.</span><span class="sxs-lookup"><span data-stu-id="dc954-189">Some of the command codes correspond to actions in Excel that use dialog boxes.</span></span> <span data-ttu-id="dc954-190">Например, **xlcFileDelete** принимает один аргумент — маску или имя файла.</span><span class="sxs-lookup"><span data-stu-id="dc954-190">For example, **xlcFileDelete** takes a single argument: a file name or mask.</span></span> <span data-ttu-id="dc954-191">Вызов можно выполнить с помощью диалогового окна, чтобы у пользователя была возможность отменить или изменить операцию удаления.</span><span class="sxs-lookup"><span data-stu-id="dc954-191">This can be invoked with the dialog box so that the user has the opportunity to cancel or modify the delete operation.</span></span> <span data-ttu-id="dc954-192">Вызов возможен и без диалогового окна. В этом случае один или более файлов будут удалены без дальнейшего вмешательства при условии, что они существуют, а у вызывающего есть разрешение.</span><span class="sxs-lookup"><span data-stu-id="dc954-192">It can also be called without the dialog box, in which case the file or files are deleted without any further interaction, assuming they exist and the caller has permission.</span></span> <span data-ttu-id="dc954-193">Для вызова таких команд в формах диалогового окна перечисление команды должно объединяться с помощью битовой операции OR с 0x1000 (**xlPrompt**).</span><span class="sxs-lookup"><span data-stu-id="dc954-193">To call such commands in their dialog box form, the command enumeration must be combined by using the bitwise OR operation with 0x1000 (**xlPrompt**).</span></span>
  
<span data-ttu-id="dc954-194">В показанном ниже примере кода удаляются файлы из текущего каталога, соответствующие маске my_data\*.bak, а диалоговое окно отображается, только если аргумент верный.</span><span class="sxs-lookup"><span data-stu-id="dc954-194">The following code example deletes files in the current directory matching the mask my_data\*.bak, displaying a dialog box only if the argument is true.</span></span>
  
```cs
bool delete_my_backup_files(bool show_dialog)
{
    XLOPER12 xResult, xFilter;
    xFilter.xltype = xltypeStr;
    xFilter.val.str = L"\014my_data*.bak"; // String length: 14 octal
    int cmd;
    if(show_dialog)
        cmd = xlcFileDelete | xlPrompt;
    else
        cmd = xlcFileDelete;
// xResult should be Boolean TRUE if successful, in which
// case return true; otherwise, false.
    return (Excel12(cmd, &xResult, 1, &xFilter) == xlretSuccess
        && xResult.xltype == xltypeBool
        && xResult.val.xbool == 1);
}
```

### <a name="calling-functions-and-commands-in-international-versions"></a><span data-ttu-id="dc954-195">Вызов функций и команд в международных версиях</span><span class="sxs-lookup"><span data-stu-id="dc954-195">Calling Functions and Commands in International Versions</span></span>

<span data-ttu-id="dc954-196">Вы можете настроить в Excel вывод на экран имен функций и команд XLM на разных языках.</span><span class="sxs-lookup"><span data-stu-id="dc954-196">You can configure Excel to display functions and XLM command names in a variety of languages.</span></span> <span data-ttu-id="dc954-197">Некоторые команды и функции API C работают со строками, которые будут интерпретироваться как имена функций или команд.</span><span class="sxs-lookup"><span data-stu-id="dc954-197">Some C API commands and functions operate on strings that are interpreted as function or command names.</span></span> <span data-ttu-id="dc954-198">Например, **xlcFormula** имеет аргумент строки, который предназначен для размещения в указанной ячейке.</span><span class="sxs-lookup"><span data-stu-id="dc954-198">For example, **xlcFormula** takes a string argument that is intended to be placed in a specified cell.</span></span> <span data-ttu-id="dc954-199">Чтобы надстройка работала со всеми языковыми параметрами, можно указать имена строк на английском и задать бит 0x2000 (**xlIntl**) в перечислении функций или команд.</span><span class="sxs-lookup"><span data-stu-id="dc954-199">For your add-in to work with all language settings, you can supply the English string names and set the bit 0x2000 (**xlIntl**) in the function or command enumeration.</span></span>
  
<span data-ttu-id="dc954-200">В представленном ниже примере кода эквивалент `=SUM(X1:X100)` помещается в ячейку A2 на активном листе.</span><span class="sxs-lookup"><span data-stu-id="dc954-200">The following code example places the equivalent of  `=SUM(X1:X100)` in cell A2 on the active sheet.</span></span> <span data-ttu-id="dc954-201">Обратите внимание на то, что он использует функцию Framework **TempActiveRef**, чтобы создать временную внешнюю ссылку **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="dc954-201">Note that it uses the Framework function, **TempActiveRef**, to create a temporary external reference **XLOPER**.</span></span> <span data-ttu-id="dc954-202">Формула будет отображаться в ячейке A2 на правильном языке, соответствующем региону (например, `=SOMME(X1:X100)`, если язык французский).</span><span class="sxs-lookup"><span data-stu-id="dc954-202">The formula will appear in A2 in the correct locale-determined language (for example,  `=SOMME(X1:X100)` if the language is French).</span></span> 
  
```cs
int WINAPI InternationlExample(void)
{
    XLOPER12 xSum, xResult;
    xSum.xltype = xltypeStr;
    xSum.val.str = L"\015=SUM(X1:X100)";
    Excel12(xlcFormula | xlIntl, &xResult, 2,
        &xSum, TempActiveRef(2,2,1,1));
    return 1;
}

```

> [!NOTE]
> <span data-ttu-id="dc954-203">Так как результат вызова в **Excel12** не требуется, нулевое значение (NULL) можно передать как второй аргумент вместо адреса **xResult**.</span><span class="sxs-lookup"><span data-stu-id="dc954-203">Because the result of the call to **Excel12** is not required, zero (NULL) could be passed as the second argument instead of the address of **xResult**.</span></span> <span data-ttu-id="dc954-204">Это обсуждается более подробно в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="dc954-204">( is discussed in the next section.)</span></span> 
  
### <a name="dll-only-functions-and-commands"></a><span data-ttu-id="dc954-205">Функции и команды только для DLL</span><span class="sxs-lookup"><span data-stu-id="dc954-205">DLL-Only Functions and Commands</span></span>

<span data-ttu-id="dc954-206">Excel поддерживает небольшое количество функций, которые доступны только из DLL или XLL.</span><span class="sxs-lookup"><span data-stu-id="dc954-206">Excel supports a small number of functions that are only accessible from a DLL or XLL.</span></span> <span data-ttu-id="dc954-207">Они определяются в файле заголовка как `(n | xlSpecial)`, где `n` — это десятичное число не меньше 0, а `xlSpecial` определяется как шестнадцатеричное число 0x4000.</span><span class="sxs-lookup"><span data-stu-id="dc954-207">These are defined in the header file as  `(n | xlSpecial)` where  `n` is a decimal number greater than or equal to 0 and  `xlSpecial` is defined as 0x4000 hexadecimal.</span></span> <span data-ttu-id="dc954-208">Эти функции перечислены в приведенной ниже таблице и задокументированы в [справочнике по функциям API](excel-xll-sdk-api-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="dc954-208">These functions are listed in the following table and documented in the [API Function Reference](excel-xll-sdk-api-function-reference.md).</span></span>
  
||||
|:-----|:-----|:-----|
|[<span data-ttu-id="dc954-209">xlFree</span><span class="sxs-lookup"><span data-stu-id="dc954-209">xlFree</span></span>](xlfree.md) <br/> |<span data-ttu-id="dc954-210">0</span><span class="sxs-lookup"><span data-stu-id="dc954-210">(0)</span></span> | <span data-ttu-id="dc954-211">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="dc954-211">xlSpecial</span></span>  <br/> |<span data-ttu-id="dc954-212">Освобождает ресурсы памяти, выделенные для Excel.</span><span class="sxs-lookup"><span data-stu-id="dc954-212">Frees Excel-allocated memory resources.</span></span>  <br/> |
|[<span data-ttu-id="dc954-213">xlStack</span><span class="sxs-lookup"><span data-stu-id="dc954-213">xlStack</span></span>](xlstack.md) <br/> |<span data-ttu-id="dc954-214">1</span><span class="sxs-lookup"><span data-stu-id="dc954-214">-1</span></span> | <span data-ttu-id="dc954-215">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="dc954-215">xlSpecial</span></span>  <br/> |<span data-ttu-id="dc954-216">Возвращает свободное место в стеке Excel.</span><span class="sxs-lookup"><span data-stu-id="dc954-216">Returns the free space on the Excel stack.</span></span>  <br/> |
|[<span data-ttu-id="dc954-217">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="dc954-217">xlCoerce</span></span>](xlcoerce.md) <br/> |<span data-ttu-id="dc954-218">2</span><span class="sxs-lookup"><span data-stu-id="dc954-218">-2</span></span> | <span data-ttu-id="dc954-219">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="dc954-219">xlSpecial</span></span>  <br/> |<span data-ttu-id="dc954-220">Преобразует тип **XLOPER** в **XLOPER12** и наоборот</span><span class="sxs-lookup"><span data-stu-id="dc954-220">Converts between **XLOPER** and **XLOPER12** types</span></span>  <br/> |
|[<span data-ttu-id="dc954-221">xlSet</span><span class="sxs-lookup"><span data-stu-id="dc954-221">xlSet</span></span>](xlset.md) <br/> |<span data-ttu-id="dc954-222">3</span><span class="sxs-lookup"><span data-stu-id="dc954-222">-3</span></span> | <span data-ttu-id="dc954-223">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="dc954-223">xlSpecial</span></span>  <br/> |<span data-ttu-id="dc954-224">Предоставляет быстрый метод для задания значений в ячейках.</span><span class="sxs-lookup"><span data-stu-id="dc954-224">Provides a fast method of setting cell values.</span></span>  <br/> |
|[<span data-ttu-id="dc954-225">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="dc954-225">xlSheetId</span></span>](xlsheetid.md) <br/> |<span data-ttu-id="dc954-226">4</span><span class="sxs-lookup"><span data-stu-id="dc954-226">4</span></span> | <span data-ttu-id="dc954-227">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="dc954-227">xlSpecial</span></span>  <br/> |<span data-ttu-id="dc954-228">Получает имя листа от внутреннего идентификатора.</span><span class="sxs-lookup"><span data-stu-id="dc954-228">Obtains a worksheet name from its internal ID.</span></span>  <br/> |
|[<span data-ttu-id="dc954-229">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="dc954-229">xlSheetNm</span></span>](xlsheetnm.md) <br/> |<span data-ttu-id="dc954-230">5</span><span class="sxs-lookup"><span data-stu-id="dc954-230">5</span></span> | <span data-ttu-id="dc954-231">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="dc954-231">xlSpecial</span></span>  <br/> |<span data-ttu-id="dc954-232">Получает внутренний идентификатор листа от его имени.</span><span class="sxs-lookup"><span data-stu-id="dc954-232">Obtains a worksheet internal ID from its name.</span></span>  <br/> |
|[<span data-ttu-id="dc954-233">xlAbort</span><span class="sxs-lookup"><span data-stu-id="dc954-233">xlAbort</span></span>](xlabort.md) <br/> |<span data-ttu-id="dc954-234">6</span><span class="sxs-lookup"><span data-stu-id="dc954-234">6</span></span> | <span data-ttu-id="dc954-235">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="dc954-235">xlSpecial</span></span>  <br/> |<span data-ttu-id="dc954-236">Проверяет, нажал ли пользователь кнопку **ОТМЕНА** или клавишу ESC.</span><span class="sxs-lookup"><span data-stu-id="dc954-236">Verifies whether the user clicked the **CANCEL** button or pressed the ESC key.</span></span>  <br/> |
|[<span data-ttu-id="dc954-237">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="dc954-237">xlGetInst</span></span>](xlgetinst.md) <br/> |<span data-ttu-id="dc954-238">7</span><span class="sxs-lookup"><span data-stu-id="dc954-238">7</span></span> | <span data-ttu-id="dc954-239">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="dc954-239">xlSpecial</span></span>  <br/> |<span data-ttu-id="dc954-240">Получает дескриптор экземпляра Excel.</span><span class="sxs-lookup"><span data-stu-id="dc954-240">Gets the Excel instance handle.</span></span>  <br/> |
|[<span data-ttu-id="dc954-241">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="dc954-241">xlGetHwnd</span></span>](xlgethwnd.md) <br/> |<span data-ttu-id="dc954-242">8</span><span class="sxs-lookup"><span data-stu-id="dc954-242"> :=8</span></span> | <span data-ttu-id="dc954-243">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="dc954-243">xlSpecial</span></span>  <br/> |<span data-ttu-id="dc954-244">Получает дескриптор главного окна Excel.</span><span class="sxs-lookup"><span data-stu-id="dc954-244">Gets the Excel main window handle.</span></span>  <br/> |
|[<span data-ttu-id="dc954-245">xlGetName</span><span class="sxs-lookup"><span data-stu-id="dc954-245">xlGetName</span></span>](xlgetname.md) <br/> |<span data-ttu-id="dc954-246">9</span><span class="sxs-lookup"><span data-stu-id="dc954-246"> :=9</span></span> | <span data-ttu-id="dc954-247">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="dc954-247">xlSpecial</span></span>  <br/> |<span data-ttu-id="dc954-248">Получает путь и имя файла DLL.</span><span class="sxs-lookup"><span data-stu-id="dc954-248">Gets the path and file name of the DLL.</span></span>  <br/> |
|[<span data-ttu-id="dc954-249">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="dc954-249">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md) <br/> |<span data-ttu-id="dc954-250">10</span><span class="sxs-lookup"><span data-stu-id="dc954-250">1.0</span></span> | <span data-ttu-id="dc954-251">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="dc954-251">xlSpecial</span></span>  <br/> |<span data-ttu-id="dc954-252">Эта функция устарела, ее больше не нужно вызывать.</span><span class="sxs-lookup"><span data-stu-id="dc954-252">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="dc954-253">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="dc954-253">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md) <br/> |<span data-ttu-id="dc954-254">11</span><span class="sxs-lookup"><span data-stu-id="dc954-254">1.1</span></span> | <span data-ttu-id="dc954-255">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="dc954-255">xlSpecial</span></span>  <br/> |<span data-ttu-id="dc954-256">Эта функция устарела, ее больше не нужно вызывать.</span><span class="sxs-lookup"><span data-stu-id="dc954-256">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="dc954-257">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="dc954-257">xlDefineBinaryName</span></span>](xldefinebinaryname.md) <br/> |<span data-ttu-id="dc954-258">12</span><span class="sxs-lookup"><span data-stu-id="dc954-258">1.2</span></span> | <span data-ttu-id="dc954-259">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="dc954-259">xlSpecial</span></span>  <br/> |<span data-ttu-id="dc954-260">Определяет имя постоянного хранилища двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="dc954-260">Defines a persistent binary storage name.</span></span>  <br/> |
|[<span data-ttu-id="dc954-261">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="dc954-261">xlGetBinaryName</span></span>](xlgetbinaryname.md) <br/> |<span data-ttu-id="dc954-262">13</span><span class="sxs-lookup"><span data-stu-id="dc954-262">1.3</span></span> | <span data-ttu-id="dc954-263">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="dc954-263">xlSpecial</span></span>  <br/> |<span data-ttu-id="dc954-264">Получает данные имени постоянного хранилища двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="dc954-264">Gets a persistent binary storage name's data.</span></span>  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a><span data-ttu-id="dc954-265">Возвращаемое значение XLOPER/XLOPER12: operRes</span><span class="sxs-lookup"><span data-stu-id="dc954-265">Return value XLOPER/XLOPER12: operRes</span></span>

<span data-ttu-id="dc954-266">Аргумент _operRes_ — это второй аргумент для обратных вызовов, который является указателем на **XLOPER** (**Excel4** и **Excel4v**) или **XLOPER12** (**Excel12** и **Excel12v**).</span><span class="sxs-lookup"><span data-stu-id="dc954-266">The  _operRes_ argument is the second argument to the callbacks and is a pointer to an **XLOPER** (**Excel4** and **Excel4v**) or **XLOPER12** (**Excel12** and **Excel12v**).</span></span> <span data-ttu-id="dc954-267">После успешного вызова он содержит значение, возвращаемое функцией или командой.</span><span class="sxs-lookup"><span data-stu-id="dc954-267">After a successful call, it contains the return value of the function or command.</span></span> <span data-ttu-id="dc954-268">В **operRes** можно задать нуль (указатель NULL), если возвращаемое значение не требуется.</span><span class="sxs-lookup"><span data-stu-id="dc954-268">**operRes** can be set to zero (NULL pointer) if no return value is required.</span></span> <span data-ttu-id="dc954-269">Предыдущее содержимое **operRes** будет перезаписано, чтобы вся ранее указанная память была освобождена перед вызовом во избежание утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="dc954-269">The previous contents of **operRes** are overwritten so that any memory previously pointed to must be freed before to the call to avoid memory leaks.</span></span> 
  
<span data-ttu-id="dc954-270">Если не удается вызвать функцию или команду (например, если аргументы неправильные), для **operRes** будет задана ошибка **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="dc954-270">If the function or command cannot be called (for example, if the arguments are incorrect), **operRes** is set to the error **#VALUE!**.</span></span> <span data-ttu-id="dc954-271">Команда всегда возвращает **логическое** значение **TRUE**, если выполнена успешно, или **FALSE**, если она не выполнена или если пользователь ее отменил.</span><span class="sxs-lookup"><span data-stu-id="dc954-271">A command always returns **Boolean** **TRUE** if it is successful, or **FALSE** if it failed or the user canceled it.</span></span> 
  
## <a name="number-of-subsequent-arguments-count"></a><span data-ttu-id="dc954-272">Число последовательных аргументов: count</span><span class="sxs-lookup"><span data-stu-id="dc954-272">Number of Subsequent Arguments: count</span></span>

<span data-ttu-id="dc954-273">Аргумент _count_ — это третий аргумент для обратного вызова, он представляет собой 32-разрядное подписанное целое число.</span><span class="sxs-lookup"><span data-stu-id="dc954-273">The  _count_ argument is the third argument to the callbacks and is a 32-bit signed integer.</span></span> <span data-ttu-id="dc954-274">Для него должно быть задано число последующих аргументов, начиная с 1.</span><span class="sxs-lookup"><span data-stu-id="dc954-274">It should be set to the number of subsequent arguments, counting from 1.</span></span> <span data-ttu-id="dc954-275">Если функция или команда не принимает аргументы, для него нужно задать ноль.</span><span class="sxs-lookup"><span data-stu-id="dc954-275">If a function or command takes no arguments, it should be set to zero.</span></span> <span data-ttu-id="dc954-276">В Microsoft Office Excel 2003 максимальное число аргументов, которое может принять функция, — 30, хотя большинство принимает меньше.</span><span class="sxs-lookup"><span data-stu-id="dc954-276">In Microsoft Office Excel 2003, the maximum number of arguments that any function can take is 30, although most take fewer than this.</span></span> <span data-ttu-id="dc954-277">Начиная с Excel 2007, максимальное число аргументов, которое может принять функция, увеличилось до 255.</span><span class="sxs-lookup"><span data-stu-id="dc954-277">Starting in Excel 2007, the maximum number of arguments that any function can take was increased to 255.</span></span> 
  
<span data-ttu-id="dc954-278">_count_ в **Excel4** и **Excel12** — это количество указателей на передаваемые значения **XLOPER** или **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="dc954-278">With **Excel4** and **Excel12**,  _count_ is the number of pointers to **XLOPER** or **XLOPER12** values that are being passed.</span></span> <span data-ttu-id="dc954-279">Нужно внимательно следить за тем, чтобы не передать меньше аргументов, чем заданное значение _count_.</span><span class="sxs-lookup"><span data-stu-id="dc954-279">You should be very careful not to pass fewer arguments than the value that  _count_ is set to.</span></span> <span data-ttu-id="dc954-280">Это приведет к тому, что Excel прочтет стек преждевременно и попытается обработать недопустимые значения **XLOPER** или **XLOPER12**, что может привести к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="dc954-280">This would result in Excel reading ahead into the stack and trying to process invalid **XLOPER** or **XLOPER12** values, which could cause an application crash.</span></span> 
  
<span data-ttu-id="dc954-281">_count_ в **Excel4v** и **Excel12v** — это размер массива указателей на значения **XLOPER** или **XLOPER12**, которые передаются как следующий и окончательный аргументы.</span><span class="sxs-lookup"><span data-stu-id="dc954-281">With **Excel4v** and **Excel12v**,  _count_ is the size of the array of pointers to **XLOPER** or **XLOPER12** values that is being passed as the next and final argument.</span></span> <span data-ttu-id="dc954-282">Здесь также нужно внимательно следить за тем, чтобы не передать меньший массив, чем количество элементов _count_ в размере, так как это приведет к переполнению границ массива.</span><span class="sxs-lookup"><span data-stu-id="dc954-282">Again, you should be very careful not to pass a smaller array than  _count_ elements in size, as this will result in the bounds of the array being overrun.</span></span> 
  
## <a name="passing-arguments-to-c-api-functions"></a><span data-ttu-id="dc954-283">Передача аргументов функции API C</span><span class="sxs-lookup"><span data-stu-id="dc954-283">Passing Arguments to C API Functions</span></span>

<span data-ttu-id="dc954-284">**Excel4** и **Excel12** принимают списки аргументов переменной длины после _count_, которые интерпретируются как указатели на значения **XLOPER** и **XLOPER12** соответственно.</span><span class="sxs-lookup"><span data-stu-id="dc954-284">Both **Excel4** and **Excel12** take variable length argument lists, after  _count_, which are interpreted as pointers to **XLOPER** and **XLOPER12** values, respectively.</span></span> <span data-ttu-id="dc954-285">**Excel4v** и **Excel12v** принимают один аргумент после _count_, который является указателем на массив указателей на значения **XLOPER** в случае **Excel4v**, а также на значения **XLOPER12** в случае **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="dc954-285">**Excel4v** and **Excel12v** take a single argument, after  _count_, which is a pointer to an array of pointers to **XLOPER** values in the case of **Excel4v**, and to **XLOPER12** values in the case of **Excel12v**.</span></span>
  
<span data-ttu-id="dc954-286">Формы массива **Excel4v** и **Excel12v** позволяют четко прописать в коде вызов API C, когда число аргументов меняется.</span><span class="sxs-lookup"><span data-stu-id="dc954-286">The array forms, **Excel4v** and **Excel12v**, enable you to code a call to the C API cleanly when the number of arguments is variable.</span></span> <span data-ttu-id="dc954-287">В примере ниже показана функция, которая принимает массив чисел переменного раздела и использует функции листа Excel через API C, чтобы вычислить сумму, среднее, минимальное и максимальное.</span><span class="sxs-lookup"><span data-stu-id="dc954-287">The following example shows a function that takes a variable-sized array of numbers and uses Excel worksheet functions, via the C API, to calculate the sum, average, minimum, and maximum.</span></span> 
  
```cs
void Excel12v_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// 30 is the limit in Excel 2003. 255 is the limit in Excel 2007.
// Use the lower limit to be safe, although it is better to make
// the function version-aware and use the correct limit.
    if(size < 1 || size > 30)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create an array of pointers to XLOPER12 values.
    LPXLOPER12 *xPtrArray =
        (LPXLOPER12 *)malloc(size * sizeof(LPXLOPER12));
// Initialize and populate the array of XLOPER12 values
// and set up the pointers in the pointer array.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
        xPtrArray[i] = xOpArray + i;
    }
    XLOPER12 xResult;
    int retval;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        retval = Excel12v(fn[i], &xResult, size, xPtrArray);
        if(retval == xlretSuccess && xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xPtrArray);
    free(xOpArray);
}

```

<span data-ttu-id="dc954-288">Если в предыдущем коде заменить ссылки на значения **XLOPER12** и **Excel12v**, указав **XLOPER** и **Excel4v** соответственно, функция будет работать во всех версиях Excel.</span><span class="sxs-lookup"><span data-stu-id="dc954-288">Replacing references to **XLOPER12** values with **XLOPER**, and **Excel12v** with **Excel4v**, in the preceding code would result in a function that would work with all versions of Excel.</span></span> <span data-ttu-id="dc954-289">Эта операция функций Excel **SUM**, **AVERAGE**, **MIN** и **MAX** достаточно проста, ее код было бы эффективнее написать на C, чтобы избежать чрезмерных затрат на подготовку аргументов и вызовы в Excel.</span><span class="sxs-lookup"><span data-stu-id="dc954-289">This operation of the Excel functions **SUM**, **AVERAGE**, **MIN**, and **MAX** is simple enough that it would be more efficient to code them in C and avoid the overhead of preparing the arguments and calling into Excel.</span></span> <span data-ttu-id="dc954-290">Однако многие функции Excel более сложные, поэтому такой подход полезен в некоторых случаях.</span><span class="sxs-lookup"><span data-stu-id="dc954-290">However, many of the functions Excel contains are more complex, making this approach useful in some cases.</span></span> 
  
<span data-ttu-id="dc954-291">В статье о [xlfRegister](xlfregister-form-1.md) приведен другой пример работы с **Excel4v** и **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="dc954-291">The [xlfRegister](xlfregister-form-1.md) topic provides another example of working with **Excel4v** and **Excel12v**.</span></span> <span data-ttu-id="dc954-292">При регистрации функции листа XLL можно указать описательную строку для каждого аргумента, который используется в диалоговом окне **Вставить функцию**.</span><span class="sxs-lookup"><span data-stu-id="dc954-292">When registering an XLL worksheet function, you can supply a descriptive string for each argument that is used in the **Paste Function** dialog box.</span></span> <span data-ttu-id="dc954-293">Число всех аргументов, переданных в **xlfRegister**, зависит от числа аргументов, которые принимает функция XLL, и меняется от функции к функции.</span><span class="sxs-lookup"><span data-stu-id="dc954-293">Therefore, the number of total arguments being supplied to **xlfRegister** depends on the number of arguments your XLL function takes and will vary from one function to the next.</span></span> 
  
<span data-ttu-id="dc954-294">Если вы всегда вызываете функцию или команду API C с одним и тем же числом аргументов, вам лучше обойтись без дополнительного шага создания массива указателей для этих аргументов.</span><span class="sxs-lookup"><span data-stu-id="dc954-294">Where you always call a C API function or command with the same number of arguments, you want to avoid the extra step of creating an array of pointers for those arguments.</span></span> <span data-ttu-id="dc954-295">В таких случаях проще и понятнее использование **Excel4** и **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="dc954-295">In those cases, it is simpler and cleaner to use **Excel4** and **Excel12**.</span></span> <span data-ttu-id="dc954-296">Например, при регистрации функций и команд XLL нужно ввести полный путь и имя файла DLL или XLL.</span><span class="sxs-lookup"><span data-stu-id="dc954-296">For example, when registering XLL functions and commands, you need to supply the full path and file name of the DLL or XLL.</span></span> <span data-ttu-id="dc954-297">Можно получить имя файла в вызове **xlfGetName**, а затем передать его с вызовом в **xlFree**, как показано в приведенном ниже примере, посвященном **Excel4** и \*\* Excel12\*\*.</span><span class="sxs-lookup"><span data-stu-id="dc954-297">You can obtain the file name in a call to **xlfGetName** and then release it with a call to **xlFree**, as shown in the following example for both **Excel4** and **Excel12**.</span></span>
  
```cs
XLOPER xDllName;
if(Excel4(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and 
    // then free the memory that Excel allocated for the string.
    Excel4(xlFree, 0, 1, &xDllName);
}
XLOPER12 xDllName;
if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and
    // then free the memory that Excel allocated for the string.
    Excel12(xlFree, 0, 1, &xDllName);
}

```

<span data-ttu-id="dc954-298">На практике код функции **Excel12v_example** можно более эффективно написать путем создания одного аргумента **xltypeMulti** **XLOPER12** и вызова API C с использованием **Excel12**, как показано в примере ниже.</span><span class="sxs-lookup"><span data-stu-id="dc954-298">In practice, the function, **Excel12v_example**, could be coded more efficiently by creating a single **xltypeMulti** **XLOPER12** argument, and calling the C API by using **Excel12**, as shown in the following example.</span></span>
  
```cs
void Excel12_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// In this implementation, the upper limit is the largest
// single column array (equals 2^20, or 1048576, rows in Excel 2007).
    if(size < 1 || size > 1048576)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create and initialize an xltypeMulti array
// that represents a one-column array.
    XLOPER12 xOpMulti;
    xOpMulti.xltype = xltypeMulti;
    xOpMulti.val.array.lparray = xOpArray;
    xOpMulti.val.array.columns = 1;
    xOpMulti.val.array.rows = size;
// Initialize and populate the array of XLOPER12 values.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
    }
    XLOPER12 xResult;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        Excel12(fn[i], &xResult, 1, &xOpMulti);
        if(xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xOpArray);
}

```

> [!NOTE]
> <span data-ttu-id="dc954-299">В этом случае возвращаемое значение **Excel12** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="dc954-299">In this case, the return value of **Excel12** is ignored.</span></span> <span data-ttu-id="dc954-300">Вместо этого код проверяет, является ли возвращаемое значение **XLOPER12** **xltypeNum**, чтобы определить, выполнен ли вызов.</span><span class="sxs-lookup"><span data-stu-id="dc954-300">The code instead checks that the returned **XLOPER12** is **xltypeNum** to determine whether the call was successful.</span></span> 
  
## <a name="xlcallver"></a><span data-ttu-id="dc954-301">XLCallVer</span><span class="sxs-lookup"><span data-stu-id="dc954-301">XLCallVer</span></span>

<span data-ttu-id="dc954-302">Помимо обратных вызовов **Excel4**, **Excel4v**, **Excel12** и **Excel12v**, Excel экспортирует функцию **XLCallVer**, которая возвращает версию API C, выполняемого в настоящий момент.</span><span class="sxs-lookup"><span data-stu-id="dc954-302">In addition to the callbacks **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**, Excel exports a function **XLCallVer**, which returns the version of the C API currently running.</span></span>
  
<span data-ttu-id="dc954-303">Прототип функции выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="dc954-303">The code for the HrProtect function is as follows.</span></span>
  
 `int pascal XLCallVer(void);`
  
<span data-ttu-id="dc954-304">Эту потокобезопасную функцию можно вызвать из любой команды или функции XLL.</span><span class="sxs-lookup"><span data-stu-id="dc954-304">You can call this function, which is thread safe, from any XLL command or function.</span></span>
  
<span data-ttu-id="dc954-305">В версиях Excel, начиная с Excel 97 и заканчивая Excel 2003, **XLCallVer** возвращает 1280 = 0x0500 шестн. = 5 x 256, что означает Excel версии 5.</span><span class="sxs-lookup"><span data-stu-id="dc954-305">In Excel 97 through Excel 2003, **XLCallVer** returns 1280 = 0x0500 hex = 5 x 256, which indicates Excel version 5.</span></span> <span data-ttu-id="dc954-306">Начиная с Excel 2007, функция возвращает 3072 = 0x0c00 шестн. = 12 x 256, что означает версию 12.</span><span class="sxs-lookup"><span data-stu-id="dc954-306">Starting in Excel 2007, it returns 3072 = 0x0c00 hex = 12 x 256, which similarly indicates version 12.</span></span>
  
<span data-ttu-id="dc954-307">Хотя ее можно использовать для определения доступности нового API C во время выполнения, иногда лучше определить текущую версию Excel с помощью `Excel4(xlfGetWorkspace, &version, 1, &arg)`, где `arg` является **XLOPER** с заданным числовым значением 2.</span><span class="sxs-lookup"><span data-stu-id="dc954-307">Although you can use this to determine whether the new C API is available at run time, you might prefer to detect the running version of Excel by using  `Excel4(xlfGetWorkspace, &version, 1, &arg)`, where  `arg` is a numeric **XLOPER** set to 2.</span></span> <span data-ttu-id="dc954-308">Функция возвращает строку **XLOPER**, версию, которую можно привести к целому числу.</span><span class="sxs-lookup"><span data-stu-id="dc954-308">The function returns a string **XLOPER**, version, which can then be coerced to an integer.</span></span> <span data-ttu-id="dc954-309">Причина, по которой лучше полагаться на версию Excel, а не версию API C, заключается в том, что есть различия между Excel 2000, Excel 2002 и Excel 2003, которые вашей надстройке может понадобиться определять.</span><span class="sxs-lookup"><span data-stu-id="dc954-309">The reason for relying on the Excel version rather than the C API version is that there are differences between Excel 2000, Excel 2002, and Excel 2003 that your add-in may also need to detect.</span></span> <span data-ttu-id="dc954-310">Например, изменения точности некоторых статистических функций.</span><span class="sxs-lookup"><span data-stu-id="dc954-310">For example, changes were made to the accuracy of some of the statistics functions.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dc954-311">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dc954-311">See also</span></span>

- [<span data-ttu-id="dc954-312">Создание XLL-файлов</span><span class="sxs-lookup"><span data-stu-id="dc954-312">Creating XLLs</span></span>](creating-xlls.md)  
- [<span data-ttu-id="dc954-313">Доступ к коду XLL в Excel</span><span class="sxs-lookup"><span data-stu-id="dc954-313">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)  
- [<span data-ttu-id="dc954-314">Справочник по функциям API SDK XLL для Excel</span><span class="sxs-lookup"><span data-stu-id="dc954-314">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)  
- [<span data-ttu-id="dc954-315">Функции обратного вызова API C: Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="dc954-315">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)  
- [<span data-ttu-id="dc954-316">Разработка XLL-файлов для Excel</span><span class="sxs-lookup"><span data-stu-id="dc954-316">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

