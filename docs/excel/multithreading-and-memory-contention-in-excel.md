---
title: Многопоточность и конфликты памяти в Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- Многопоточность в excel, конфликтов памяти в Excel, функции [Excel 2007], являющихся потокобезопасными, являющихся потокобезопасными функции памяти локального потока [Excel 2007], [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fb0eddfff2f34307143bb896fd451de357f2b639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807317"
---
# <a name="multithreading-and-memory-contention-in-excel"></a><span data-ttu-id="21217-104">Многопоточность и конфликты памяти в Excel</span><span class="sxs-lookup"><span data-stu-id="21217-104">Multithreading and Memory Contention in Excel</span></span>

 <span data-ttu-id="21217-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="21217-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="21217-106">Чем Excel 2007 версиям Microsoft Excel использовать единый поток для всех расчетов на листе.</span><span class="sxs-lookup"><span data-stu-id="21217-106">Versions of Microsoft Excel earlier than Excel 2007 use a single thread for all worksheet calculations.</span></span> <span data-ttu-id="21217-107">Тем не менее начиная с версии Excel 2007, Excel может быть настроена на использование от 1 для 1024 параллельных потоков для расчета рабочего листа.</span><span class="sxs-lookup"><span data-stu-id="21217-107">However, starting in Excel 2007, Excel can be configured to use from 1 to 1024 concurrent threads for worksheet calculation.</span></span> <span data-ttu-id="21217-108">Компьютера с несколькими процессорами или многоядерная по умолчанию количество потоков равно числу процессоров или ядер.</span><span class="sxs-lookup"><span data-stu-id="21217-108">On a multi-processor or multi-core computer, the default number of threads is equal to the number of processors or cores.</span></span> <span data-ttu-id="21217-109">Таким образом являющихся потокобезопасными ячеек или ячеек, которые содержат только функции, которые являются потокобезопасными, может быть предоставлена параллельных потоков, может быть обычным пересчета логику для вычисления после их влияющие ячейки.</span><span class="sxs-lookup"><span data-stu-id="21217-109">Therefore, thread-safe cells, or cells that only contain functions that are thread safe, can be allotted to concurrent threads, subject to the usual recalculation logic of needing to be calculated after their precedents.</span></span>
  
## <a name="thread-safe-functions"></a><span data-ttu-id="21217-110">Функции потоками</span><span class="sxs-lookup"><span data-stu-id="21217-110">Thread-Safe Functions</span></span>

<span data-ttu-id="21217-111">Большая часть встроенных функций, начиная с версии Excel 2007 являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="21217-111">Most of the built-in worksheet functions starting in Excel 2007 are thread safe.</span></span> <span data-ttu-id="21217-112">Также можно записать и зарегистрировать функции XLL как потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="21217-112">You can also write and register XLL functions as being thread safe.</span></span> <span data-ttu-id="21217-113">Excel использует один поток (главный поток) для вызова всех команд, поток небезопасных функций, функций **xlAuto** (за исключением [xlAutoFree](xlautofree-xlautofree12.md) и **xlAutoFree12**) и COM и Visual Basic для приложений (VBA) функций.</span><span class="sxs-lookup"><span data-stu-id="21217-113">Excel uses one thread (its main thread) to call all commands, thread-unsafe functions, **xlAuto** functions (except [xlAutoFree](xlautofree-xlautofree12.md) and **xlAutoFree12**), and COM and Visual Basic for Applications (VBA) functions.</span></span>
  
<span data-ttu-id="21217-114">В функции XLL возвращает **XLOPER** или **XLOPER12** с набором **xlbitDLLFree** , Excel использует тот же поток, на котором был выполнен вызов функции для вызова **xlAutoFree** или **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="21217-114">Where an XLL function returns an **XLOPER** or **XLOPER12** with **xlbitDLLFree** set, Excel uses the same thread on which the function call was made to call **xlAutoFree** or **xlAutoFree12**.</span></span> <span data-ttu-id="21217-115">Вызов **xlAutoFree** или **xlAutoFree12** осуществляется до следующего вызова функции для этого потока.</span><span class="sxs-lookup"><span data-stu-id="21217-115">The call to **xlAutoFree** or **xlAutoFree12** is made before the next function call on that thread.</span></span> 
  
<span data-ttu-id="21217-116">Для разработчиков, XLL существует ряд преимуществ для создания функций являющихся потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="21217-116">For XLL developers, there are benefits for creating thread-safe functions:</span></span>
  
- <span data-ttu-id="21217-117">Они позволяют Excel, чтобы максимально эффективно использовать многопроцессорных или многоядерная компьютера.</span><span class="sxs-lookup"><span data-stu-id="21217-117">They allow Excel to make the most of a multi-processor or multi-core computer.</span></span>
    
- <span data-ttu-id="21217-118">Они открываются возможность намного эффективнее, чем можно выполнить с помощью удаленных серверов с помощью одного потока.</span><span class="sxs-lookup"><span data-stu-id="21217-118">They open up the possibility of using remote servers much more efficiently than can be done using a single thread.</span></span>
    
<span data-ttu-id="21217-119">Предположим, что у вас есть одним процессором компьютера, который был настроен для использования, например, *N* потоков.</span><span class="sxs-lookup"><span data-stu-id="21217-119">Suppose that you have a single-processor computer that has been configured to use, say,  *N*  threads.</span></span> <span data-ttu-id="21217-120">Предположим, что запущен электронной таблицы, что делает большое число вызовов функции XLL, в свою очередь отправляет запрос для данных или вычислений, выполняемых для удаленного сервера или кластера серверов.</span><span class="sxs-lookup"><span data-stu-id="21217-120">Suppose that a spreadsheet is running that makes a large number of calls to an XLL function that in turn sends a request for data or for a calculation to be performed to a remote server or cluster of servers.</span></span> <span data-ttu-id="21217-121">Может быть топологии дерева зависимостей Excel вызвать функцию N раз почти одновременно.</span><span class="sxs-lookup"><span data-stu-id="21217-121">Subject to the topology of the dependency tree, Excel could call the function N times almost simultaneously.</span></span> <span data-ttu-id="21217-122">При условии, что сервер или серверы, достаточно fast или параллельный, времени пересчета листа может добиться по мере фактор 1/N.</span><span class="sxs-lookup"><span data-stu-id="21217-122">Provided that the server or servers are sufficiently fast or parallel, the recalculation time of the spreadsheet could be reduced by as much as a factor of 1/N.</span></span> 
  
<span data-ttu-id="21217-123">Ключевые проблемы в создание функций потоками правильно обрабатывает конкуренции за ресурсы.</span><span class="sxs-lookup"><span data-stu-id="21217-123">The key issue in writing thread-safe functions is handling contention for resources correctly.</span></span> <span data-ttu-id="21217-124">Обычно это означает конфликтов памяти, и его можно разделить на две проблемы:</span><span class="sxs-lookup"><span data-stu-id="21217-124">This usually means memory contention, and it can be broken down into two issues:</span></span>
  
- <span data-ttu-id="21217-125">Как создать объем памяти, вы знаете, будут использоваться только потока.</span><span class="sxs-lookup"><span data-stu-id="21217-125">How to create memory that you know will only be used by this thread.</span></span>
    
- <span data-ttu-id="21217-126">Как убедиться, что к памяти с несколькими потоками безопасно.</span><span class="sxs-lookup"><span data-stu-id="21217-126">How to ensure that shared memory is accessed by multiple threads safely.</span></span>
    
<span data-ttu-id="21217-127">В первую очередь необходимо иметь в виду — какой объем памяти в надстройке XLL доступны для всех потоков, и что доступно только из текущего потока.</span><span class="sxs-lookup"><span data-stu-id="21217-127">The first thing to be aware of is what memory in an XLL is accessible by all threads, and what is only accessible by the currently executing thread.</span></span>
  
 <span data-ttu-id="21217-128">**Доступны для всех потоков**</span><span class="sxs-lookup"><span data-stu-id="21217-128">**Accessible by all threads**</span></span>
  
- <span data-ttu-id="21217-129">Переменные, структуры и экземпляры класса объявлен вне тела функции.</span><span class="sxs-lookup"><span data-stu-id="21217-129">Variables, structures, and class instances declared outside the body of a function.</span></span>
    
- <span data-ttu-id="21217-130">Статические переменные, объявляемые в теле функции.</span><span class="sxs-lookup"><span data-stu-id="21217-130">Static variables declared within the body of a function.</span></span>
    
<span data-ttu-id="21217-131">В этих двух случаях памяти резервируется в блоке памяти библиотеки DLL, созданные для этого экземпляра библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="21217-131">In these two cases, memory is set aside in the DLL's memory block created for this instance of the DLL.</span></span> <span data-ttu-id="21217-132">Если другой экземпляр приложения загружает библиотеку DLL, получает собственную копию памяти, чтобы не нет конфликтов для этих ресурсов из за пределами этого экземпляра библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="21217-132">If another application instance loads the DLL, it gets its own copy of that memory so that there is no contention for these resources from outside this instance of the DLL.</span></span>
  
 <span data-ttu-id="21217-133">**Доступны только для текущего потока**</span><span class="sxs-lookup"><span data-stu-id="21217-133">**Accessible only by the current thread**</span></span>
  
- <span data-ttu-id="21217-134">Автоматическое переменные в коде функции (в том числе аргументы функций).</span><span class="sxs-lookup"><span data-stu-id="21217-134">Automatic variables within function code (including function arguments).</span></span>
    
<span data-ttu-id="21217-135">В этом случае памяти резервируется в стеке для каждого экземпляра вызова функции.</span><span class="sxs-lookup"><span data-stu-id="21217-135">In this case, memory is set aside on the stack for each instance of the function call.</span></span>
  
> [!NOTE]
> <span data-ttu-id="21217-136">Область динамически выделенной памяти зависит от области, указывающий на него указатель мыши: если указатель находится доступны для всех потоков, также является объем памяти.</span><span class="sxs-lookup"><span data-stu-id="21217-136">The scope of dynamically allocated memory depends on the scope of the pointer that points to it: if the pointer is accessible by all threads, the memory is also.</span></span> <span data-ttu-id="21217-137">Если указатель находится автоматическую переменную в функцию, выделенной памяти эффективно закрытый этого потока.</span><span class="sxs-lookup"><span data-stu-id="21217-137">If the pointer is an automatic variable in a function, the allocated memory is effectively private to that thread.</span></span> 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a><span data-ttu-id="21217-138">Только один поток объем доступной памяти: локальной памяти потока</span><span class="sxs-lookup"><span data-stu-id="21217-138">Memory Accessible by Only One Thread: Thread-Local Memory</span></span>

<span data-ttu-id="21217-139">Учитывая, что статические переменные в теле функции будут доступны для всех потоков, функции, использующие их четко не являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="21217-139">Given that static variables within the body of a function are accessible by all threads, functions that use them are clearly not thread safe.</span></span> <span data-ttu-id="21217-140">Один экземпляр функции в одном потоке могут изменять значение во время другого экземпляра в другом потоке предполагается, что это совершенно другой.</span><span class="sxs-lookup"><span data-stu-id="21217-140">One instance of the function on one thread could be changing the value while another instance on another thread is assuming it is something completely different.</span></span> 
  
<span data-ttu-id="21217-141">Существует две причины объявление статических переменных в функцию.</span><span class="sxs-lookup"><span data-stu-id="21217-141">There are two reasons for declaring static variables within a function:</span></span>
  
1. <span data-ttu-id="21217-142">Статические данные сохраняются из одного вызова к следующему.</span><span class="sxs-lookup"><span data-stu-id="21217-142">Static data persist from one call to the next.</span></span>
    
2. <span data-ttu-id="21217-143">Указатель на статические данные безопасно можно получить с помощью функции.</span><span class="sxs-lookup"><span data-stu-id="21217-143">A pointer to static data can safely be returned by the function.</span></span>
    
<span data-ttu-id="21217-144">В случае первая причина может потребоваться данными, сохраняет и имеет значение для всех вызовов функции: возможно простой счетчик, который увеличивается каждый раз вызывает функцию в любом потоке или структуру, которая собирает данные об использовании и производительности на ночь вызов трана.</span><span class="sxs-lookup"><span data-stu-id="21217-144">In the case of first reason, you might want to have data that persists and has meaning for all calls to the function: perhaps a simple counter that is incremented every time the function is called on any thread, or a structure that collects usage and performance data on every call.</span></span> <span data-ttu-id="21217-145">Вопрос является защита общих данных или структуру данных.</span><span class="sxs-lookup"><span data-stu-id="21217-145">The question is how to protect the shared data or data structure.</span></span> <span data-ttu-id="21217-146">Лучше всего этого с помощью критический раздел, как в следующем разделе поясняются.</span><span class="sxs-lookup"><span data-stu-id="21217-146">This is best done by using critical section as the next section explains.</span></span>
  
<span data-ttu-id="21217-147">Если данные предназначен только для использования в данный поток, который может быть установлено по причине 1 и происходит всегда по причине 2, вопрос является то, как создание объем памяти, сохраняется, но доступно только из этого потока.</span><span class="sxs-lookup"><span data-stu-id="21217-147">If the data is intended only for use by this thread, which could be the case for reason 1 and is always the case for reason 2, the question is how to create memory that persists but is only accessible from this thread.</span></span> <span data-ttu-id="21217-148">Одним из решений является использование локальной памяти потока (TLS) API.</span><span class="sxs-lookup"><span data-stu-id="21217-148">One solution is to use the thread-local storage (TLS) API.</span></span>
  
<span data-ttu-id="21217-149">Например рассмотрим функция, которая возвращает указатель на **структуру XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="21217-149">For example, consider a function that returns a pointer to an **XLOPER**.</span></span>
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

<span data-ttu-id="21217-150">Эта функция не потокобезопасными, так как один поток может возвратить статические **XLOPER12** , в то время как другой перезаписывает ее.</span><span class="sxs-lookup"><span data-stu-id="21217-150">This function is not thread safe because one thread can return the static **XLOPER12** while another is overwriting it.</span></span> <span data-ttu-id="21217-151">Вероятность такого события еще выше, если **XLOPER12** должно быть передано **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="21217-151">The likelihood of this happening is greater still if the **XLOPER12** needs to be passed to **xlAutoFree12**.</span></span> <span data-ttu-id="21217-152">Решением является выделить **XLOPER12**и возвращает указатель на него применить **xlAutoFree12** , чтобы освободить память **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="21217-152">One solution is to allocate an **XLOPER12**, return a pointer to it, and implement **xlAutoFree12** so that the **XLOPER12** memory itself is freed.</span></span> <span data-ttu-id="21217-153">Такой подход используется в многие функции примере показано [Управление памятью в Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="21217-153">This approach is used in many of the example functions shown in [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
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

<span data-ttu-id="21217-154">Такой подход проще реализовать, чем подход, описанные в следующем разделе основывается на TLS API, но имеет несколько недостатков.</span><span class="sxs-lookup"><span data-stu-id="21217-154">This approach is simpler to implement than the approach outlined in the next section, which relies on the TLS API, but it has some disadvantages.</span></span> <span data-ttu-id="21217-155">Во-первых, Excel необходимо вызвать **xlAutoFree**/ **xlAutoFree12** любой тип возвращаемых **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="21217-155">First, Excel must call **xlAutoFree**/ **xlAutoFree12** whatever the type of the returned **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="21217-156">Во-вторых, имеется проблема при возврате **XLOPER**/ s**XLOPER12**, которые возвращаемое значение для вызова функции обратного вызова интерфейса API для C.</span><span class="sxs-lookup"><span data-stu-id="21217-156">Second, there is a problem when returning **XLOPER**/ **XLOPER12**s that are the return value of a call to a C API callback function.</span></span> <span data-ttu-id="21217-157">**XLOPER**/ **XLOPER12** могут указывать на объем памяти, который необходимо освободить путем Excel, но **XLOPER**/ **XLOPER12** самого освобождения так же, как было выполнено выделение.</span><span class="sxs-lookup"><span data-stu-id="21217-157">The **XLOPER**/ **XLOPER12** may point to memory that needs to be freed by Excel, but the **XLOPER**/ **XLOPER12** itself must be freed in the same way it was allocated.</span></span> <span data-ttu-id="21217-158">Если такие **XLOPER**/ **XLOPER12** — для использования в качестве возвращаемое значение функции листа XLL, невозможно просто для оповещения **xlAutoFree**/ **xlAutoFree12** требуется дополнительная обоих указатели тем способом.</span><span class="sxs-lookup"><span data-stu-id="21217-158">If such an **XLOPER**/ **XLOPER12** is to be used as the return value of an XLL worksheet function, there is no easy way to inform **xlAutoFree**/ **xlAutoFree12** of the need to free both pointers in the appropriate way.</span></span> <span data-ttu-id="21217-159">(Установка **xlbitXLFree** и **xlbitDLLFree** не помогает, как лечения **XLOPER/XLOPER12s** в Excel с помощью оба набора не определен и может изменяться от версии на другую.) Чтобы обойти эту проблему, XLL можно сделать глубокие копии всех выделенных Excel **XLOPER/XLOPER12s** , которая возвращает в лист.</span><span class="sxs-lookup"><span data-stu-id="21217-159">(Setting both the **xlbitXLFree** and **xlbitDLLFree** does not solve the problem, as the treatment of **XLOPER/XLOPER12s** in Excel with both set is undefined and might change from version to version.) To work around this problem, the XLL can make deep copies of all Excel-allocated **XLOPER/XLOPER12s** that it returns to the worksheet.</span></span> 
  
<span data-ttu-id="21217-160">Решение, которое позволяет избежать этих ограничений для заполнения и возврата локального потока **XLOPER и XLOPER12**, подхода необходимо, **xlAutoFree/xlAutoFree12** без использования сам указатель **XLOPER и XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="21217-160">A solution that avoids these limitations is to populate and return a thread-local **XLOPER/XLOPER12**, an approach that necessitates that **xlAutoFree/xlAutoFree12** does not free the **XLOPER/XLOPER12** pointer itself.</span></span> 
  
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

<span data-ttu-id="21217-161">Следующий вопрос является, как настраивать и извлекать локальную память потока, иными словами, как реализовать функцию **get_thread_local_xloper12** в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="21217-161">The next question is how to set up and retrieve the thread-local memory, in other words, how to implement the function **get_thread_local_xloper12** in the previous example.</span></span> <span data-ttu-id="21217-162">Это делается с помощью потока локального хранилища (TLS) API.</span><span class="sxs-lookup"><span data-stu-id="21217-162">This is done using the Thread Local Storage (TLS) API.</span></span> <span data-ttu-id="21217-163">Сначала необходимо получить индекс TLS с помощью **TlsAlloc**, который в конечном счете освобождается с помощью **TlsFree**.</span><span class="sxs-lookup"><span data-stu-id="21217-163">The first step is to obtain a TLS index by using **TlsAlloc**, which must ultimately be released using **TlsFree**.</span></span> <span data-ttu-id="21217-164">Как лучше всего выполняются из **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="21217-164">Both are best accomplished from **DllMain**.</span></span>
  
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

<span data-ttu-id="21217-165">После получения индекса, следующим шагом является выделить блок памяти для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="21217-165">After you obtain the index, the next step is to allocate a block of memory for each thread.</span></span> <span data-ttu-id="21217-166">[Документация по разработке Windows](http://msdn.microsoft.com/en-us/library/ms682583%28VS.85%29.aspx) рекомендуется выполнять это каждый раз **DllMain** функции обратного вызова вызывается с **DLL_THREAD_ATTACH** событий и освобождения памяти на каждом **DLL_THREAD_DETACH**.</span><span class="sxs-lookup"><span data-stu-id="21217-166">The [Windows Development Documentation](http://msdn.microsoft.com/en-us/library/ms682583%28VS.85%29.aspx) recommends doing this every time the **DllMain** callback function is called with a **DLL_THREAD_ATTACH** event, and freeing the memory on every **DLL_THREAD_DETACH**.</span></span> <span data-ttu-id="21217-167">Тем не менее выполнив этот совет вызовет библиотеки DLL выполнить ненужных рабочих потоков, не используется для пересчета.</span><span class="sxs-lookup"><span data-stu-id="21217-167">However, following this advice would cause your DLL to do unnecessary work for threads not used for recalculation.</span></span> 
  
<span data-ttu-id="21217-168">Вместо этого лучше использовать стратегию распределения на первом использовании.</span><span class="sxs-lookup"><span data-stu-id="21217-168">Instead, it is better to use an allocate-on-first-use strategy.</span></span> <span data-ttu-id="21217-169">Во-первых необходимо определить структуру, который вы хотите выделить для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="21217-169">First, you need to define a structure that you want to allocate for each thread.</span></span> <span data-ttu-id="21217-170">Предыдущие примеры, которые возвращают **XLOPERs** или **XLOPER12s**следующие достаточно, но можно создать любое структуру, которая должна удовлетворять потребностям.</span><span class="sxs-lookup"><span data-stu-id="21217-170">For the previous examples that return **XLOPERs** or **XLOPER12s**, the following suffices, but you can create any structure that satisfies your needs.</span></span>
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

<span data-ttu-id="21217-171">Следующая функция получает указатель на локальный экземпляр потока или выделяет один, если это первый вызов.</span><span class="sxs-lookup"><span data-stu-id="21217-171">The following function gets a pointer to the thread-local instance, or allocates one if this is the first call.</span></span>
  
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

<span data-ttu-id="21217-172">Теперь можно увидеть способ получения памяти **XLOPER и XLOPER12** локального потока: во-первых, получить указатель на экземпляр потока **TLS_data**, и затем возвращает указатель на **XLOPER и XLOPER12** , содержащиеся в нем, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="21217-172">Now you can see how the thread-local **XLOPER/XLOPER12** memory is obtained: first, you get a pointer to the thread's instance of **TLS_data**, and then you return a pointer to the **XLOPER/XLOPER12** contained within it, as follows.</span></span> 
  
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

<span data-ttu-id="21217-173">Функции **mtr_safe_example_1** и **mtr_safe_example_2** могут быть зарегистрирована как функции листа потоками при запуске Excel.</span><span class="sxs-lookup"><span data-stu-id="21217-173">The **mtr_safe_example_1** and **mtr_safe_example_2** functions can be registered as thread-safe worksheet functions when you are running Excel.</span></span> <span data-ttu-id="21217-174">Тем не менее нельзя смешивать два подхода в один XLL.</span><span class="sxs-lookup"><span data-stu-id="21217-174">However, you cannot mix the two approaches in one XLL.</span></span> <span data-ttu-id="21217-175">Ваше XLL можно экспортировать только один реализации **xlAutoFree** и **xlAutoFree12**и каждой стратегии памяти требуется используется другой подход.</span><span class="sxs-lookup"><span data-stu-id="21217-175">Your XLL can only export one implementation of **xlAutoFree** and **xlAutoFree12**, and each memory strategy requires a different approach.</span></span> <span data-ttu-id="21217-176">С помощью **mtr_safe_example_1**указатель, переданный **xlAutoFree/xlAutoFree12** освобождения вместе с данными ссылается на.</span><span class="sxs-lookup"><span data-stu-id="21217-176">With **mtr_safe_example_1**, the pointer passed to **xlAutoFree/xlAutoFree12** must be freed along with any data it points to.</span></span> <span data-ttu-id="21217-177">С помощью **mtr_safe_example_2**нужно освободить только указывает на данные.</span><span class="sxs-lookup"><span data-stu-id="21217-177">With **mtr_safe_example_2**, only the pointed-to data should be freed.</span></span>
  
<span data-ttu-id="21217-178">Windows также предоставляет функцию **GetCurrentThreadId**, который возвращает текущий поток уникальный системных идентификатор.</span><span class="sxs-lookup"><span data-stu-id="21217-178">Windows also provides a function **GetCurrentThreadId**, which returns the current thread's unique system-wide ID.</span></span> <span data-ttu-id="21217-179">Это обеспечивает разработчик с другим способом сделать надежных потока кода или сделать его поток поведение определенных.</span><span class="sxs-lookup"><span data-stu-id="21217-179">This provides the developer with another way to make code thread safe, or to make its behavior thread specific.</span></span>
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a><span data-ttu-id="21217-180">Только с более одного потока объем доступной памяти: критических разделов</span><span class="sxs-lookup"><span data-stu-id="21217-180">Memory Accessible Only by More than One Thread: Critical Sections</span></span>

<span data-ttu-id="21217-181">Следует защитить чтения/записи памяти, который может осуществляться более одного потока, с помощью критических секций.</span><span class="sxs-lookup"><span data-stu-id="21217-181">You should protect read/write memory that can be accessed by more than one thread using critical sections.</span></span> <span data-ttu-id="21217-182">Именованные критический раздел требуются для каждого блока памяти, который необходимо защитить.</span><span class="sxs-lookup"><span data-stu-id="21217-182">You need a named critical section for each block of memory you want to protect.</span></span> <span data-ttu-id="21217-183">Можно инициализировать ходе вызова функции **xlAutoOpen** и освобождать их и присвойте их значения NULL во время вызова функции **xlAutoClose** .</span><span class="sxs-lookup"><span data-stu-id="21217-183">You can initialize these during the call to the **xlAutoOpen** function, and release them and set them to null during the call to the **xlAutoClose** function.</span></span> <span data-ttu-id="21217-184">Вы должны содержать каждого доступ в защищенный блок в паре вызовы **EnterCriticalSection** и **LeaveCriticalSection**.</span><span class="sxs-lookup"><span data-stu-id="21217-184">You then need to contain each access to the protected block within a pair of calls to **EnterCriticalSection** and **LeaveCriticalSection**.</span></span> <span data-ttu-id="21217-185">В разделе критические может только один поток в любое время.</span><span class="sxs-lookup"><span data-stu-id="21217-185">Only one thread is permitted into the critical section at any time.</span></span> <span data-ttu-id="21217-186">Ниже приведен пример инициализации, инициализации и использования секции с именем **g_csSharedTable**.</span><span class="sxs-lookup"><span data-stu-id="21217-186">Here is an example of the initialization, uninitialization, and use of a section called **g_csSharedTable**.</span></span>
  
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

<span data-ttu-id="21217-187">Другой, возможно, более безопасным способом защиты блока памяти является создание класса, содержащего свою собственную **CRITICAL_SECTION** и которого конструктор, деструктор и методы доступа к взяла на себя его использования.</span><span class="sxs-lookup"><span data-stu-id="21217-187">Another, perhaps safer way of protecting a block of memory is to create a class that contains its own **CRITICAL_SECTION** and whose constructor, destructor, and accessor methods take care of its use.</span></span> <span data-ttu-id="21217-188">Такой подход имеет преимущество Защита объектов, которые могут быть инициализирован перед **xlAutoOpen** запускается или миру после вызова **xlAutoClose** , однако следует проявлять осторожность сведения о создании слишком много критические разделы и операционной системы Дополнительная нагрузка, при этом будет создана.</span><span class="sxs-lookup"><span data-stu-id="21217-188">This approach has the added advantage of protecting objects that may be initialized before **xlAutoOpen** is run, or survive after **xlAutoClose** is called, but you should be careful about creating too many critical sections and the operating system overhead that this would create.</span></span> 
  
<span data-ttu-id="21217-189">При наличии кода, который требуется доступ к более одного блока защищенной памяти в то же время, необходимо тщательно рассмотрите порядок введены и выхода из критических разделов.</span><span class="sxs-lookup"><span data-stu-id="21217-189">When you have code that needs access to more than one block of protected memory at the same time, you need to consider very carefully the order in which the critical sections are entered and exited.</span></span> <span data-ttu-id="21217-190">Например следующие две функции создать взаимоблокировки.</span><span class="sxs-lookup"><span data-stu-id="21217-190">For example, the following two functions could create a deadlock.</span></span>
  
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

<span data-ttu-id="21217-191">Если первая функция в одном потоке вводит **g_csSharedTableA** , а второй — в другом потоке вводит **g_csSharedTableB**, зависание оба потока.</span><span class="sxs-lookup"><span data-stu-id="21217-191">If the first function on one thread enters **g_csSharedTableA** while the second on another thread enters **g_csSharedTableB**, both threads hang.</span></span> <span data-ttu-id="21217-192">— Это правильный подход для ввода в едином порядке и выйдите из в обратном порядке, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="21217-192">The correct approach is to enter in a consistent order and exit in the reverse order, as follows.</span></span>
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

<span data-ttu-id="21217-193">Где это возможно, лучше с потока сотрудничестве точка зрения изоляции доступа для различных блоки, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="21217-193">Where possible, it is better from a thread co-operation point of view to isolate access to distinct blocks, as shown here.</span></span>
  
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

<span data-ttu-id="21217-194">При наличии большого числа конфликтов для общего ресурса, такие как запросы часто используемые кратковременного доступа, можно использовать возможности критический раздел на вращение.</span><span class="sxs-lookup"><span data-stu-id="21217-194">Where there is a lot of contention for a shared resource, such as frequent short-duration access requests, you should consider using the critical section's ability to spin.</span></span> <span data-ttu-id="21217-195">Это способ, с помощью ожидание ресурса меньше процессор.</span><span class="sxs-lookup"><span data-stu-id="21217-195">This is a technique that makes waiting for the resource less processor-intensive.</span></span> <span data-ttu-id="21217-196">Для этого можно использовать либо **InitializeCriticalSectionAndSpinCount** при инициализации раздел или **SetCriticalSectionSpinCount** после инициализации, чтобы задать число попыток потока циклически до завершения ресурсы, которые становятся доступно.</span><span class="sxs-lookup"><span data-stu-id="21217-196">To do this, you can use either **InitializeCriticalSectionAndSpinCount** when initializing the section or **SetCriticalSectionSpinCount** once initialized, to set the number of times the thread loops before waiting for resources to become available.</span></span> <span data-ttu-id="21217-197">Операция ожидания дорогим, поэтому прокрутка позволяет избежать таких ресурс освобождается на данном этапе.</span><span class="sxs-lookup"><span data-stu-id="21217-197">The wait operation is expensive, so spinning avoids this if the resource is freed in the meantime.</span></span> <span data-ttu-id="21217-198">В системе одного процессора число смен хэша эффективно игнорируется, но вы по-прежнему можно указать без внесения любой вред.</span><span class="sxs-lookup"><span data-stu-id="21217-198">On a single processor system, the spin count is effectively ignored, but you can still specify it without doing any harm.</span></span> <span data-ttu-id="21217-199">Диспетчер кучи памяти использует число смен хэша 4000.</span><span class="sxs-lookup"><span data-stu-id="21217-199">The memory heap manager uses a spin count of 4000.</span></span> <span data-ttu-id="21217-200">Дополнительные сведения об использовании критические разделы документации пакета SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="21217-200">For more information about the use of critical sections, see the Windows SDK documentation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="21217-201">См. также</span><span class="sxs-lookup"><span data-stu-id="21217-201">See also</span></span>



[<span data-ttu-id="21217-202">���������� ������� � Excel</span><span class="sxs-lookup"><span data-stu-id="21217-202">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="21217-203">�������������� �������� � Excel</span><span class="sxs-lookup"><span data-stu-id="21217-203">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="21217-204">Диспетчер надстроек и функции XLL интерфейса</span><span class="sxs-lookup"><span data-stu-id="21217-204">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

