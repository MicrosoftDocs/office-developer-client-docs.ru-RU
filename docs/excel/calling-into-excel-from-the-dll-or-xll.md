---
title: Вызов в Excel из DLL или XLL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- диалоговые окна [excel 2007], вызов excel команды, DLL-библиотеки [Excel 2007] команды вызова Excel, передача аргументов в функции интерфейса API C [Excel 2007], [Excel 2007], вызова с диалоговые окна команды [Excel 2007], доступного из DLL или XLL Excel4 функции [ Функция Excel12 Excel 2007], [Excel 2007], XLCallVer функции аргумент operRes [Excel 2007], [Excel 2007], функции [Excel 2007], доступного из DLL или XLL Excel12v функции [Excel 2007], DLL-только для функции интерфейса API для C [Excel 2007], [Excel 2007], передача аргументы, аргумент [Excel 2007], команды [Excel 2007], вызов при использовании локализованных версий, DLL-только для команды [Excel 2007], международных версий [Excel 2007], вызов функций и счетчика команд, XLL-модулей [Excel 2007], вызов в Excel, функция [4v Excel Excel 2007] xlfn аргумент [Excel 2007], функции [Excel 2007], вызов при использовании локализованных версий
localization_priority: Normal
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3f36d2f59b7f5bef9f9ffdca4d13e95c788bf113
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807197"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a><span data-ttu-id="4f29d-104">Вызов в Excel из DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="4f29d-104">Calling into Excel from the DLL or XLL</span></span>

<span data-ttu-id="4f29d-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4f29d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4f29d-106">Microsoft Excel позволяет библиотеки DLL для доступа к встроенными командами Excel, функции листа и функции листа макросов.</span><span class="sxs-lookup"><span data-stu-id="4f29d-106">Microsoft Excel enables your DLL to access built-in Excel commands, worksheet functions, and macro sheet functions.</span></span> <span data-ttu-id="4f29d-107">Эти параметры доступны из DLL-Библиотеку команд и функций, вызываемых из Visual Basic для приложений (VBA) и зарегистрированных XLL команд и функций, вызываемых непосредственно в Excel.</span><span class="sxs-lookup"><span data-stu-id="4f29d-107">These are available both from DLL commands and functions called from Visual Basic for Applications (VBA), and from registered XLL commands and functions called directly by Excel.</span></span>
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a><span data-ttu-id="4f29d-108">Excel4, Excel4v, Excel12 и Excel12v функции</span><span class="sxs-lookup"><span data-stu-id="4f29d-108">Excel4, Excel4v, Excel12, and Excel12v Functions</span></span>

<span data-ttu-id="4f29d-109">Приложение Excel позволяет получить доступ к команд и функций через функции обратного вызова [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)и [Excel12v](excel4v-excel12v.md)библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="4f29d-109">Excel enables your DLL to access the commands and functions through the callback functions [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), and [Excel12v](excel4v-excel12v.md).</span></span>
  
<span data-ttu-id="4f29d-110">Функции **Excel4** и **Excel4v** впервые появились в Excel версии 4.</span><span class="sxs-lookup"><span data-stu-id="4f29d-110">The **Excel4** and **Excel4v** functions were introduced in Excel version 4.</span></span> <span data-ttu-id="4f29d-111">Они работают со структурой данных **XLOPER** .</span><span class="sxs-lookup"><span data-stu-id="4f29d-111">They work with the **XLOPER** data structure.</span></span> <span data-ttu-id="4f29d-112">Excel 2007 появились две новые функции обратного вызова, **Excel12** и **Excel12v**, которые работают со структурой данных **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="4f29d-112">Excel 2007 introduced two new callback functions, **Excel12** and **Excel12v**, which work with the **XLOPER12** data structure.</span></span> <span data-ttu-id="4f29d-113">Функции **Excel4** и **Excel4v** экспортируются библиотекой Xlcall32.lib, которое должно быть включено в проекте библиотеки DLL или XLL.</span><span class="sxs-lookup"><span data-stu-id="4f29d-113">The **Excel4** and **Excel4v** functions are exported by the library Xlcall32.lib, which must be included in your DLL or XLL project.</span></span> <span data-ttu-id="4f29d-114">В SDK C++ исходный файл Xlcall.cpp, которая должна быть включена в проект, если вы хотите получить доступ к функциональности Excel с помощью структур **XLOPER12** включены **Excel12** и **Excel12v** .</span><span class="sxs-lookup"><span data-stu-id="4f29d-114">**Excel12** and **Excel12v** are included in the SDK C++ source file Xlcall.cpp, which must be included in your project if you want to access Excel functionality by using **XLOPER12** structures.</span></span> 
  
<span data-ttu-id="4f29d-115">В следующем коде показан прототипов функций для этих функций.</span><span class="sxs-lookup"><span data-stu-id="4f29d-115">The following code shows the function prototypes for these four functions.</span></span> <span data-ttu-id="4f29d-116">Первые три аргумента, совпадают, за исключением того, что второй аргумент указатель **XLOPER** в первой паре и указатель **XLOPER12** второй пару.</span><span class="sxs-lookup"><span data-stu-id="4f29d-116">The first three arguments are the same except that the second argument is a pointer to an **XLOPER** in the first pair and a pointer to an **XLOPER12** in the second pair.</span></span> <span data-ttu-id="4f29d-117">Соглашение о вызове — **_cdecl** в **Excel4** и **Excel12** , чтобы разрешить списки аргументов переменных.</span><span class="sxs-lookup"><span data-stu-id="4f29d-117">The calling convention is **_cdecl** in **Excel4** and **Excel12** to permit the variable argument lists.</span></span> <span data-ttu-id="4f29d-118">Многоточие представляет указатели значения **Excel4** **XLOPER** и **XLOPER12** значения для **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="4f29d-118">The ellipsis represents pointers to **XLOPER** values for **Excel4** and **XLOPER12** values for **Excel12**.</span></span> <span data-ttu-id="4f29d-119">Число указатели равно значение параметра _count_ .</span><span class="sxs-lookup"><span data-stu-id="4f29d-119">The number of pointers equals the value of the  _count_ parameter.</span></span> 
  
<span data-ttu-id="4f29d-120">**Все версии Excel**</span><span class="sxs-lookup"><span data-stu-id="4f29d-120">**All versions of Excel**</span></span>
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
<span data-ttu-id="4f29d-121">**Начиная с версии Excel 2007**</span><span class="sxs-lookup"><span data-stu-id="4f29d-121">**Starting in Excel 2007**</span></span>
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
<span data-ttu-id="4f29d-122">Для библиотеки DLL иметь возможность вызова **Excel4**, **Excel4v**, **Excel12**или **Excel12v**Excel необходимо передать управление библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="4f29d-122">For the DLL to be able to call **Excel4**, **Excel4v**, **Excel12**, or **Excel12v**, Excel must pass control to the DLL.</span></span> <span data-ttu-id="4f29d-123">Это означает, что эти обратные вызовы интерфейса API для C могут вызываться только в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="4f29d-123">This means that these C API callbacks can be called only in the following scenarios:</span></span>
  
