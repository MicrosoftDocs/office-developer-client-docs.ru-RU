---
title: Многопоточность и конфликты памяти в Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- Многопоточность в Excel, конфликты памяти в Excel, функции [Excel 2007], потокобезопасные и потокобезопасные функции [Excel 2007], локальная память потока [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a385728450fc6519d7f5211c186a9d74e623bf7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301640"
---
# <a name="multithreading-and-memory-contention-in-excel"></a><span data-ttu-id="e4957-104">Многопоточность и конфликты памяти в Excel</span><span class="sxs-lookup"><span data-stu-id="e4957-104">Multithreading and Memory Contention in Excel</span></span>

 <span data-ttu-id="e4957-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e4957-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e4957-106">Более ранние версии Microsoft Excel, чем Excel 2007, используют один поток для всех вычислений листа.</span><span class="sxs-lookup"><span data-stu-id="e4957-106">Versions of Microsoft Excel earlier than Excel 2007 use a single thread for all worksheet calculations.</span></span> <span data-ttu-id="e4957-107">Тем не менее, начиная с Excel 2007, в Excel можно настроить использование от 1 до 1024 параллельных потоков для вычисления листа.</span><span class="sxs-lookup"><span data-stu-id="e4957-107">However, starting in Excel 2007, Excel can be configured to use from 1 to 1024 concurrent threads for worksheet calculation.</span></span> <span data-ttu-id="e4957-108">На многопроцессорном или многоядерном компьютере количество потоков по умолчанию равно числу процессоров или ядер.</span><span class="sxs-lookup"><span data-stu-id="e4957-108">On a multi-processor or multi-core computer, the default number of threads is equal to the number of processors or cores.</span></span> <span data-ttu-id="e4957-109">Таким образом, потокобезопасные ячейки или ячейки, содержащие только функции, которые являются потокобезопасными, могут быть выделены для параллельных потоков, подчиняются обычной логике пересчета, которую необходимо вычислить после их приоритетов.</span><span class="sxs-lookup"><span data-stu-id="e4957-109">Therefore, thread-safe cells, or cells that only contain functions that are thread safe, can be allotted to concurrent threads, subject to the usual recalculation logic of needing to be calculated after their precedents.</span></span>
  
## <a name="thread-safe-functions"></a><span data-ttu-id="e4957-110">Потокобезопасные функции</span><span class="sxs-lookup"><span data-stu-id="e4957-110">Thread-Safe Functions</span></span>

<span data-ttu-id="e4957-111">Большинство встроенных функций листа, начиная с Excel 2007, являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="e4957-111">Most of the built-in worksheet functions starting in Excel 2007 are thread safe.</span></span> <span data-ttu-id="e4957-112">Вы также можете записывать и регистрировать функции XLL как потокобезопасные.</span><span class="sxs-lookup"><span data-stu-id="e4957-112">You can also write and register XLL functions as being thread safe.</span></span> <span data-ttu-id="e4957-113">Excel использует один поток (основной поток), чтобы вызывать все команды, небезопасные функции, функции **xlAuto** (кроме [xlAutoFree](xlautofree-xlautofree12.md) и **xlAutoFree12**), а также функции COM и Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="e4957-113">Excel uses one thread (its main thread) to call all commands, thread-unsafe functions, **xlAuto** functions (except [xlAutoFree](xlautofree-xlautofree12.md) and **xlAutoFree12**), and COM and Visual Basic for Applications (VBA) functions.</span></span>
  
<span data-ttu-id="e4957-114">Где функция XLL возвращает **XLOPER** или **XLOPER12** с набором **кслбитдллфри** , Excel использует тот же поток, в котором был выполнен вызов функции для вызова **xlAutoFree** или **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="e4957-114">Where an XLL function returns an **XLOPER** or **XLOPER12** with **xlbitDLLFree** set, Excel uses the same thread on which the function call was made to call **xlAutoFree** or **xlAutoFree12**.</span></span> <span data-ttu-id="e4957-115">Вызов **xlAutoFree** или **xlAutoFree12** выполняется до следующего вызова функции в этом потоке.</span><span class="sxs-lookup"><span data-stu-id="e4957-115">The call to **xlAutoFree** or **xlAutoFree12** is made before the next function call on that thread.</span></span> 
  
<span data-ttu-id="e4957-116">Для разработчиков XLL существуют преимущества для создания потокобезопасных функций:</span><span class="sxs-lookup"><span data-stu-id="e4957-116">For XLL developers, there are benefits for creating thread-safe functions:</span></span>
  
- <span data-ttu-id="e4957-117">Они позволяют Excel максимально использовать многопроцессорный или многоядерный компьютер.</span><span class="sxs-lookup"><span data-stu-id="e4957-117">They allow Excel to make the most of a multi-processor or multi-core computer.</span></span>
    
- <span data-ttu-id="e4957-118">Они открывают возможность использования удаленных серверов гораздо эффективнее, чем можно сделать с помощью одного потока.</span><span class="sxs-lookup"><span data-stu-id="e4957-118">They open up the possibility of using remote servers much more efficiently than can be done using a single thread.</span></span>
    
<span data-ttu-id="e4957-119">Предположим, что у вас есть компьютер с одним процессором, на котором настроено использование, скажем, *N* потоков.</span><span class="sxs-lookup"><span data-stu-id="e4957-119">Suppose that you have a single-processor computer that has been configured to use, say,  *N*  threads.</span></span> <span data-ttu-id="e4957-120">Предположим, что электронная таблица работает с большим количеством вызовов функции XLL, которые в свою очередь отправляют запрос на данные или вычисление, выполняемое на удаленном сервере или кластере серверов.</span><span class="sxs-lookup"><span data-stu-id="e4957-120">Suppose that a spreadsheet is running that makes a large number of calls to an XLL function that in turn sends a request for data or for a calculation to be performed to a remote server or cluster of servers.</span></span> <span data-ttu-id="e4957-121">В зависимости от топологии дерева зависимостей Excel может вызвать функцию N раз почти одновременно.</span><span class="sxs-lookup"><span data-stu-id="e4957-121">Subject to the topology of the dependency tree, Excel could call the function N times almost simultaneously.</span></span> <span data-ttu-id="e4957-122">При условии, что сервер или серверы работают достаточно быстро или параллельно, время пересчета электронной таблицы может быть уменьшено до 1/N-кратного.</span><span class="sxs-lookup"><span data-stu-id="e4957-122">Provided that the server or servers are sufficiently fast or parallel, the recalculation time of the spreadsheet could be reduced by as much as a factor of 1/N.</span></span> 
  
<span data-ttu-id="e4957-123">Ключевая ошибка при написании потокобезопасных функций — корректно обрабатывает конфликты для ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e4957-123">The key issue in writing thread-safe functions is handling contention for resources correctly.</span></span> <span data-ttu-id="e4957-124">Обычно это означает состязание за память и может быть разбито на две проблемы:</span><span class="sxs-lookup"><span data-stu-id="e4957-124">This usually means memory contention, and it can be broken down into two issues:</span></span>
  
- <span data-ttu-id="e4957-125">Сведения о том, как создать память, которая будет использоваться только для этого потока.</span><span class="sxs-lookup"><span data-stu-id="e4957-125">How to create memory that you know will only be used by this thread.</span></span>
    
- <span data-ttu-id="e4957-126">Обеспечение безопасного доступа к общей памяти несколькими потоками.</span><span class="sxs-lookup"><span data-stu-id="e4957-126">How to ensure that shared memory is accessed by multiple threads safely.</span></span>
    
<span data-ttu-id="e4957-127">Первое, что следует знать о том, какой объем памяти XLL доступен всем потокам, и что доступно только в выполняемом в настоящий момент потоке.</span><span class="sxs-lookup"><span data-stu-id="e4957-127">The first thing to be aware of is what memory in an XLL is accessible by all threads, and what is only accessible by the currently executing thread.</span></span>
  
 <span data-ttu-id="e4957-128">**Доступно всем потокам**</span><span class="sxs-lookup"><span data-stu-id="e4957-128">**Accessible by all threads**</span></span>
  
- <span data-ttu-id="e4957-129">Переменные, структуры и экземпляры классов, объявленные вне тела функции.</span><span class="sxs-lookup"><span data-stu-id="e4957-129">Variables, structures, and class instances declared outside the body of a function.</span></span>
    
- <span data-ttu-id="e4957-130">Статические переменные, объявленные в теле функции.</span><span class="sxs-lookup"><span data-stu-id="e4957-130">Static variables declared within the body of a function.</span></span>
    
<span data-ttu-id="e4957-131">В этих двух случаях память задается в блоке памяти DLL, созданном для этого экземпляра DLL.</span><span class="sxs-lookup"><span data-stu-id="e4957-131">In these two cases, memory is set aside in the DLL's memory block created for this instance of the DLL.</span></span> <span data-ttu-id="e4957-132">Если другой экземпляр приложения загружает библиотеку DLL, он получает собственную копию этой памяти, чтобы избежать конфликтов для этих ресурсов извне этого экземпляра DLL.</span><span class="sxs-lookup"><span data-stu-id="e4957-132">If another application instance loads the DLL, it gets its own copy of that memory so that there is no contention for these resources from outside this instance of the DLL.</span></span>
  
 <span data-ttu-id="e4957-133">**Доступно только текущему потоку**</span><span class="sxs-lookup"><span data-stu-id="e4957-133">**Accessible only by the current thread**</span></span>
  
- <span data-ttu-id="e4957-134">Автоматические переменные в коде функции (включая аргументы функции).</span><span class="sxs-lookup"><span data-stu-id="e4957-134">Automatic variables within function code (including function arguments).</span></span>
    
<span data-ttu-id="e4957-135">В этом случае память задается в стеке для каждого экземпляра вызова функции.</span><span class="sxs-lookup"><span data-stu-id="e4957-135">In this case, memory is set aside on the stack for each instance of the function call.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e4957-136">Область динамически выделяемой памяти зависит от области указателя, указывающей на него: если указатель доступен всем потокам, память также будет иметь.</span><span class="sxs-lookup"><span data-stu-id="e4957-136">The scope of dynamically allocated memory depends on the scope of the pointer that points to it: if the pointer is accessible by all threads, the memory is also.</span></span> <span data-ttu-id="e4957-137">Если указатель является автоматической переменной в функции, выделенная память фактически является закрытой для этого потока.</span><span class="sxs-lookup"><span data-stu-id="e4957-137">If the pointer is an automatic variable in a function, the allocated memory is effectively private to that thread.</span></span> 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a><span data-ttu-id="e4957-138">Память, доступная только для одного потока: локальная память потока</span><span class="sxs-lookup"><span data-stu-id="e4957-138">Memory Accessible by Only One Thread: Thread-Local Memory</span></span>

<span data-ttu-id="e4957-139">С учетом того, что статические переменные в теле функции доступны всем потокам, функции, которые их используют, ясно являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="e4957-139">Given that static variables within the body of a function are accessible by all threads, functions that use them are clearly not thread safe.</span></span> <span data-ttu-id="e4957-140">Один экземпляр функции в одном потоке может изменить значение, в то время как другой экземпляр в другом потоке предполагается, что это совершенно другое.</span><span class="sxs-lookup"><span data-stu-id="e4957-140">One instance of the function on one thread could be changing the value while another instance on another thread is assuming it is something completely different.</span></span> 
  
<span data-ttu-id="e4957-141">Объявить статические переменные в функции можно двумя причинами:</span><span class="sxs-lookup"><span data-stu-id="e4957-141">There are two reasons for declaring static variables within a function:</span></span>
  
1. <span data-ttu-id="e4957-142">Статические данные можно хранить от одного вызова к другому.</span><span class="sxs-lookup"><span data-stu-id="e4957-142">Static data persist from one call to the next.</span></span>
    
2. <span data-ttu-id="e4957-143">Функция может безопасно возвратить указатель на статические данные.</span><span class="sxs-lookup"><span data-stu-id="e4957-143">A pointer to static data can safely be returned by the function.</span></span>
    
<span data-ttu-id="e4957-144">В первую очередь вы можете использовать данные, которые хранятся и имеют значение для всех вызовов функции: возможно, простой счетчик, увеличивающийся каждый раз при вызове функции в любом потоке, или структура, собирающая данные об использовании и производительности при каждом вызове.</span><span class="sxs-lookup"><span data-stu-id="e4957-144">In the case of first reason, you might want to have data that persists and has meaning for all calls to the function: perhaps a simple counter that is incremented every time the function is called on any thread, or a structure that collects usage and performance data on every call.</span></span> <span data-ttu-id="e4957-145">Вопрос заключается в защите общих данных или структуры данных.</span><span class="sxs-lookup"><span data-stu-id="e4957-145">The question is how to protect the shared data or data structure.</span></span> <span data-ttu-id="e4957-146">Это лучше всего сделать с помощью критического раздела, как описано в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="e4957-146">This is best done by using critical section as the next section explains.</span></span>
  
<span data-ttu-id="e4957-147">Если данные предназначены только для этого потока, что может быть из-за случая 1 и всегда является основанием 2, то вопрос состоит в том, как создать память, которая сохраняется, но доступна только из этого потока.</span><span class="sxs-lookup"><span data-stu-id="e4957-147">If the data is intended only for use by this thread, which could be the case for reason 1 and is always the case for reason 2, the question is how to create memory that persists but is only accessible from this thread.</span></span> <span data-ttu-id="e4957-148">Одним из решений является использование API локальной памяти потока (TLS).</span><span class="sxs-lookup"><span data-stu-id="e4957-148">One solution is to use the thread-local storage (TLS) API.</span></span>
  
<span data-ttu-id="e4957-149">Например, рассмотрим функцию, которая возвращает указатель на **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="e4957-149">For example, consider a function that returns a pointer to an **XLOPER**.</span></span>
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

<span data-ttu-id="e4957-150">Эта функция не является потокобезопасной, так как один поток может вернуть статическую **XLOPER12** , а другая перезаписать ее.</span><span class="sxs-lookup"><span data-stu-id="e4957-150">This function is not thread safe because one thread can return the static **XLOPER12** while another is overwriting it.</span></span> <span data-ttu-id="e4957-151">Вероятность того, что это **произошло, еще** лучше, если она должна передаваться в **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="e4957-151">The likelihood of this happening is greater still if the **XLOPER12** needs to be passed to **xlAutoFree12**.</span></span> <span data-ttu-id="e4957-152">Одно решение состоит в том, чтобы выделить **XLOPER12**, вернуть указатель на него и реализовать **xlAutoFree12** , чтобы освободить память **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="e4957-152">One solution is to allocate an **XLOPER12**, return a pointer to it, and implement **xlAutoFree12** so that the **XLOPER12** memory itself is freed.</span></span> <span data-ttu-id="e4957-153">Этот подход используется во многих примерах функций, показанных в разделе [Управление памятью в Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="e4957-153">This approach is used in many of the example functions shown in [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
```cs
LPXLOPER12 WINAPI mtr_safe_example_1(LPXLOPER12 pxArg)
{
// pxRetVal must be freed later by xlAutoFree12
    LPXLOPER12 pxRetVal = new XLOPER12;
// code sets pxRetVal to a function of pxArg ...
    pxRetVal->xltype |= xlbitDLLFree; // Needed for all types
    return pxRetVal; // xlAutoFree12 must free this
}
```

<span data-ttu-id="e4957-154">Такой подход проще реализовать, чем подход, описанный в следующем разделе, который основывается на API TLS, но у него есть некоторые недостатки.</span><span class="sxs-lookup"><span data-stu-id="e4957-154">This approach is simpler to implement than the approach outlined in the next section, which relies on the TLS API, but it has some disadvantages.</span></span> <span data-ttu-id="e4957-155">Сначала Excel должен вызвать **xlAutoFree**/ **xlAutoFree12** любого **типа возвращенной**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="e4957-155">First, Excel must call **xlAutoFree**/ **xlAutoFree12** whatever the type of the returned **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="e4957-156">Во-вторых, возникла проблема при возврате параметра **XLOPER**/ **XLOPER12**s, который возвращает возвращаемое значение вызова функции обратного вызова C API.</span><span class="sxs-lookup"><span data-stu-id="e4957-156">Second, there is a problem when returning **XLOPER**/ **XLOPER12**s that are the return value of a call to a C API callback function.</span></span> <span data-ttu-id="e4957-157">В параметре **XLOPER**/ **XLOPER12** может указываться память, которую необходимо освободить в Excel, но **XLOPER**/ **XLOPER12** сама по себе она должна быть освобождена таким же образом, как и выделенная.</span><span class="sxs-lookup"><span data-stu-id="e4957-157">The **XLOPER**/ **XLOPER12** may point to memory that needs to be freed by Excel, but the **XLOPER**/ **XLOPER12** itself must be freed in the same way it was allocated.</span></span> <span data-ttu-id="e4957-158">Если такая таблица **XLOPER**/ **должна использоваться** в качестве значения, возвращаемого функцией листа XLL, простой способ информирования **xlAutoFree**/ **xlAutoFree12** о необходимости освобождать оба указателя соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="e4957-158">If such an **XLOPER**/ **XLOPER12** is to be used as the return value of an XLL worksheet function, there is no easy way to inform **xlAutoFree**/ **xlAutoFree12** of the need to free both pointers in the appropriate way.</span></span> <span data-ttu-id="e4957-159">(Установка **кслбиткслфри** и **кслбитдллфри** не решает проблему, так как обработка **XLOPER/XLOPER12** в Excel с обоими наборами не определена и может изменяться от версии к версии.) Чтобы обойти эту проблему, XLL может выполнить глубокое копирование всех размещенных в Excel структур **и XLOPER12** , которые она возвращает на лист.</span><span class="sxs-lookup"><span data-stu-id="e4957-159">(Setting both the **xlbitXLFree** and **xlbitDLLFree** does not solve the problem, as the treatment of **XLOPER/XLOPER12s** in Excel with both set is undefined and might change from version to version.) To work around this problem, the XLL can make deep copies of all Excel-allocated **XLOPER/XLOPER12s** that it returns to the worksheet.</span></span> 
  
<span data-ttu-id="e4957-160">Решение, которое не позволяет избежать этих **ограничений, заключается**в заполнении и возврате локальных данных, подходов, которые требуют, чтобы **xlAutoFree/xlAutoFree12** не освобождают сам указатель в **XLOPER/XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="e4957-160">A solution that avoids these limitations is to populate and return a thread-local **XLOPER/XLOPER12**, an approach that necessitates that **xlAutoFree/xlAutoFree12** does not free the **XLOPER/XLOPER12** pointer itself.</span></span> 
  
```cs
LPXLOPER12 get_thread_local_xloper12(void);
LPXLOPER12 WINAPI mtr_safe_example_2(LPXLOPER12 pxArg)
{
    LPXLOPER12 pxRetVal = get_thread_local_xloper12();
// Code sets pxRetVal to a function of pxArg setting xlbitDLLFree or
// xlbitXLFree as required.
    return pxRetVal; // xlAutoFree12 must not free this pointer!
}

```

<span data-ttu-id="e4957-161">Следующий вопрос заключается в том, как настраивать и извлекать локальную память потока, другими словами, как реализовать функцию **get_thread_local_xloper12** в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="e4957-161">The next question is how to set up and retrieve the thread-local memory, in other words, how to implement the function **get_thread_local_xloper12** in the previous example.</span></span> <span data-ttu-id="e4957-162">Это выполняется с помощью API локального хранилища потока (TLS).</span><span class="sxs-lookup"><span data-stu-id="e4957-162">This is done using the Thread Local Storage (TLS) API.</span></span> <span data-ttu-id="e4957-163">Первым шагом является получение индекса TLS с помощью параметра **TlsAlloc**, который в конечном счете должен быть выпущен с помощью **тлсфри**.</span><span class="sxs-lookup"><span data-stu-id="e4957-163">The first step is to obtain a TLS index by using **TlsAlloc**, which must ultimately be released using **TlsFree**.</span></span> <span data-ttu-id="e4957-164">Оба варианта лучше всего выполняются из **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="e4957-164">Both are best accomplished from **DllMain**.</span></span>
  
```cs
// This implementation just calls a function to set up
// thread-local storage.
BOOL TLS_Action(DWORD Reason); // Could be in another module
BOOL WINAPI DllMain(HINSTANCE hDll, DWORD Reason, void *Reserved)
{
    return TLS_Action(Reason);
}
DWORD TlsIndex; // Module scope only if all TLS access in this module
BOOL TLS_Action(DWORD DllMainCallReason)
{
    switch (DllMainCallReason)
    {
    case DLL_PROCESS_ATTACH: // The DLL is being loaded.
        if((TlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES)
            return FALSE;
        break;
    case DLL_PROCESS_DETACH: // The DLL is being unloaded.
        TlsFree(TlsIndex); // Release the TLS index.
        break;
    }
    return TRUE;
}
```

<span data-ttu-id="e4957-165">После получения индекса следующим шагом будет выделить блок памяти для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="e4957-165">After you obtain the index, the next step is to allocate a block of memory for each thread.</span></span> <span data-ttu-id="e4957-166">[Документация по разработке Windows](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) рекомендует делать это каждый раз, когда функция обратного вызова **DllMain** вызывается с помощью события **DLL_THREAD_ATTACH** , и освобождает память на каждом **DLL_THREAD_DETACH**.</span><span class="sxs-lookup"><span data-stu-id="e4957-166">The [Windows Development Documentation](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) recommends doing this every time the **DllMain** callback function is called with a **DLL_THREAD_ATTACH** event, and freeing the memory on every **DLL_THREAD_DETACH**.</span></span> <span data-ttu-id="e4957-167">Тем не менее, следуя этим рекомендациям, Библиотека DLL сделает ненужную работу для потоков, не используемых для пересчета.</span><span class="sxs-lookup"><span data-stu-id="e4957-167">However, following this advice would cause your DLL to do unnecessary work for threads not used for recalculation.</span></span> 
  
<span data-ttu-id="e4957-168">Вместо этого лучше использовать стратегию выделения на основе первого использования.</span><span class="sxs-lookup"><span data-stu-id="e4957-168">Instead, it is better to use an allocate-on-first-use strategy.</span></span> <span data-ttu-id="e4957-169">Сначала необходимо определить структуру, которую необходимо выделить для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="e4957-169">First, you need to define a structure that you want to allocate for each thread.</span></span> <span data-ttu-id="e4957-170">Для предыдущих примеров, которые возвращают **XLOPER** или **XLOPER12**, достаточно выполнить следующие задачи, но вы можете создать любую структуру, удовлетворяющую Вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="e4957-170">For the previous examples that return **XLOPERs** or **XLOPER12s**, the following suffices, but you can create any structure that satisfies your needs.</span></span>
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

<span data-ttu-id="e4957-171">Следующая функция получает указатель на локальный экземпляр потока или выделяет его, если это первый вызов.</span><span class="sxs-lookup"><span data-stu-id="e4957-171">The following function gets a pointer to the thread-local instance, or allocates one if this is the first call.</span></span>
  
```cs
TLS_data *get_TLS_data(void)
{
// Get a pointer to this thread's static memory.
    void *pTLS = TlsGetValue(TlsIndex);
    if(!pTLS) // No TLS memory for this thread yet
    {
        if((pTLS = calloc(1, sizeof(TLS_data))) == NULL)
        // Display some error message (omitted).
            return NULL;
        TlsSetValue(TlsIndex, pTLS); // Associate with this thread
    }
    return (TLS_data *)pTLS;
}
```

<span data-ttu-id="e4957-172">Теперь можно увидеть, как получается локальная память **XLOPER/XLOPER12** потока: сначала вы получаете указатель на экземпляр **TLS_data**потока, а затем вернете указатель на **XLOPER/XLOPER12** , содержащийся в нем, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="e4957-172">Now you can see how the thread-local **XLOPER/XLOPER12** memory is obtained: first, you get a pointer to the thread's instance of **TLS_data**, and then you return a pointer to the **XLOPER/XLOPER12** contained within it, as follows.</span></span> 
  
```cs
LPXLOPER get_thread_local_xloper(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper_shared_ret_val);
    return NULL;
}
LPXLOPER12 get_thread_local_xloper12(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper12_shared_ret_val);
    return NULL;
}

```

<span data-ttu-id="e4957-173">Функции **mtr_safe_example_1** и **mtr_safe_example_2** могут быть зарегистрированы как потокобезопасные функции для работы с листом при запуске Excel.</span><span class="sxs-lookup"><span data-stu-id="e4957-173">The **mtr_safe_example_1** and **mtr_safe_example_2** functions can be registered as thread-safe worksheet functions when you are running Excel.</span></span> <span data-ttu-id="e4957-174">Однако вы не можете смешивать два подхода в одном XLL.</span><span class="sxs-lookup"><span data-stu-id="e4957-174">However, you cannot mix the two approaches in one XLL.</span></span> <span data-ttu-id="e4957-175">XLL может экспортировать только одну реализацию **xlAutoFree** и **xlAutoFree12**, а каждая стратегия использования памяти требует различных подходов.</span><span class="sxs-lookup"><span data-stu-id="e4957-175">Your XLL can only export one implementation of **xlAutoFree** and **xlAutoFree12**, and each memory strategy requires a different approach.</span></span> <span data-ttu-id="e4957-176">При использовании **mtr_safe_example_1**указатель, передаваемый в **xlAutoFree/xlAutoFree12** , должен быть освобожден вместе с любыми данными, на которые они указывают.</span><span class="sxs-lookup"><span data-stu-id="e4957-176">With **mtr_safe_example_1**, the pointer passed to **xlAutoFree/xlAutoFree12** must be freed along with any data it points to.</span></span> <span data-ttu-id="e4957-177">С **mtr_safe_example_2**только данные, указывающие на данные, должны быть освобождены.</span><span class="sxs-lookup"><span data-stu-id="e4957-177">With **mtr_safe_example_2**, only the pointed-to data should be freed.</span></span>
  
<span data-ttu-id="e4957-178">Кроме того, Windows предоставляет функцию **жеткуррентсреадид**, которая возвращает уникальный системный идентификатор текущего потока.</span><span class="sxs-lookup"><span data-stu-id="e4957-178">Windows also provides a function **GetCurrentThreadId**, which returns the current thread's unique system-wide ID.</span></span> <span data-ttu-id="e4957-179">Это предоставляет разработчику еще один способ сделать код потокобезопасным, а также присвоить конкретному потоку поведение.</span><span class="sxs-lookup"><span data-stu-id="e4957-179">This provides the developer with another way to make code thread safe, or to make its behavior thread specific.</span></span>
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a><span data-ttu-id="e4957-180">Память, доступная только для нескольких потоков: критические секции</span><span class="sxs-lookup"><span data-stu-id="e4957-180">Memory Accessible Only by More than One Thread: Critical Sections</span></span>

<span data-ttu-id="e4957-181">Необходимо защитить память чтения/записи, к которой можно получить доступ из нескольких потоков, используя критические разделы.</span><span class="sxs-lookup"><span data-stu-id="e4957-181">You should protect read/write memory that can be accessed by more than one thread using critical sections.</span></span> <span data-ttu-id="e4957-182">Для каждого блока памяти, который необходимо защитить, требуется именованный критический раздел.</span><span class="sxs-lookup"><span data-stu-id="e4957-182">You need a named critical section for each block of memory you want to protect.</span></span> <span data-ttu-id="e4957-183">Вы можете инициализировать их во время вызова функции **xlAutoOpen** и освободить их и задать значение null при вызове функции **xlAutoClose** .</span><span class="sxs-lookup"><span data-stu-id="e4957-183">You can initialize these during the call to the **xlAutoOpen** function, and release them and set them to null during the call to the **xlAutoClose** function.</span></span> <span data-ttu-id="e4957-184">Затем необходимо включить каждый доступ к защищенному блоку в пределах одной из двух вызовов **ентеркритикалсектион** и **леавекритикалсектион**.</span><span class="sxs-lookup"><span data-stu-id="e4957-184">You then need to contain each access to the protected block within a pair of calls to **EnterCriticalSection** and **LeaveCriticalSection**.</span></span> <span data-ttu-id="e4957-185">В любой момент времени в критический раздел может быть разрешен только один поток.</span><span class="sxs-lookup"><span data-stu-id="e4957-185">Only one thread is permitted into the critical section at any time.</span></span> <span data-ttu-id="e4957-186">Ниже приведен пример инициализации, неинициализации и использования раздела с именем **g_csSharedTable**.</span><span class="sxs-lookup"><span data-stu-id="e4957-186">Here is an example of the initialization, uninitialization, and use of a section called **g_csSharedTable**.</span></span>
  
```cs
CRITICAL_SECTION g_csSharedTable; // global scope (if required)
bool xll_initialised = false; // Only module scope needed
int WINAPI xlAutoOpen(void)
{
    if(xll_initialised)
        return 1;
// Other initialisation omitted
    InitializeCriticalSection(&g_csSharedTable);
    xll_initialised = true;
    return 1;
}
int WINAPI xlAutoClose(void)
{
    if(!xll_initialised)
        return 1;
// Other cleaning up omitted.
    DeleteCriticalSection(&g_csSharedTable);
    xll_initialised = false;
    return 1;
}
#define SHARED_TABLE_SIZE 1000 /* Some value consistent with the table */
bool read_shared_table_element(unsigned int index, double &d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    d = shared_table[index];
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
bool set_shared_table_element(unsigned int index, double d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    shared_table[index] = d;
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
```

<span data-ttu-id="e4957-187">Другой, возможно, более безопасный способ защиты блока памяти состоит в создании класса, который содержит собственные **critical_section** , а методы конструктора, деструктора и метода доступа отвечают за его использование.</span><span class="sxs-lookup"><span data-stu-id="e4957-187">Another, perhaps safer way of protecting a block of memory is to create a class that contains its own **CRITICAL_SECTION** and whose constructor, destructor, and accessor methods take care of its use.</span></span> <span data-ttu-id="e4957-188">В этом подходе Добавлено преимущество защиты объектов, которые могут быть инициализированы до **xlAutoOpen** , или после вызова **xlAutoClose** , однако следует быть внимательным при создании слишком большого количества критически важных разделов и издержек операционной системы, которые будут создаваться.</span><span class="sxs-lookup"><span data-stu-id="e4957-188">This approach has the added advantage of protecting objects that may be initialized before **xlAutoOpen** is run, or survive after **xlAutoClose** is called, but you should be careful about creating too many critical sections and the operating system overhead that this would create.</span></span> 
  
<span data-ttu-id="e4957-189">При наличии кода, который нуждается в одновременном доступе к нескольким блокам защищенной памяти, необходимо тщательно продумать порядок ввода и выхода критических разделов.</span><span class="sxs-lookup"><span data-stu-id="e4957-189">When you have code that needs access to more than one block of protected memory at the same time, you need to consider very carefully the order in which the critical sections are entered and exited.</span></span> <span data-ttu-id="e4957-190">Например, следующие две функции могут создать взаимоблокировку.</span><span class="sxs-lookup"><span data-stu-id="e4957-190">For example, the following two functions could create a deadlock.</span></span>
  
```cs
// WARNING: Do not copy this code. These two functions
// can produce a deadlock and are provided for
// example and illustration only.
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = shared_table_A[index];
// Critical sections should be exited in the order
// they were entered, NOT as shown here in this
// deliberately wrong illustration.
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
bool copy_shared_table_element_B_to_A(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableB);
    EnterCriticalSection(&g_csSharedTableA);
    shared_table_A[index] = shared_table_B[index];
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

<span data-ttu-id="e4957-191">Если первая функция в одном потоке вводит **g_csSharedTableA** , а вторая — в другом потоке, **g_csSharedTableB**, оба потока зависают.</span><span class="sxs-lookup"><span data-stu-id="e4957-191">If the first function on one thread enters **g_csSharedTableA** while the second on another thread enters **g_csSharedTableB**, both threads hang.</span></span> <span data-ttu-id="e4957-192">Правильный подход состоит в том, чтобы войти в последовательный порядок и выйти в обратном порядке, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="e4957-192">The correct approach is to enter in a consistent order and exit in the reverse order, as follows.</span></span>
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

<span data-ttu-id="e4957-193">Там, где это возможно, лучше всего использовать точку совместной работы с потоком, чтобы изолировать доступ к отдельным блокам, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="e4957-193">Where possible, it is better from a thread co-operation point of view to isolate access to distinct blocks, as shown here.</span></span>
  
```cs
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    double d = shared_table_A[index];
    LeaveCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = d;
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

<span data-ttu-id="e4957-194">При большом объеме конфликтов для общего ресурса, например, при частом коротком доступе к короткой длительности, следует рассмотреть возможность использования критической секции для прокрутки.</span><span class="sxs-lookup"><span data-stu-id="e4957-194">Where there is a lot of contention for a shared resource, such as frequent short-duration access requests, you should consider using the critical section's ability to spin.</span></span> <span data-ttu-id="e4957-195">Это методика, которая делает ожидание менее ресурсоемких ресурсов процессора.</span><span class="sxs-lookup"><span data-stu-id="e4957-195">This is a technique that makes waiting for the resource less processor-intensive.</span></span> <span data-ttu-id="e4957-196">Для этого можно использовать **инитиализекритикалсектионандспинкаунт** при инициализации раздела или **сеткритикалсектионспинкаунт** после инициализации, чтобы задать количество циклов потока перед тем, как оно станет доступным.</span><span class="sxs-lookup"><span data-stu-id="e4957-196">To do this, you can use either **InitializeCriticalSectionAndSpinCount** when initializing the section or **SetCriticalSectionSpinCount** once initialized, to set the number of times the thread loops before waiting for resources to become available.</span></span> <span data-ttu-id="e4957-197">Операция ожидания является дорогим, поэтому она позволяет избежать этого, если ресурс освобождается.</span><span class="sxs-lookup"><span data-stu-id="e4957-197">The wait operation is expensive, so spinning avoids this if the resource is freed in the meantime.</span></span> <span data-ttu-id="e4957-198">В системе с одним процессором счетчик прокруток фактически игнорируется, но вы можете указать его без ущерба.</span><span class="sxs-lookup"><span data-stu-id="e4957-198">On a single processor system, the spin count is effectively ignored, but you can still specify it without doing any harm.</span></span> <span data-ttu-id="e4957-199">Диспетчер кучи памяти использует счетчик прокрутки 4000.</span><span class="sxs-lookup"><span data-stu-id="e4957-199">The memory heap manager uses a spin count of 4000.</span></span> <span data-ttu-id="e4957-200">Дополнительные сведения об использовании критических разделов можно найти в документации по пакету SDK для Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e4957-200">For more information about the use of critical sections, see the Windows SDK documentation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e4957-201">См. также</span><span class="sxs-lookup"><span data-stu-id="e4957-201">See also</span></span>



[<span data-ttu-id="e4957-202">Управление памятью в Excel</span><span class="sxs-lookup"><span data-stu-id="e4957-202">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="e4957-203">Многопоточный пересчет в Excel</span><span class="sxs-lookup"><span data-stu-id="e4957-203">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="e4957-204">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="e4957-204">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