- <span data-ttu-id="4f29d-124">Внутри одной командой XLL, Excel, называется напрямую или с помощью VBA.</span><span class="sxs-lookup"><span data-stu-id="4f29d-124">From within an XLL command that Excel has called directly or via VBA.</span></span>
    
- <span data-ttu-id="4f29d-125">Из функцию листа электронной таблицы или макрос XLL, Excel вызываются напрямую или с помощью VBA.</span><span class="sxs-lookup"><span data-stu-id="4f29d-125">From within an XLL worksheet or macro sheet function that Excel has called directly or via VBA.</span></span>
    
<span data-ttu-id="4f29d-126">Не может вызывать Excel C API в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="4f29d-126">You cannot call the Excel C API in the following scenarios:</span></span>
  
- <span data-ttu-id="4f29d-127">Из событий операционной системы (например, от функции [DllMain](http://msdn.microsoft.com/library/base.dllmain%28Office.15%29.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="4f29d-127">From an operating system event (for example, from the [DllMain](http://msdn.microsoft.com/library/base.dllmain%28Office.15%29.aspx) function).</span></span> 
    
- <span data-ttu-id="4f29d-128">В фоновом потоке, которые созданы библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="4f29d-128">From a background thread that your DLL created.</span></span>
    
### <a name="return-values"></a><span data-ttu-id="4f29d-129">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="4f29d-129">Return values</span></span>

<span data-ttu-id="4f29d-130">Все четыре эти функции возвращают целое число, чтобы сообщить вызывающего ли функция или команды успешного вызова.</span><span class="sxs-lookup"><span data-stu-id="4f29d-130">All four of these functions return an integer value that informs the caller whether the function or command was called successfully.</span></span> <span data-ttu-id="4f29d-131">Возвращаемые значения может быть одной из следующих:</span><span class="sxs-lookup"><span data-stu-id="4f29d-131">The values returned can be any of the following:</span></span>
  
|<span data-ttu-id="4f29d-132">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="4f29d-132">**Return value**</span></span>|<span data-ttu-id="4f29d-133">**Определенные в Xlcall.h как**</span><span class="sxs-lookup"><span data-stu-id="4f29d-133">**Defined in Xlcall.h as**</span></span>|<span data-ttu-id="4f29d-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4f29d-134">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4f29d-135">0</span><span class="sxs-lookup"><span data-stu-id="4f29d-135">0</span></span>  <br/> |<span data-ttu-id="4f29d-136">**xlretSuccess**</span><span class="sxs-lookup"><span data-stu-id="4f29d-136">**xlretSuccess**</span></span> <br/> |<span data-ttu-id="4f29d-137">Функция или команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4f29d-137">The function or command executed successfully.</span></span> <span data-ttu-id="4f29d-138">Это означает, что выполнение был ошибки.</span><span class="sxs-lookup"><span data-stu-id="4f29d-138">This does not mean that the execution was error free.</span></span> <span data-ttu-id="4f29d-139">Например, **Excel4** может вернуть **xlretSuccess** при вызове функции **поиска**, несмотря на то, что рассчитано для **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="4f29d-139">For example, **Excel4** could return **xlretSuccess** when calling the function **FIND**, even though it evaluated to **#VALUE!**</span></span> <span data-ttu-id="4f29d-140">так как текст поиска не найден.</span><span class="sxs-lookup"><span data-stu-id="4f29d-140">because the search text could not be found.</span></span> <span data-ttu-id="4f29d-141">Следует проанализировать тип и значение возвращенные **XLOPER и XLOPER12** там, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="4f29d-141">You should inspect the type and value of the returned **XLOPER/XLOPER12** where this is a possibility.</span></span>  <br/> |
|<span data-ttu-id="4f29d-142">1</span><span class="sxs-lookup"><span data-stu-id="4f29d-142">1</span></span>  <br/> |<span data-ttu-id="4f29d-143">**xlretAbort**</span><span class="sxs-lookup"><span data-stu-id="4f29d-143">**xlretAbort**</span></span> <br/> |<span data-ttu-id="4f29d-144">Команда макроса остановлена пользователем, нажав кнопку **Отмена** или нажав клавишу ESC.</span><span class="sxs-lookup"><span data-stu-id="4f29d-144">A command macro was stopped by the user clicking the **CANCEL** button or pressing the ESC key.</span></span>  <br/> |
|<span data-ttu-id="4f29d-145">2</span><span class="sxs-lookup"><span data-stu-id="4f29d-145">2</span></span>  <br/> |<span data-ttu-id="4f29d-146">**xlretInvXlfn**</span><span class="sxs-lookup"><span data-stu-id="4f29d-146">**xlretInvXlfn**</span></span> <br/> |<span data-ttu-id="4f29d-147">Предоставленный функции или код команды является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="4f29d-147">The supplied function or command code is not valid.</span></span> <span data-ttu-id="4f29d-148">Эта ошибка может возникнуть при вызывающей функции не имеет разрешения на вызов функции или команды.</span><span class="sxs-lookup"><span data-stu-id="4f29d-148">This error can occur when the calling function does not have permission to call the function or command.</span></span> <span data-ttu-id="4f29d-149">Например функция листа не может вызывать функции сведений листа макроса или функции, команда.</span><span class="sxs-lookup"><span data-stu-id="4f29d-149">For example, a worksheet function cannot call a macro sheet information function or a command function.</span></span>  <br/> |
|<span data-ttu-id="4f29d-150">4</span><span class="sxs-lookup"><span data-stu-id="4f29d-150">4</span></span>  <br/> |<span data-ttu-id="4f29d-151">**xlretInvCount**</span><span class="sxs-lookup"><span data-stu-id="4f29d-151">**xlretInvCount**</span></span> <br/> |<span data-ttu-id="4f29d-152">Число аргументов в вызове не правильный.</span><span class="sxs-lookup"><span data-stu-id="4f29d-152">The number of arguments supplied in the call is not correct.</span></span>  <br/> |
|<span data-ttu-id="4f29d-153">8</span><span class="sxs-lookup"><span data-stu-id="4f29d-153">8</span></span>  <br/> |<span data-ttu-id="4f29d-154">**xlretInvXloper**</span><span class="sxs-lookup"><span data-stu-id="4f29d-154">**xlretInvXloper**</span></span> <br/> |<span data-ttu-id="4f29d-155">Одно или несколько значений **XLOPER** или **XLOPER12** аргумент неправильно сформирован или не появится.</span><span class="sxs-lookup"><span data-stu-id="4f29d-155">One or more of the argument **XLOPER** or **XLOPER12** values are not properly formed or populated.</span></span>  <br/> |
|<span data-ttu-id="4f29d-156">16</span><span class="sxs-lookup"><span data-stu-id="4f29d-156">16</span></span>  <br/> |<span data-ttu-id="4f29d-157">**xlretStackOvfl**</span><span class="sxs-lookup"><span data-stu-id="4f29d-157">**xlretStackOvfl**</span></span> <br/> |<span data-ttu-id="4f29d-158">Excel обнаружено риск, что операция может переполнения стек и, таким образом, не удалось вызвать функцию.</span><span class="sxs-lookup"><span data-stu-id="4f29d-158">Excel detected a risk that the operation might overflow its stack and, therefore, did not call the function.</span></span>  <br/> |
|<span data-ttu-id="4f29d-159">32</span><span class="sxs-lookup"><span data-stu-id="4f29d-159">32</span></span>  <br/> |<span data-ttu-id="4f29d-160">**xlretFailed**</span><span class="sxs-lookup"><span data-stu-id="4f29d-160">**xlretFailed**</span></span> <br/> |<span data-ttu-id="4f29d-161">Команда или функция не удалось по причине, не описываемых возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="4f29d-161">The command or function failed for a reason not described by one of the other return values.</span></span> <span data-ttu-id="4f29d-162">Операция, которая может потребоваться слишком много памяти, например произойдет сбой с этой ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4f29d-162">An operation that would require too much memory, for example, would fail with this error.</span></span> <span data-ttu-id="4f29d-163">Это может произойти при попытке преобразовать ссылки на очень больших массива **xltypeMulti** с помощью функции [xlCoerce](http://msdn.microsoft.com/library/guid_9d47c16c-a7e7-4998-b594-9cf001827b7b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4f29d-163">This could happen during an attempt to convert a very large reference to an **xltypeMulti** array by using the [xlCoerce](http://msdn.microsoft.com/library/guid_9d47c16c-a7e7-4998-b594-9cf001827b7b%28Office.15%29.aspx) function.</span></span>  <br/> |
|<span data-ttu-id="4f29d-164">64</span><span class="sxs-lookup"><span data-stu-id="4f29d-164">64</span></span>  <br/> |<span data-ttu-id="4f29d-165">**xlretUncalced**</span><span class="sxs-lookup"><span data-stu-id="4f29d-165">**xlretUncalced**</span></span> <br/> |<span data-ttu-id="4f29d-166">Операция для извлечения значения не вычисленной ячейки.</span><span class="sxs-lookup"><span data-stu-id="4f29d-166">The operation attempted to retrieve the value of an uncalculated cell.</span></span> <span data-ttu-id="4f29d-167">Чтобы сохранить целостность Пересчет в Excel, функции листа для этого не разрешены.</span><span class="sxs-lookup"><span data-stu-id="4f29d-167">To preserve recalculation integrity in Excel, worksheet functions are not permitted to do this.</span></span> <span data-ttu-id="4f29d-168">Тем не менее XLL команд и функций, зарегистрированных как функции листа макросов разрешается доступ к значениям, не вычисленной ячейки.</span><span class="sxs-lookup"><span data-stu-id="4f29d-168">However, XLL commands and functions registered as macro sheet functions are permitted to access uncalculated cell values.</span></span>  <br/> |
|<span data-ttu-id="4f29d-169">128</span><span class="sxs-lookup"><span data-stu-id="4f29d-169">128</span></span>  <br/> |<span data-ttu-id="4f29d-170">**xlretNotThreadSafe**</span><span class="sxs-lookup"><span data-stu-id="4f29d-170">**xlretNotThreadSafe**</span></span> <br/> |<span data-ttu-id="4f29d-171">(Начиная с версии Excel 2007) Функция листа XLL зарегистрирована как потокобезопасными попытка вызова функции интерфейса API для C, который не является потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="4f29d-171">(Starting in Excel 2007) An XLL worksheet function registered as thread safe attempted to call a C API function that is not thread safe.</span></span> <span data-ttu-id="4f29d-172">Например являющихся потокобезопасными функции не может вызывать функции XLM **xlfGetCell**.</span><span class="sxs-lookup"><span data-stu-id="4f29d-172">For example, a thread-safe function cannot call the XLM function **xlfGetCell**.</span></span>  <br/> |
|<span data-ttu-id="4f29d-173">256</span><span class="sxs-lookup"><span data-stu-id="4f29d-173">256</span></span>  <br/> |<span data-ttu-id="4f29d-174">**xlRetInvAsynchronousContext**</span><span class="sxs-lookup"><span data-stu-id="4f29d-174">**xlRetInvAsynchronousContext**</span></span> <br/> |<span data-ttu-id="4f29d-175">(Начиная с Excel 2010) Недопустимый дескриптор асинхронные функции.</span><span class="sxs-lookup"><span data-stu-id="4f29d-175">(Starting in Excel 2010) The asynchronous function handle is invalid.</span></span>  <br/> |
|<span data-ttu-id="4f29d-176">512</span><span class="sxs-lookup"><span data-stu-id="4f29d-176">512</span></span>  <br/> |<span data-ttu-id="4f29d-177">**xlretNotClusterSafe**</span><span class="sxs-lookup"><span data-stu-id="4f29d-177">**xlretNotClusterSafe**</span></span> <br/> |<span data-ttu-id="4f29d-178">(Начиная с Excel 2010) Вызов не поддерживается для кластеров.</span><span class="sxs-lookup"><span data-stu-id="4f29d-178">(Starting in Excel 2010) The call is not supported on clusters.</span></span>  <br/> |
   
<span data-ttu-id="4f29d-179">Если функция возвращает одно из значений сбоя в таблице (то есть, он не возвращает **xlretSuccess**), возвращаемое значение **XLOPER** или **XLOPER12** также будет иметь значение **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="4f29d-179">If the function returns one of the failure values in the table (that is, it does not return **xlretSuccess**), the **XLOPER** or **XLOPER12** return value will also be set to **#VALUE!**.</span></span> <span data-ttu-id="4f29d-180">В некоторых случаях, проверка может быть достаточно тест успешно, но следует иметь в виду, что звонка можно вернуть оба **xlretSuccess** и **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="4f29d-180">In certain circumstances, checking for this might be a sufficient test of success, but you should note that a call can return both **xlretSuccess** and **#VALUE!**.</span></span>
  
<span data-ttu-id="4f29d-181">Если вызова интерфейса API для C результатов в **xlretUncalced** или **xlretAbort**, DLL или XLL код должен возвращать элемента управления в Excel перед внесением других вызовов интерфейса API для C (кроме вызовы функции [xlfree](http://msdn.microsoft.com/library/guid_8ce2eef2-0138-495d-b6cb-bbb727a3cda4%28Office.15%29.aspx) для освобождения Excel выделенной памяти ресурсы в **XLOPER** и **XLOPER12** значения).</span><span class="sxs-lookup"><span data-stu-id="4f29d-181">If a call to the C API results in either **xlretUncalced** or **xlretAbort**, your DLL or XLL code should return control to Excel before making any other C API calls (other than calls to the [xlfree](http://msdn.microsoft.com/library/guid_8ce2eef2-0138-495d-b6cb-bbb727a3cda4%28Office.15%29.aspx) function to release Excel-allocated memory resources in **XLOPER** and **XLOPER12** values).</span></span> 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a><span data-ttu-id="4f29d-182">Команда или функция перечисление аргумент: xlfn</span><span class="sxs-lookup"><span data-stu-id="4f29d-182">Command or Function Enumeration Argument: xlfn</span></span>

<span data-ttu-id="4f29d-183">Аргумент _xlfn_ является первый аргумент для обратного вызова функции и 32-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="4f29d-183">The  _xlfn_ argument is the first argument to the callback functions and is a 32-bit signed integer.</span></span> <span data-ttu-id="4f29d-184">Его значение должно быть одно из перечисления команду или функции, определенные в файле заголовка SDK Xlcall.h, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="4f29d-184">Its value should be one of the function or command enumerations defined in the SDK header file Xlcall.h, as shown in the following example.</span></span> 
  
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

<span data-ttu-id="4f29d-185">Все списки и макрос лист функции, в диапазоне от 0 (**xlfCount**) до 0x0fff шестнадцатеричные, несмотря на то, что самый высокий назначен номер в Excel 2013 — 547 decimal, 0x0223 шестнадцатеричных (**xlfFloor_precise**).</span><span class="sxs-lookup"><span data-stu-id="4f29d-185">All worksheet and macro sheet functions are in the range from 0 (**xlfCount**) through 0x0fff hexadecimal, although the highest assigned number in Excel 2013 is 547 decimal, 0x0223 hexadecimal (**xlfFloor_precise**).</span></span>
  
<span data-ttu-id="4f29d-186">Все функции, команды, в диапазоне от 0x8000 шестнадцатеричных (**xlcBeep**) через 0x8fff шестнадцатеричные, несмотря на то, что с наибольшим числом назначенный в Excel 2013 — это шестнадцатеричный 0x8328 (**xlcHideallInkannots**).</span><span class="sxs-lookup"><span data-stu-id="4f29d-186">All command functions are in the range from 0x8000 hexadecimal (**xlcBeep**) through 0x8fff hexadecimal, although the highest assigned number in Excel 2013 is 0x8328 hexadecimal (**xlcHideallInkannots**).</span></span> <span data-ttu-id="4f29d-187">Они определены в файле заголовка как `(n | xlCommand)` где `n` — десятичное число, большее или равное 0 и **xlCommand** определяется как 0x8000 шестнадцатеричные.</span><span class="sxs-lookup"><span data-stu-id="4f29d-187">These are defined in the header file as  `(n | xlCommand)` where  `n` is a decimal number greater than or equal to 0 and **xlCommand** is defined as 0x8000 hexadecimal.</span></span> 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a><span data-ttu-id="4f29d-188">Вызов, использовать диалоговые окна команды Excel</span><span class="sxs-lookup"><span data-stu-id="4f29d-188">Invoking Excel Commands that Use Dialog Boxes</span></span>

<span data-ttu-id="4f29d-189">Некоторые коды команд соответствуют действия в Excel, использующие диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="4f29d-189">Some of the command codes correspond to actions in Excel that use dialog boxes.</span></span> <span data-ttu-id="4f29d-190">Например, **xlcFileDelete** принимает один аргумент: имя файла или маску.</span><span class="sxs-lookup"><span data-stu-id="4f29d-190">For example, **xlcFileDelete** takes a single argument: a file name or mask.</span></span> <span data-ttu-id="4f29d-191">Это может быть вызван с диалоговое окно, чтобы у пользователя есть возможность отменить или изменить операцию удаления.</span><span class="sxs-lookup"><span data-stu-id="4f29d-191">This can be invoked with the dialog box so that the user has the opportunity to cancel or modify the delete operation.</span></span> <span data-ttu-id="4f29d-192">Его можно также вызвать без диалоговом окне в противном случае файл или файлы удаляются без дальнейший взаимодействия, если они существуют и вызывающего абонента есть разрешение.</span><span class="sxs-lookup"><span data-stu-id="4f29d-192">It can also be called without the dialog box, in which case the file or files are deleted without any further interaction, assuming they exist and the caller has permission.</span></span> <span data-ttu-id="4f29d-193">Чтобы позвонить в командах в форму их диалогового окна, перечисление команду должен быть объединен с помощью битовой операции с 0x1000 (**xlPrompt**).</span><span class="sxs-lookup"><span data-stu-id="4f29d-193">To call such commands in their dialog box form, the command enumeration must be combined by using the bitwise OR operation with 0x1000 (**xlPrompt**).</span></span>
  
<span data-ttu-id="4f29d-194">В следующем примере кода удаляются файлы в текущем каталоге соответствия my_data маска\*.bak, отображение диалогового окна только в том случае, если аргумент имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="4f29d-194">The following code example deletes files in the current directory matching the mask my_data\*.bak, displaying a dialog box only if the argument is true.</span></span>
  
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

### <a name="calling-functions-and-commands-in-international-versions"></a><span data-ttu-id="4f29d-195">Вызов функций и команд при использовании локализованных версий</span><span class="sxs-lookup"><span data-stu-id="4f29d-195">Calling Functions and Commands in International Versions</span></span>

<span data-ttu-id="4f29d-196">Можно настроить для отображения функций и имена команд XLM в различных языков в Excel.</span><span class="sxs-lookup"><span data-stu-id="4f29d-196">You can configure Excel to display functions and XLM command names in a variety of languages.</span></span> <span data-ttu-id="4f29d-197">Некоторые команды C API и функции работают, которые интерпретируются как имена функции или командной строки.</span><span class="sxs-lookup"><span data-stu-id="4f29d-197">Some C API commands and functions operate on strings that are interpreted as function or command names.</span></span> <span data-ttu-id="4f29d-198">Например **xlcFormula** принимает строковый аргумент, предназначенного для находились в указанной ячейке.</span><span class="sxs-lookup"><span data-stu-id="4f29d-198">For example, **xlcFormula** takes a string argument that is intended to be placed in a specified cell.</span></span> <span data-ttu-id="4f29d-199">Для надстройки для работы со всех языковых параметров можно задать имена строки на английском языке и установить бит 0x2000 (**библиотеки xlIntl**) в перечислении команду или функции.</span><span class="sxs-lookup"><span data-stu-id="4f29d-199">For your add-in to work with all language settings, you can supply the English string names and set the bit 0x2000 (**xlIntl**) in the function or command enumeration.</span></span>
  
<span data-ttu-id="4f29d-200">В следующем примере кода помещает эквивалент `=SUM(X1:X100)` в ячейку A2 на активном листе.</span><span class="sxs-lookup"><span data-stu-id="4f29d-200">The following code example places the equivalent of  `=SUM(X1:X100)` in cell A2 on the active sheet.</span></span> <span data-ttu-id="4f29d-201">Обратите внимание, что для создания временной внешние ссылки **XLOPER**используется функция Framework, **TempActiveRef**.</span><span class="sxs-lookup"><span data-stu-id="4f29d-201">Note that it uses the Framework function, **TempActiveRef**, to create a temporary external reference **XLOPER**.</span></span> <span data-ttu-id="4f29d-202">Формула будет отображаться в A2 на правильном языке определить языковой стандарт (например, `=SOMME(X1:X100)` Если установлен французский язык).</span><span class="sxs-lookup"><span data-stu-id="4f29d-202">The formula will appear in A2 in the correct locale-determined language (for example,  `=SOMME(X1:X100)` if the language is French).</span></span> 
  
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
> <span data-ttu-id="4f29d-203">Так как в результате вызова **Excel12** не является обязательным, 0 (ноль) может быть передан в качестве аргумента второй, а не адрес **xResult**.</span><span class="sxs-lookup"><span data-stu-id="4f29d-203">Because the result of the call to **Excel12** is not required, zero (NULL) could be passed as the second argument instead of the address of **xResult**.</span></span> <span data-ttu-id="4f29d-204">Рассматривается более в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="4f29d-204">This is discussed more in the next section.</span></span> 
  
### <a name="dll-only-functions-and-commands"></a><span data-ttu-id="4f29d-205">Команды и функции DLL</span><span class="sxs-lookup"><span data-stu-id="4f29d-205">DLL-Only Functions and Commands</span></span>

<span data-ttu-id="4f29d-206">Excel поддерживает несколько функций, которые доступны только из DLL или XLL.</span><span class="sxs-lookup"><span data-stu-id="4f29d-206">Excel supports a small number of functions that are only accessible from a DLL or XLL.</span></span> <span data-ttu-id="4f29d-207">Они определены в файле заголовка как `(n | xlSpecial)` где `n` — десятичное число, большее или равное 0 и `xlSpecial` определяется как 0x4000 шестнадцатеричные.</span><span class="sxs-lookup"><span data-stu-id="4f29d-207">These are defined in the header file as  `(n | xlSpecial)` where  `n` is a decimal number greater than or equal to 0 and  `xlSpecial` is defined as 0x4000 hexadecimal.</span></span> <span data-ttu-id="4f29d-208">Эти функции в следующей таблице перечислены и описаны в [Справочник по функциям API](excel-xll-sdk-api-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="4f29d-208">These functions are listed in the following table and documented in the [API Function Reference](excel-xll-sdk-api-function-reference.md).</span></span>
  
||||
|:-----|:-----|:-----|
|[<span data-ttu-id="4f29d-209">xlFree</span><span class="sxs-lookup"><span data-stu-id="4f29d-209">xlFree</span></span>](xlfree.md) <br/> |<span data-ttu-id="4f29d-210">0</span><span class="sxs-lookup"><span data-stu-id="4f29d-210">0</span></span> | <span data-ttu-id="4f29d-211">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="4f29d-211">xlSpecial</span></span>  <br/> |<span data-ttu-id="4f29d-212">Освобождает ресурсы Excel выделенной памяти.</span><span class="sxs-lookup"><span data-stu-id="4f29d-212">Frees Excel-allocated memory resources.</span></span>  <br/> |
|[<span data-ttu-id="4f29d-213">xlStack</span><span class="sxs-lookup"><span data-stu-id="4f29d-213">xlStack</span></span>](xlstack.md) <br/> |<span data-ttu-id="4f29d-214">1</span><span class="sxs-lookup"><span data-stu-id="4f29d-214">1</span></span> | <span data-ttu-id="4f29d-215">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="4f29d-215">xlSpecial</span></span>  <br/> |<span data-ttu-id="4f29d-216">Возвращает объем свободного пространства в стеке Excel.</span><span class="sxs-lookup"><span data-stu-id="4f29d-216">Returns the free space on the Excel stack.</span></span>  <br/> |
|[<span data-ttu-id="4f29d-217">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="4f29d-217">xlCoerce</span></span>](xlcoerce.md) <br/> |<span data-ttu-id="4f29d-218">2</span><span class="sxs-lookup"><span data-stu-id="4f29d-218">2</span></span> | <span data-ttu-id="4f29d-219">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="4f29d-219">xlSpecial</span></span>  <br/> |<span data-ttu-id="4f29d-220">Преобразование между типами **XLOPER** и **XLOPER12**</span><span class="sxs-lookup"><span data-stu-id="4f29d-220">Converts between **XLOPER** and **XLOPER12** types</span></span>  <br/> |
|[<span data-ttu-id="4f29d-221">функция xlSet</span><span class="sxs-lookup"><span data-stu-id="4f29d-221">xlSet</span></span>](xlset.md) <br/> |<span data-ttu-id="4f29d-222">3</span><span class="sxs-lookup"><span data-stu-id="4f29d-222">3</span></span> | <span data-ttu-id="4f29d-223">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="4f29d-223">xlSpecial</span></span>  <br/> |<span data-ttu-id="4f29d-224">Обеспечивает быстрый метод установки значений ячеек.</span><span class="sxs-lookup"><span data-stu-id="4f29d-224">Provides a fast method of setting cell values.</span></span>  <br/> |
|[<span data-ttu-id="4f29d-225">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="4f29d-225">xlSheetId</span></span>](xlsheetid.md) <br/> |<span data-ttu-id="4f29d-226">4</span><span class="sxs-lookup"><span data-stu-id="4f29d-226">4</span></span> | <span data-ttu-id="4f29d-227">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="4f29d-227">xlSpecial</span></span>  <br/> |<span data-ttu-id="4f29d-228">Получает имя листа из его внутренний идентификатор.</span><span class="sxs-lookup"><span data-stu-id="4f29d-228">Obtains a worksheet name from its internal ID.</span></span>  <br/> |
|[<span data-ttu-id="4f29d-229">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="4f29d-229">xlSheetNm</span></span>](xlsheetnm.md) <br/> |<span data-ttu-id="4f29d-230">5</span><span class="sxs-lookup"><span data-stu-id="4f29d-230">5</span></span> | <span data-ttu-id="4f29d-231">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="4f29d-231">xlSpecial</span></span>  <br/> |<span data-ttu-id="4f29d-232">Получает внутренний идентификатор листа от его имени.</span><span class="sxs-lookup"><span data-stu-id="4f29d-232">Obtains a worksheet internal ID from its name.</span></span>  <br/> |
|[<span data-ttu-id="4f29d-233">xlAbort</span><span class="sxs-lookup"><span data-stu-id="4f29d-233">xlAbort</span></span>](xlabort.md) <br/> |<span data-ttu-id="4f29d-234">6</span><span class="sxs-lookup"><span data-stu-id="4f29d-234">6</span></span> | <span data-ttu-id="4f29d-235">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="4f29d-235">xlSpecial</span></span>  <br/> |<span data-ttu-id="4f29d-236">Проверяет ли пользователь нажимает кнопку **Отмена** или нажата клавиша ESC.</span><span class="sxs-lookup"><span data-stu-id="4f29d-236">Verifies whether the user clicked the **CANCEL** button or pressed the ESC key.</span></span>  <br/> |
|[<span data-ttu-id="4f29d-237">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="4f29d-237">xlGetInst</span></span>](xlgetinst.md) <br/> |<span data-ttu-id="4f29d-238">7</span><span class="sxs-lookup"><span data-stu-id="4f29d-238">7</span></span> | <span data-ttu-id="4f29d-239">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="4f29d-239">xlSpecial</span></span>  <br/> |<span data-ttu-id="4f29d-240">Получает дескриптор экземпляра Excel.</span><span class="sxs-lookup"><span data-stu-id="4f29d-240">Gets the Excel instance handle.</span></span>  <br/> |
|[<span data-ttu-id="4f29d-241">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="4f29d-241">xlGetHwnd</span></span>](xlgethwnd.md) <br/> |<span data-ttu-id="4f29d-242">8</span><span class="sxs-lookup"><span data-stu-id="4f29d-242">8</span></span> | <span data-ttu-id="4f29d-243">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="4f29d-243">xlSpecial</span></span>  <br/> |<span data-ttu-id="4f29d-244">Получает дескриптор главного окна Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="4f29d-244">Gets the Excel main window handle.</span></span>  <br/> |
|[<span data-ttu-id="4f29d-245">xlGetName</span><span class="sxs-lookup"><span data-stu-id="4f29d-245">xlGetName</span></span>](xlgetname.md) <br/> |<span data-ttu-id="4f29d-246">9</span><span class="sxs-lookup"><span data-stu-id="4f29d-246">9</span></span> | <span data-ttu-id="4f29d-247">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="4f29d-247">xlSpecial</span></span>  <br/> |<span data-ttu-id="4f29d-248">Возвращает путь и имя файла библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="4f29d-248">Gets the path and file name of the DLL.</span></span>  <br/> |
|[<span data-ttu-id="4f29d-249">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="4f29d-249">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md) <br/> |<span data-ttu-id="4f29d-250">10</span><span class="sxs-lookup"><span data-stu-id="4f29d-250">10</span></span> | <span data-ttu-id="4f29d-251">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="4f29d-251">xlSpecial</span></span>  <br/> |<span data-ttu-id="4f29d-252">Эта функция устарел и больше не требуется для вызова.</span><span class="sxs-lookup"><span data-stu-id="4f29d-252">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="4f29d-253">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="4f29d-253">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md) <br/> |<span data-ttu-id="4f29d-254">11</span><span class="sxs-lookup"><span data-stu-id="4f29d-254">11</span></span> | <span data-ttu-id="4f29d-255">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="4f29d-255">xlSpecial</span></span>  <br/> |<span data-ttu-id="4f29d-256">Эта функция устарел и больше не требуется для вызова.</span><span class="sxs-lookup"><span data-stu-id="4f29d-256">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="4f29d-257">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="4f29d-257">xlDefineBinaryName</span></span>](xldefinebinaryname.md) <br/> |<span data-ttu-id="4f29d-258">12</span><span class="sxs-lookup"><span data-stu-id="4f29d-258">12</span></span> | <span data-ttu-id="4f29d-259">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="4f29d-259">xlSpecial</span></span>  <br/> |<span data-ttu-id="4f29d-260">Определяет имя сохраняемого двоичные хранения.</span><span class="sxs-lookup"><span data-stu-id="4f29d-260">Defines a persistent binary storage name.</span></span>  <br/> |
|[<span data-ttu-id="4f29d-261">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="4f29d-261">xlGetBinaryName</span></span>](xlgetbinaryname.md) <br/> |<span data-ttu-id="4f29d-262">13</span><span class="sxs-lookup"><span data-stu-id="4f29d-262">13</span></span> | <span data-ttu-id="4f29d-263">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="4f29d-263">xlSpecial</span></span>  <br/> |<span data-ttu-id="4f29d-264">Получает имя постоянное хранилище двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="4f29d-264">Gets a persistent binary storage name's data.</span></span>  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a><span data-ttu-id="4f29d-265">Возвращаемое значение XLOPER и XLOPER12: operRes</span><span class="sxs-lookup"><span data-stu-id="4f29d-265">Return value XLOPER/XLOPER12: operRes</span></span>

<span data-ttu-id="4f29d-266">Аргумент _operRes_ является второй аргумент процедуры обратного вызова и указатель **XLOPER** (**Excel4** и **Excel4v**) или **XLOPER12** (**Excel12** и **Excel12v**).</span><span class="sxs-lookup"><span data-stu-id="4f29d-266">The  _operRes_ argument is the second argument to the callbacks and is a pointer to an **XLOPER** (**Excel4** and **Excel4v**) or **XLOPER12** (**Excel12** and **Excel12v**).</span></span> <span data-ttu-id="4f29d-267">После успешного вызова в нем возвращаемое значение функции или команды.</span><span class="sxs-lookup"><span data-stu-id="4f29d-267">After a successful call, it contains the return value of the function or command.</span></span> <span data-ttu-id="4f29d-268">можно включить **operRes** ноль (указатель NULL), если необходим без возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="4f29d-268">**operRes** can be set to zero (NULL pointer) if no return value is required.</span></span> <span data-ttu-id="4f29d-269">Предыдущее содержимое **operRes** , будут перезаписаны, чтобы любой памяти, ранее, на который указывает освобождения перед звонок во избежание утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="4f29d-269">The previous contents of **operRes** are overwritten so that any memory previously pointed to must be freed before to the call to avoid memory leaks.</span></span> 
  
<span data-ttu-id="4f29d-270">Если функция или команда не может вызываться (например, если неправильные аргументы), **operRes** задано значение ошибки **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="4f29d-270">If the function or command cannot be called (for example, if the arguments are incorrect), **operRes** is set to the error **#VALUE!**.</span></span> <span data-ttu-id="4f29d-271">Команду всегда возвращает **логическое** **значение TRUE,** Если операция будет успешна, или **значение FALSE,** если он не или пользователь отменил ее.</span><span class="sxs-lookup"><span data-stu-id="4f29d-271">A command always returns **Boolean** **TRUE** if it is successful, or **FALSE** if it failed or the user canceled it.</span></span> 
  
## <a name="number-of-subsequent-arguments-count"></a><span data-ttu-id="4f29d-272">Число аргументов последующие: count</span><span class="sxs-lookup"><span data-stu-id="4f29d-272">Number of Subsequent Arguments: count</span></span>

<span data-ttu-id="4f29d-273">Аргумент _count_ — третий аргумент процедуры обратного вызова и 32-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="4f29d-273">The  _count_ argument is the third argument to the callbacks and is a 32-bit signed integer.</span></span> <span data-ttu-id="4f29d-274">Он должен быть задан номер последующие аргументы, начиная с 1.</span><span class="sxs-lookup"><span data-stu-id="4f29d-274">It should be set to the number of subsequent arguments, counting from 1.</span></span> <span data-ttu-id="4f29d-275">Если функция или команда не принимает аргументы, его необходимо задать нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="4f29d-275">If a function or command takes no arguments, it should be set to zero.</span></span> <span data-ttu-id="4f29d-276">В Microsoft Office Excel 2003 максимальное количество аргументов, которые может выполнять все функции является 30, однако большинство меньше, чем это.</span><span class="sxs-lookup"><span data-stu-id="4f29d-276">In Microsoft Office Excel 2003, the maximum number of arguments that any function can take is 30, although most take fewer than this.</span></span> <span data-ttu-id="4f29d-277">Начиная с версии Excel 2007, максимальное количество аргументов, которые может выполнять все функции было увеличено до 255.</span><span class="sxs-lookup"><span data-stu-id="4f29d-277">Starting in Excel 2007, the maximum number of arguments that any function can take was increased to 255.</span></span> 
  
<span data-ttu-id="4f29d-278">С помощью **Excel4** и **Excel12** _счетчик_ — число указатели на **XLOPER** или **XLOPER12** значения, которые передаются.</span><span class="sxs-lookup"><span data-stu-id="4f29d-278">With **Excel4** and **Excel12**,  _count_ is the number of pointers to **XLOPER** or **XLOPER12** values that are being passed.</span></span> <span data-ttu-id="4f29d-279">Внимательно очень не для передачи меньше аргументов, чем значение этого _счетчика_ имеет значение.</span><span class="sxs-lookup"><span data-stu-id="4f29d-279">You should be very careful not to pass fewer arguments than the value that  _count_ is set to.</span></span> <span data-ttu-id="4f29d-280">В результате Excel чтение издержек в стеке и выполнении недопустимые значения **XLOPER** или **XLOPER12** , что может привести к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="4f29d-280">This would result in Excel reading ahead into the stack and trying to process invalid **XLOPER** or **XLOPER12** values, which could cause an application crash.</span></span> 
  
<span data-ttu-id="4f29d-281">С помощью **Excel4v** и **Excel12v** _count_ — размер массива указатели на **XLOPER** или **XLOPER12** значения, которое передается в качестве аргумента следующий и последний.</span><span class="sxs-lookup"><span data-stu-id="4f29d-281">With **Excel4v** and **Excel12v**,  _count_ is the size of the array of pointers to **XLOPER** or **XLOPER12** values that is being passed as the next and final argument.</span></span> <span data-ttu-id="4f29d-282">Опять же должен быть очень избегать передать меньшего размера массива, чем _количество_ элементов в размер, как это приведет к границ массива переполнения.</span><span class="sxs-lookup"><span data-stu-id="4f29d-282">Again, you should be very careful not to pass a smaller array than  _count_ elements in size, as this will result in the bounds of the array being overrun.</span></span> 
  
## <a name="passing-arguments-to-c-api-functions"></a><span data-ttu-id="4f29d-283">Передача аргументов в функции интерфейса API для C</span><span class="sxs-lookup"><span data-stu-id="4f29d-283">Passing Arguments to C API Functions</span></span>

<span data-ttu-id="4f29d-284">**Excel4** и **Excel12** занять переменной длины списки аргументов, после _count_, которые интерпретируются как указатели на значения **XLOPER** и **XLOPER12** , соответственно.</span><span class="sxs-lookup"><span data-stu-id="4f29d-284">Both **Excel4** and **Excel12** take variable length argument lists, after  _count_, which are interpreted as pointers to **XLOPER** and **XLOPER12** values, respectively.</span></span> <span data-ttu-id="4f29d-285">**Excel4v** и **Excel12v** принимает один аргумент, после _count_, то есть указатель на массив указателей **XLOPER** значения в случае **Excel4v**и **XLOPER12** значения в случае **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="4f29d-285">**Excel4v** and **Excel12v** take a single argument, after  _count_, which is a pointer to an array of pointers to **XLOPER** values in the case of **Excel4v**, and to **XLOPER12** values in the case of **Excel12v**.</span></span>
  
<span data-ttu-id="4f29d-286">Формы массива, **Excel4v** и **Excel12v**позволяют аккуратно код вызова интерфейса API для C при число аргументов является переменной.</span><span class="sxs-lookup"><span data-stu-id="4f29d-286">The array forms, **Excel4v** and **Excel12v**, enable you to code a call to the C API cleanly when the number of arguments is variable.</span></span> <span data-ttu-id="4f29d-287">В следующем примере функция, которая принимает размер переменной массива чисел и использует функции листа Excel, с помощью интерфейса API для C, для вычисления суммы, средний, минимальный и максимальный.</span><span class="sxs-lookup"><span data-stu-id="4f29d-287">The following example shows a function that takes a variable-sized array of numbers and uses Excel worksheet functions, via the C API, to calculate the sum, average, minimum, and maximum.</span></span> 
  
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

<span data-ttu-id="4f29d-288">Замените ссылки значения **XLOPER12** **XLOPER**и **Excel12v** с **Excel4v**, в предыдущем примере кода приведет к функции, которая будет работать со всеми версиями Excel.</span><span class="sxs-lookup"><span data-stu-id="4f29d-288">Replacing references to **XLOPER12** values with **XLOPER**, and **Excel12v** with **Excel4v**, in the preceding code would result in a function that would work with all versions of Excel.</span></span> <span data-ttu-id="4f29d-289">Эта операция функции Excel **Сумма**, **Среднее**, **MIN**и **MAX** довольно проста, что было бы более эффективно код их C и избежать Подготовка аргументов и вызов в Excel.</span><span class="sxs-lookup"><span data-stu-id="4f29d-289">This operation of the Excel functions **SUM**, **AVERAGE**, **MIN**, and **MAX** is simple enough that it would be more efficient to code them in C and avoid the overhead of preparing the arguments and calling into Excel.</span></span> <span data-ttu-id="4f29d-290">Тем не менее многие из функций, которые Excel содержит более сложны, выполнение этого подхода полезно в некоторых случаях.</span><span class="sxs-lookup"><span data-stu-id="4f29d-290">However, many of the functions Excel contains are more complex, making this approach useful in some cases.</span></span> 
  
<span data-ttu-id="4f29d-291">Другой пример работы с **Excel4v** и **Excel12v**раздел [xlfRegister](http://msdn.microsoft.com/library/guid_c730124c-1886-4a0f-8f06-79763025537d%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4f29d-291">The [xlfRegister](http://msdn.microsoft.com/library/guid_c730124c-1886-4a0f-8f06-79763025537d%28Office.15%29.aspx) topic provides another example of working with **Excel4v** and **Excel12v**.</span></span> <span data-ttu-id="4f29d-292">При регистрации функция листа XLL, можно указать строку описания для каждого аргумента, который используется в диалоговом окне **Вставить функцию** .</span><span class="sxs-lookup"><span data-stu-id="4f29d-292">When registering an XLL worksheet function, you can supply a descriptive string for each argument that is used in the **Paste Function** dialog box.</span></span> <span data-ttu-id="4f29d-293">Таким образом число общее аргументов в **xlfRegister** зависит от числа аргументы, которые использует функцию XLL и будут зависеть от одной функции в другую.</span><span class="sxs-lookup"><span data-stu-id="4f29d-293">Therefore, the number of total arguments being supplied to **xlfRegister** depends on the number of arguments your XLL function takes and will vary from one function to the next.</span></span> 
  
<span data-ttu-id="4f29d-294">Там, где вы всегда вызова функции интерфейса API для C или команды с такое же число аргументов, необходимо избежать дополнительные действия по созданию массив указателей для этих аргументов.</span><span class="sxs-lookup"><span data-stu-id="4f29d-294">Where you always call a C API function or command with the same number of arguments, you want to avoid the extra step of creating an array of pointers for those arguments.</span></span> <span data-ttu-id="4f29d-295">В таких случаях проще и более чистый используйте **Excel4** и **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="4f29d-295">In those cases, it is simpler and cleaner to use **Excel4** and **Excel12**.</span></span> <span data-ttu-id="4f29d-296">Например при регистрации функций и команд XLL, необходимо указать полный путь и имя библиотеки DLL или XLL.</span><span class="sxs-lookup"><span data-stu-id="4f29d-296">For example, when registering XLL functions and commands, you need to supply the full path and file name of the DLL or XLL.</span></span> <span data-ttu-id="4f29d-297">Можно получить имя файла в вызове **xlfGetName** и освобождать с помощью вызова **xlFree**, как показано в следующем примере для **Excel4** и **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="4f29d-297">You can obtain the file name in a call to **xlfGetName** and then release it with a call to **xlFree**, as shown in the following example for both **Excel4** and **Excel12**.</span></span>
  
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

<span data-ttu-id="4f29d-298">На практике функцию **Excel12v_example**можно построить более эффективно путем создания одного **xltypeMulti** **XLOPER12** аргумент и вызова интерфейса API для C с помощью **Excel12**, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="4f29d-298">In practice, the function, **Excel12v_example**, could be coded more efficiently by creating a single **xltypeMulti** **XLOPER12** argument, and calling the C API by using **Excel12**, as shown in the following example.</span></span>
  
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
> <span data-ttu-id="4f29d-299">В этом случае возвращаемое значение **Excel12** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="4f29d-299">In this case, the return value of **Excel12** is ignored.</span></span> <span data-ttu-id="4f29d-300">Код вместо этого проверяется, что возвращенные **XLOPER12** **xltypeNum** для определения, успешно ли вызов.</span><span class="sxs-lookup"><span data-stu-id="4f29d-300">The code instead checks that the returned **XLOPER12** is **xltypeNum** to determine whether the call was successful.</span></span> 
  
## <a name="xlcallver"></a><span data-ttu-id="4f29d-301">XLCallVer</span><span class="sxs-lookup"><span data-stu-id="4f29d-301">XLCallVer</span></span>

<span data-ttu-id="4f29d-302">В дополнение к обратных вызовов **Excel4**, **Excel4v**, **Excel12**и **Excel12v**Excel экспортирует функции **XLCallVer**, который возвращает номер версии интерфейса API для C в настоящее время работает.</span><span class="sxs-lookup"><span data-stu-id="4f29d-302">In addition to the callbacks **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**, Excel exports a function **XLCallVer**, which returns the version of the C API currently running.</span></span>
  
<span data-ttu-id="4f29d-303">Прототип функции выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4f29d-303">The function prototype is as follows:</span></span>
  
 `int pascal XLCallVer(void);`
  
<span data-ttu-id="4f29d-304">Можно вызвать эту функцию, являющийся потокобезопасными, из XLL команда или функция.</span><span class="sxs-lookup"><span data-stu-id="4f29d-304">You can call this function, which is thread safe, from any XLL command or function.</span></span>
  
<span data-ttu-id="4f29d-305">В Excel 97 — Excel 2003, **XLCallVer** возвращает 1280 = значения 0x0500 hex = 5 x 256, что указывает Excel версии 5.</span><span class="sxs-lookup"><span data-stu-id="4f29d-305">In Excel 97 through Excel 2003, **XLCallVer** returns 1280 = 0x0500 hex = 5 x 256, which indicates Excel version 5.</span></span> <span data-ttu-id="4f29d-306">Начиная с версии Excel 2007, возвращает большего 3072 пикселей = 0x0c00 hex = 12 x 256, аналогично указывает на версию 12.</span><span class="sxs-lookup"><span data-stu-id="4f29d-306">Starting in Excel 2007, it returns 3072 = 0x0c00 hex = 12 x 256, which similarly indicates version 12.</span></span>
  
<span data-ttu-id="4f29d-307">Несмотря на то, что это можно использовать для определения доступности нового C API во время выполнения, можно определять используемой версии Excel с помощью `Excel4(xlfGetWorkspace, &version, 1, &arg)`, где `arg` — это числовой, **XLOPER** значение 2.</span><span class="sxs-lookup"><span data-stu-id="4f29d-307">Although you can use this to determine whether the new C API is available at run time, you might prefer to detect the running version of Excel by using  `Excel4(xlfGetWorkspace, &version, 1, &arg)`, where  `arg` is a numeric **XLOPER** set to 2.</span></span> <span data-ttu-id="4f29d-308">Функция возвращает строку **XLOPER**версии, который затем может быть преобразован в тип integer.</span><span class="sxs-lookup"><span data-stu-id="4f29d-308">The function returns a string **XLOPER**, version, which can then be coerced to an integer.</span></span> <span data-ttu-id="4f29d-309">Причина от версии Excel, а не версия интерфейса API для C является различия между Excel 2000, Excel 2002 и Excel 2003, надстройка может также потребоваться обнаружения.</span><span class="sxs-lookup"><span data-stu-id="4f29d-309">The reason for relying on the Excel version rather than the C API version is that there are differences between Excel 2000, Excel 2002, and Excel 2003 that your add-in may also need to detect.</span></span> <span data-ttu-id="4f29d-310">Например в точность некоторых статистических функций были внесены изменения.</span><span class="sxs-lookup"><span data-stu-id="4f29d-310">For example, changes were made to the accuracy of some of the statistics functions.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4f29d-311">См. также</span><span class="sxs-lookup"><span data-stu-id="4f29d-311">See also</span></span>



[<span data-ttu-id="4f29d-312">Создание XLL-модулей</span><span class="sxs-lookup"><span data-stu-id="4f29d-312">Creating XLLs</span></span>](creating-xlls.md)
  
[<span data-ttu-id="4f29d-313">Доступ к XLL-коду в Excel</span><span class="sxs-lookup"><span data-stu-id="4f29d-313">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
[<span data-ttu-id="4f29d-314">���������� �� ������� Excel 2013 XLL SDK API</span><span class="sxs-lookup"><span data-stu-id="4f29d-314">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)
  
[<span data-ttu-id="4f29d-315">������� ��������� ������ API C Excel4 Excel12</span><span class="sxs-lookup"><span data-stu-id="4f29d-315">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)
  
[<span data-ttu-id="4f29d-316">���������� XLL-������� ��� Excel 2013</span><span class="sxs-lookup"><span data-stu-id="4f29d-316">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

