---
title: Многопоточные вычисления в Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- потоками ячеек [excel 2007], многопоточность в Excel, параллельных задач [Excel 2007], являющихся потокобезопасными функции [Excel 2007], многопоточные вычисления [Excel 2007], MTR [Excel 2007], регистрация в качестве потокобезопасными, пересчета [функции XLL [Excel 2007] Excel 2007], многопоточные, объем памяти, конфликтов [Excel 2007], регистрация XLL функции как поток безопасные небезопасные функции [Excel 2007], [Excel 2007]
localization_priority: Normal
ms.assetid: c6c831f1-4be1-4dcc-a0fa-c26052ec53c9
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 010a1029e0bf5ba1a36b324ebd402f6e90603fb9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807310"
---
# <a name="multithreaded-recalculation-in-excel"></a><span data-ttu-id="ab240-104">Многопоточные вычисления в Excel</span><span class="sxs-lookup"><span data-stu-id="ab240-104">Multithreaded recalculation in Excel</span></span>

<span data-ttu-id="ab240-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ab240-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ab240-106">Microsoft Office Excel 2007 был первая версия Excel для использования многопоточные вычисления (MTR) таблиц.</span><span class="sxs-lookup"><span data-stu-id="ab240-106">Microsoft Office Excel 2007 was the first version of Excel to use multithreaded recalculation (MTR) of worksheets.</span></span> <span data-ttu-id="ab240-107">Вы можете настроить Excel для до 1024 параллельных потоков пересчет, независимо от количества процессоров или ядер процессора на компьютере.</span><span class="sxs-lookup"><span data-stu-id="ab240-107">You can configure Excel to use up to 1024 concurrent threads when recalculating, regardless of the number of processors or processor cores on the computer.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ab240-108">С каждым потоком связаны затраты ресурсов операционной системы, поэтому не следует настраивать в Excel использование большего числа потоков, чем необходимо.</span><span class="sxs-lookup"><span data-stu-id="ab240-108">There is an operating system overhead associated with each thread, so you should not configure Excel to use more threads than you need.</span></span> 
  
<span data-ttu-id="ab240-109">Если компьютер имеет несколько процессоров или ядер, за эффективное распределение потоков между процессорами отвечает операционная система.</span><span class="sxs-lookup"><span data-stu-id="ab240-109">If the computer has multiple processors or processor cores, the operating system takes responsibility for allocating the threads to the processors in the most efficient way.</span></span>
  
## <a name="excel-mtr-overview"></a><span data-ttu-id="ab240-110">Обзор Excel MTR</span><span class="sxs-lookup"><span data-stu-id="ab240-110">Excel MTR overview</span></span>

<span data-ttu-id="ab240-p102">Excel пытается определить части цепочки вычисления, которые можно пересчитывать одновременно в разных потоках. Ниже в качестве примера приведено очень простое дерево (где "x ← y" означает, что y зависит только от x).</span><span class="sxs-lookup"><span data-stu-id="ab240-p102">Excel tries to identify parts of the calculation chain that can be recalculated concurrently on different threads. The following very simple tree (where x ← y means y only depends on x) shows an example of this.</span></span>
  
<span data-ttu-id="ab240-113">**На рисунке 1. Параллельное вычисление на различных потоках**</span><span class="sxs-lookup"><span data-stu-id="ab240-113">**Figure 1. Calculating concurrently on different threads**</span></span>

<span data-ttu-id="ab240-114">![Вычисление одновременно на различных потоках] (media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Вычисление одновременно на различных потоках")</span><span class="sxs-lookup"><span data-stu-id="ab240-114">![Calculating concurrently on different threads](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Calculating concurrently on different threads")</span></span>
  
<span data-ttu-id="ab240-115">Когда выполнено вычисление для ячейки A1, можно последовательно выполнить вычисление для ячеек A2 и A3 в одном потоке, в то время как в другом потоке последовательно выполняются вычисления для B1 и C1. Это возможно при условии, что все ячейки потокобезопасны.</span><span class="sxs-lookup"><span data-stu-id="ab240-115">After A1 is calculated, A2 and then A3 can be calculated on one thread, while B1 and then C1 can be calculated on another, assuming all the cells are thread safe.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ab240-116">Ячейка потоками терминов означает, что ячейка, которая содержит только функции являющихся потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="ab240-116">The term thread-safe cell means a cell that only contains thread-safe functions.</span></span> <span data-ttu-id="ab240-117">Подробное описание какой используется и не являющихся потокобезопасными [и является не считаются потока безопасных по Excel](#xl2007xllsdk_threadsafe).</span><span class="sxs-lookup"><span data-stu-id="ab240-117">What is and is not thread-safe is detailed [What Is and Is Not Considered Thread Safe by Excel](#xl2007xllsdk_threadsafe).</span></span> 
  
<span data-ttu-id="ab240-118">Наиболее удобным книги содержат более сложных деревья зависимостей, чем в этом примере.</span><span class="sxs-lookup"><span data-stu-id="ab240-118">Most practical workbooks contain far more complex dependency trees than this example.</span></span> <span data-ttu-id="ab240-119">Кроме того время пересчета ячейки не может быть известен, пока вычисление выполняется и не может значительно изменяться в зависимости от аргументы функций.</span><span class="sxs-lookup"><span data-stu-id="ab240-119">Moreover, the recalculation time of a cell cannot be known until a calculation is done and can vary greatly depending on the functions' arguments.</span></span> <span data-ttu-id="ab240-120">Чтобы получить наилучшие результаты, пытается улучшить порядок вычисления на каждом вычислений, пока не будет невозможно без дополнительных оптимизации Excel.</span><span class="sxs-lookup"><span data-stu-id="ab240-120">To obtain the best results, Excel tries to improve the calculation order on every calculation until no further optimization is possible.</span></span>
  
<span data-ttu-id="ab240-121">Приложение Excel использует один основной поток для запуска или выполнения следующего:</span><span class="sxs-lookup"><span data-stu-id="ab240-121">Excel uses a single main thread to run or execute the following:</span></span>
  
- <span data-ttu-id="ab240-122">встроенных команд;</span><span class="sxs-lookup"><span data-stu-id="ab240-122">Built-in commands</span></span>
    
- <span data-ttu-id="ab240-123">команд XLL;</span><span class="sxs-lookup"><span data-stu-id="ab240-123">XLL commands</span></span>
    
- <span data-ttu-id="ab240-124">Функции интерфейса диспетчера надстроек XLL (**xlAutoOpen** функции и т. д.)</span><span class="sxs-lookup"><span data-stu-id="ab240-124">XLL Add-in Manager interface functions (**xlAutoOpen** function, and so on)</span></span> 
    
- <span data-ttu-id="ab240-125">пользовательских команд Microsoft Visual Basic для приложений (VBA), часто называемых макросами;</span><span class="sxs-lookup"><span data-stu-id="ab240-125">Microsoft Visual Basic for Applications (VBA) user-defined commands (often referred to as macros)</span></span>
    
- <span data-ttu-id="ab240-126">пользовательских функций VBA;</span><span class="sxs-lookup"><span data-stu-id="ab240-126">VBA user-defined functions</span></span>
    
- <span data-ttu-id="ab240-127">встроенных потоконебезопасных функций листа (см. список в следующем разделе);</span><span class="sxs-lookup"><span data-stu-id="ab240-127">Built-in thread-unsafe worksheet functions (see the next section for a list)</span></span>
    
- <span data-ttu-id="ab240-128">пользовательских команд и функций листа макросов XLM;</span><span class="sxs-lookup"><span data-stu-id="ab240-128">XLM macro sheet user-defined commands and functions</span></span>
    
- <span data-ttu-id="ab240-129">функций и команд надстроек COM;</span><span class="sxs-lookup"><span data-stu-id="ab240-129">COM add-in commands and functions</span></span>
    
- <span data-ttu-id="ab240-130">функций и операторов в выражениях условного форматирования;</span><span class="sxs-lookup"><span data-stu-id="ab240-130">Functions and operators within conditional formatting expressions</span></span>
    
- <span data-ttu-id="ab240-131">функций и операторов в определениях имен, используемых в формулах листа;</span><span class="sxs-lookup"><span data-stu-id="ab240-131">Functions and operators within defined name definitions used in worksheet formulas</span></span>
    
- <span data-ttu-id="ab240-132">Принудительное вычисление выражения в поле изменить формулу, с помощью клавиши **F9**</span><span class="sxs-lookup"><span data-stu-id="ab240-132">The forced evaluation of an expression in the formula-edit box using the **F9** key</span></span> 
    
<span data-ttu-id="ab240-p105">Вычисления по всем формулам листа, независимо от того, потокобезопасны функции или нет, выполняются в основном потоке, если не настроено использование нескольких потоков в Excel. Когда пользователь указывает, что следует использовать несколько потоков, дополнительные потоки используются для потокобезопасных ячеек. Обратите внимание, что основной поток также может использоваться для потокобезопасных ячеек, когда это целесообразно для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ab240-p105">All worksheet formulas, regardless of whether the functions are thread safe or not, are evaluated on the main thread unless Excel is configured to use more than one thread. When the user specifies that more than one thread should be used, the additional threads are used for thread-safe cells. Note that the main thread may still be used for thread-safe cells when it makes sense from a load-balancing point of view.</span></span>
  
<span data-ttu-id="ab240-136">Стоит отметить, что Excel не выполняет более одной команды за раз, поэтому необязательно применять те же меры предосторожности, что и при написании потокобезопасных функций, например использовать локальную память потока и критические секции.</span><span class="sxs-lookup"><span data-stu-id="ab240-136">It is worth restating that Excel does not run more than one command at once, so you do not need to employ the same precautions as when you are writing thread-safe functions, such as the use of thread-local memory and critical sections.</span></span>
  
## <a name="what-is-and-is-not-considered-thread-safe-by-excel"></a><span data-ttu-id="ab240-137">Какой используется и не является поток безопасных с Excel</span><span class="sxs-lookup"><span data-stu-id="ab240-137">What is and is not considered thread safe by Excel</span></span>
<span data-ttu-id="ab240-138"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="ab240-138"></span></span>

<span data-ttu-id="ab240-139">Потокобезопасными считаются только следующие элементы в Excel:</span><span class="sxs-lookup"><span data-stu-id="ab240-139">Excel only considers the following as thread safe:</span></span>
  
- <span data-ttu-id="ab240-140">все унарные и бинарные операторы в Excel;</span><span class="sxs-lookup"><span data-stu-id="ab240-140">All unary and binary operators in Excel.</span></span>
    
- <span data-ttu-id="ab240-141">Практически во всех встроенных функций, начиная с версии Excel 2007 (см. список исключений)</span><span class="sxs-lookup"><span data-stu-id="ab240-141">Almost all built-in worksheet functions starting in Excel 2007 (see exceptions list)</span></span>
    
- <span data-ttu-id="ab240-142">функции надстроек XLL, явно зарегистрированные как потокобезопасные.</span><span class="sxs-lookup"><span data-stu-id="ab240-142">XLL add-in functions that have been explicitly registered as thread-safe.</span></span>
    
<span data-ttu-id="ab240-143">Потоконебезопасные встроенные функции листа:</span><span class="sxs-lookup"><span data-stu-id="ab240-143">The built-in worksheet functions that are not thread safe are:</span></span>
  
- <span data-ttu-id="ab240-144">**ФОНЕТИЧЕСКОЕ**</span><span class="sxs-lookup"><span data-stu-id="ab240-144">**PHONETIC**</span></span>
    
- <span data-ttu-id="ab240-145">**ЯЧЕЙКИ** , когда используется аргумент «адрес» или «формат»</span><span class="sxs-lookup"><span data-stu-id="ab240-145">**CELL** when either the "format" or "address" argument is used</span></span> 
    
- <span data-ttu-id="ab240-146">**INDIRECT**</span><span class="sxs-lookup"><span data-stu-id="ab240-146">**INDIRECT**</span></span>
    
- <span data-ttu-id="ab240-147">**ПОЛУЧИТЬ.ДАННЫЕ.СВОДНОЙ.ТАБЛИЦЫ**</span><span class="sxs-lookup"><span data-stu-id="ab240-147">**GETPIVOTDATA**</span></span>
    
- <span data-ttu-id="ab240-148">**КУБЭЛЕМЕНТ**</span><span class="sxs-lookup"><span data-stu-id="ab240-148">**CUBEMEMBER**</span></span>
    
- <span data-ttu-id="ab240-149">**КУБЗНАЧЕНИЕ**</span><span class="sxs-lookup"><span data-stu-id="ab240-149">**CUBEVALUE**</span></span>
    
- <span data-ttu-id="ab240-150">**КУБСВОЙСТВОЭЛЕМЕНТА**</span><span class="sxs-lookup"><span data-stu-id="ab240-150">**CUBEMEMBERPROPERTY**</span></span>
    
- <span data-ttu-id="ab240-151">**КУБМНОЖ**</span><span class="sxs-lookup"><span data-stu-id="ab240-151">**CUBESET**</span></span>
    
- <span data-ttu-id="ab240-152">**КУБПОРЭЛЕМЕНТ**</span><span class="sxs-lookup"><span data-stu-id="ab240-152">**CUBERANKEDMEMBER**</span></span>
    
- <span data-ttu-id="ab240-153">**КУБЭЛЕМЕНТКИП**</span><span class="sxs-lookup"><span data-stu-id="ab240-153">**CUBEKPIMEMBER**</span></span>
    
- <span data-ttu-id="ab240-154">**КУБЧИСЛОЭЛМНОЖ**</span><span class="sxs-lookup"><span data-stu-id="ab240-154">**CUBESETCOUNT**</span></span>
    
- <span data-ttu-id="ab240-155">**Адрес** , где он получает параметр пятый (sheet_name)</span><span class="sxs-lookup"><span data-stu-id="ab240-155">**ADDRESS** where the fifth parameter (the sheet_name) is given</span></span> 
    
- <span data-ttu-id="ab240-156">Базы данных все функции (**DSUM**, **DAVERAGE**и т. д.), который относится к сводной таблицы</span><span class="sxs-lookup"><span data-stu-id="ab240-156">Any database function (**DSUM**, **DAVERAGE**, and so on) that refers to a pivot table</span></span>
    
- <span data-ttu-id="ab240-157">**ОШИБКА. ТИП**</span><span class="sxs-lookup"><span data-stu-id="ab240-157">**ERROR.TYPE**</span></span>
    
- <span data-ttu-id="ab240-158">**ГИПЕРССЫЛКИ**</span><span class="sxs-lookup"><span data-stu-id="ab240-158">**HYPERLINK**</span></span>
    
<span data-ttu-id="ab240-159">Следующие элементы считаются небезопасными:</span><span class="sxs-lookup"><span data-stu-id="ab240-159">To be explicit, the following are considered to be unsafe:</span></span>
  
- <span data-ttu-id="ab240-160">пользовательские функции VBA;</span><span class="sxs-lookup"><span data-stu-id="ab240-160">VBA user-defined functions</span></span>
    
- <span data-ttu-id="ab240-161">пользовательские функции надстроек COM;</span><span class="sxs-lookup"><span data-stu-id="ab240-161">COM add-in user-defined functions</span></span>
    
- <span data-ttu-id="ab240-162">пользовательские функции листа макросов XLM;</span><span class="sxs-lookup"><span data-stu-id="ab240-162">XLM macro-sheet user-defined functions</span></span>
    
- <span data-ttu-id="ab240-163">функции надстроек XLL, не зарегистрированные как потокобезопасные.</span><span class="sxs-lookup"><span data-stu-id="ab240-163">XLL add-in functions not explicitly registered as thread safe</span></span>
    
<span data-ttu-id="ab240-164">Вывод: следующие операции и функции потоконебезопасны и дают сбой при вызове из функции XLL, зарегистрированной как потокобезопасная:</span><span class="sxs-lookup"><span data-stu-id="ab240-164">The implications are that the following operations and functions are not thread-safe, and fail if they are called from an XLL function registered as thread safe:</span></span>
  
- <span data-ttu-id="ab240-165">Вызовы функций XLM информации, например, **xlfGetCell** (**GET. Ячейка**).</span><span class="sxs-lookup"><span data-stu-id="ab240-165">Calls to XLM information functions, for example, **xlfGetCell** (**GET.CELL**).</span></span>
    
- <span data-ttu-id="ab240-166">Вызывает **xlfSetName** (**SET.NAME**) для определения или удалить внутренние имена XLL.</span><span class="sxs-lookup"><span data-stu-id="ab240-166">Calls to **xlfSetName** (**SET.NAME**) to define or delete XLL-internal names.</span></span>
    
- <span data-ttu-id="ab240-167">Вызовы для потока небезопасных пользовательских функций, с помощью **xlUDF**.</span><span class="sxs-lookup"><span data-stu-id="ab240-167">Calls to thread-unsafe user-defined functions using **xlUDF**.</span></span>
    
- <span data-ttu-id="ab240-168">Вызывает функцию [xlfEvaluate](xlfevaluate.md) выражения, которые содержат потока небезопасные функции или, которые содержат определенные имена, определения содержат потока небезопасные функции.</span><span class="sxs-lookup"><span data-stu-id="ab240-168">Calls to the [xlfEvaluate](xlfevaluate.md) function for expressions that contain thread-unsafe functions or that contain defined names whose definitions contain thread-unsafe functions.</span></span> 
    
- <span data-ttu-id="ab240-169">Вызовы функции [xlAbort](xlabort.md) снимите условия останова.</span><span class="sxs-lookup"><span data-stu-id="ab240-169">Calls to the [xlAbort](xlabort.md) function to clear a break condition.</span></span> 
    
- <span data-ttu-id="ab240-170">Вызовы функции [xlCoerce](xlcoerce.md) для получения значения ссылки на не вычисленной ячейки.</span><span class="sxs-lookup"><span data-stu-id="ab240-170">Calls to the [xlCoerce](xlcoerce.md) function to get the value of an uncalculated cell reference.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="ab240-171">Функции листа XLL не разрешены для вызова команд интерфейса API для C, например, **xlcSave**, независимо от того, является ли они зарегистрированных как потокобезопасными или нет.</span><span class="sxs-lookup"><span data-stu-id="ab240-171">XLL worksheet functions are not permitted to call C API commands, for example, **xlcSave**, regardless of whether they have been registered as thread safe or not.</span></span> 
  
<span data-ttu-id="ab240-172">Учитывая, что функции XLL, объявленные как потокобезопасными не может вызывать информационные функции XML или ссылки на ячейки невычисляемая, Excel не разрешает функции XLL, зарегистрированные в качестве эквивалентами листа макросов также быть зарегистрирована как потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="ab240-172">Given that XLL functions declared as thread safe cannot call XLM information functions or reference uncalculated cells, Excel does not permit XLL functions that are registered as macro sheet equivalents to also be registered as thread safe.</span></span> <span data-ttu-id="ab240-173">Поэтому попытки подключения для получения значения с помощью **xlCoerce** ссылки не вычисленной ячейки не удается выполнить с ошибкой **xlretUncalced** .</span><span class="sxs-lookup"><span data-stu-id="ab240-173">Therefore attempting to get the value of an uncalculated cell reference using **xlCoerce** fails with an **xlretUncalced** error.</span></span> <span data-ttu-id="ab240-174">Вызов XLM сведения о функции не удается выполнить с ошибкой **xlretFailed** .</span><span class="sxs-lookup"><span data-stu-id="ab240-174">Calling an XLM information function fails with an **xlretFailed** error.</span></span> <span data-ttu-id="ab240-175">Другие точки из списка ранее ошибкой с кодом ошибки, представлено в Excel C API: **xlretNotThreadSafe**.</span><span class="sxs-lookup"><span data-stu-id="ab240-175">The other points listed previously fail with an error code introduced in the Excel C API: **xlretNotThreadSafe**.</span></span> 
  
<span data-ttu-id="ab240-176">Все функции обратного вызова C API потокобезопасны:</span><span class="sxs-lookup"><span data-stu-id="ab240-176">The C API-only call-back functions are all thread safe:</span></span>
  
- <span data-ttu-id="ab240-177">**xlCoerce** (за исключением хотя приведения не вычисленной ячейки ссылается на возникает ошибка)</span><span class="sxs-lookup"><span data-stu-id="ab240-177">**xlCoerce** (except although coercion of uncalculated cell references fails)</span></span> 
    
- <span data-ttu-id="ab240-178">**xlFree**</span><span class="sxs-lookup"><span data-stu-id="ab240-178">**xlFree**</span></span>
    
- <span data-ttu-id="ab240-179">**xlStack**</span><span class="sxs-lookup"><span data-stu-id="ab240-179">**xlStack**</span></span>
    
- <span data-ttu-id="ab240-180">**xlSheetId**</span><span class="sxs-lookup"><span data-stu-id="ab240-180">**xlSheetId**</span></span>
    
- <span data-ttu-id="ab240-181">**xlSheetNm**</span><span class="sxs-lookup"><span data-stu-id="ab240-181">**xlSheetNm**</span></span>
    
- <span data-ttu-id="ab240-182">**xlAbort** (за исключением при использовании снимите условие прерывания)</span><span class="sxs-lookup"><span data-stu-id="ab240-182">**xlAbort** (except when used to clear a break condition)</span></span> 
    
- <span data-ttu-id="ab240-183">**xlGetInst**</span><span class="sxs-lookup"><span data-stu-id="ab240-183">**xlGetInst**</span></span>
    
- <span data-ttu-id="ab240-184">**xlGetHwnd**</span><span class="sxs-lookup"><span data-stu-id="ab240-184">**xlGetHwnd**</span></span>
    
- <span data-ttu-id="ab240-185">**xlGetBinaryName**</span><span class="sxs-lookup"><span data-stu-id="ab240-185">**xlGetBinaryName**</span></span>
    
- <span data-ttu-id="ab240-186">**xlDefineBinaryName**</span><span class="sxs-lookup"><span data-stu-id="ab240-186">**xlDefineBinaryName**</span></span>
    
<span data-ttu-id="ab240-187">Одно исключение — это функция **функция xlSet** , то есть, в любом случае эквивалент команды и поэтому не могут быть вызваны любой функции рабочего листа.</span><span class="sxs-lookup"><span data-stu-id="ab240-187">The one exception is the **xlSet** function, which is, in any case, a command-equivalent and so cannot be called from any worksheet function.</span></span> 
  
<span data-ttu-id="ab240-p107">Функцию листа XLL можно зарегистрировать в Excel как потокобезопасную. В этом случае Excel будет знать, что вызов функции безопасен и возможен одновременно в нескольких потоках. Но необходимо убедиться, что это действительно так. Работа Excel может быть нарушена, если функция, зарегистрированная как потокобезопасная, окажется небезопасной.</span><span class="sxs-lookup"><span data-stu-id="ab240-p107">An XLL worksheet function can be registered with Excel as thread safe. This tells Excel that the function can be called safely and simultaneously on multiple threads, although you must make sure this is really the case. You can possibly destabilize Excel if a function registered as thread safe then behaves unsafely.</span></span>
  
## <a name="registering-xll-functions-as-thread-safe"></a><span data-ttu-id="ab240-191">Регистрация функции XLL в качестве потокобезопасными</span><span class="sxs-lookup"><span data-stu-id="ab240-191">Registering XLL functions as thread safe</span></span>
<span data-ttu-id="ab240-192"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="ab240-192"></span></span>

<span data-ttu-id="ab240-193">Правила, которым должен следовать разработчик при написании потокобезопасных функций:</span><span class="sxs-lookup"><span data-stu-id="ab240-193">The rules that a developer must obey when writing thread-safe functions are as follows:</span></span>
  
- <span data-ttu-id="ab240-194">Не вызывайте ресурсы в других библиотеках DLL, которые могут быть потоконебезопасными.</span><span class="sxs-lookup"><span data-stu-id="ab240-194">Do not call resources in other DLLs that may not be thread safe.</span></span>
    
- <span data-ttu-id="ab240-195">Не осуществляйте потоконебезопасные вызовы с помощью C API или COM.</span><span class="sxs-lookup"><span data-stu-id="ab240-195">Do not make any thread-unsafe calls via the C API or COM.</span></span>
    
- <span data-ttu-id="ab240-196">Защищайте ресурсы, которые могут использоваться одновременно несколькими потоками, с помощью критических секций.</span><span class="sxs-lookup"><span data-stu-id="ab240-196">Protect resources that could be used simultaneously by more than one thread using critical sections.</span></span>
    
- <span data-ttu-id="ab240-197">Используйте локальную память потока для хранения данных потока и заменяйте статические переменные в функциях локальными переменными потока.</span><span class="sxs-lookup"><span data-stu-id="ab240-197">Use thread-local memory for thread-specific storage, and replace static variables within functions with thread-local variables.</span></span>
    
<span data-ttu-id="ab240-198">В Excel действует дополнительное ограничение: потокобезопасные функции невозможно зарегистрировать как эквивалентные функциям листа макросов, поэтому они не могут вызывать информационные функции XLM и получать значения непересчитанных ячеек.</span><span class="sxs-lookup"><span data-stu-id="ab240-198">Excel imposes an additional restriction: thread-safe functions cannot be registered as macro-sheet equivalents, and therefore cannot call XLM information functions or get the values of un-recalculated cells.</span></span>
  
## <a name="memory-contention"></a><span data-ttu-id="ab240-199">Конфликты памяти</span><span class="sxs-lookup"><span data-stu-id="ab240-199">Memory contention</span></span>
<span data-ttu-id="ab240-200"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="ab240-200"></span></span>

<span data-ttu-id="ab240-201">При создании многопотоковых систем необходимо решить две фундаментальные проблемы:</span><span class="sxs-lookup"><span data-stu-id="ab240-201">Multithreaded systems must address two fundamental issues:</span></span>
  
- <span data-ttu-id="ab240-202">Как защитить память, чтение или запись данных которой должны выполнять несколько потоков.</span><span class="sxs-lookup"><span data-stu-id="ab240-202">How to protect memory that must be read from, or written to, by more than one thread.</span></span>
    
- <span data-ttu-id="ab240-203">Как создать память, связанную с выполняемым потоком, и получить к ней доступ.</span><span class="sxs-lookup"><span data-stu-id="ab240-203">How to create and access memory that is associated with, and so private to, the executing thread.</span></span>
    
<span data-ttu-id="ab240-204">Операционная система Windows и Windows Software Development Kit (SDK) предоставляют средства для обоих приведенных: критические разделы и API хранилища локального потока (TLS) соответственно.</span><span class="sxs-lookup"><span data-stu-id="ab240-204">The Windows operating system and Windows Software Development Kit (SDK) provide tools for both of these: critical sections and the thread-local storage (TLS) API respectively.</span></span> <span data-ttu-id="ab240-205">Дополнительные сведения содержатся в разделе [Управление памятью в Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="ab240-205">For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="ab240-p109">Первая проблема может возникнуть, например, когда двум функциям листа (или двум параллельно выполняемым экземплярам одной функции) нужен доступ к глобальной переменной в проекте DLL (например, для ее изменения). Помните, что эта переменная может быть скрыта в глобально доступном экземпляре объекта класса.</span><span class="sxs-lookup"><span data-stu-id="ab240-p109">The first issue can arise, for example, when two worksheet functions (or two simultaneously running instances of the same function) need to access or modify a global variable in a DLL project. Remember that such a global variable might be hidden in a globally accessible instance of a class object.</span></span>
  
<span data-ttu-id="ab240-p110">Вторая проблема может возникнуть, например, когда функция листа объявляет статическую переменную или объект в коде функции. Компилятор C/C++ создает только одну копию, которую используют все потоки. Это означает, что один экземпляр функции может изменить значение, а другой (в другом потоке) может использовать ранее заданное значение.</span><span class="sxs-lookup"><span data-stu-id="ab240-p110">The second issue can arise, for example, when a worksheet function declares a static variable or object within the function body code. The C/C++ compiler only creates a single copy that all threads use. This means one instance of the function could change the value, while another on a different thread might be assuming the value is what it previously set.</span></span>
  
## <a name="example-applications-of-mtr"></a><span data-ttu-id="ab240-211">Примеры приложений MTR</span><span class="sxs-lookup"><span data-stu-id="ab240-211">Example applications of MTR</span></span>
<span data-ttu-id="ab240-212"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="ab240-212"></span></span>

<span data-ttu-id="ab240-p111">Любой XLL-модуль, который экспортирует функции листа, может использовать многопотоковый пересчет (MTR) в Excel, если эти функции не должны выполнять потоконебезопасные действия. Это позволяет Excel максимально быстро выполнять пересчет в книгах, в которых они используются, и поэтому MTR рекомендуется применять всегда.</span><span class="sxs-lookup"><span data-stu-id="ab240-p111">Any XLL that exports worksheet functions can take advantage of multithreaded recalculation (MTR) in Excel provided that those functions do not need to perform thread-unsafe actions. This enables Excel to recalculate workbooks that depend on them as quickly as possible and is therefore desirable whatever the application.</span></span>
  
<span data-ttu-id="ab240-215">В частности MTR имеет огромное влияние на время пересчета книги, которые могут вызывать пользовательские функции (UDF), сами вызова внешних процессы, используемые для получения нужного результата.</span><span class="sxs-lookup"><span data-stu-id="ab240-215">Specifically, MTR has an enormous impact on the recalculation time of workbooks that call user-defined functions (UDFs) that themselves call external processes to obtain the desired result.</span></span> <span data-ttu-id="ab240-216">В частности необходимо учитывайте UDF, который вызывает удаленного сервера, на котором можно одновременно обработать большое количество запросов и книги, содержащий много вызовов этой функции.</span><span class="sxs-lookup"><span data-stu-id="ab240-216">In particular, consider a UDF that calls a remote server that can process many requests simultaneously and a workbook containing many calls to that function.</span></span> <span data-ttu-id="ab240-217">Если пересчета книги в одном потоке, каждый вызов пользовательских Функций и поэтому к удаленному серверу, необходимо выполнить перед выполнением следующего.</span><span class="sxs-lookup"><span data-stu-id="ab240-217">If recalculation of the workbook is single-threaded, each call to the UDF, and so to the remote server, must complete before the next one can be made.</span></span> <span data-ttu-id="ab240-218">Выполняется это пустая способность сервера обрабатывать вызовы много раз.</span><span class="sxs-lookup"><span data-stu-id="ab240-218">This wastes the server's ability to process many calls at once.</span></span> <span data-ttu-id="ab240-219">Если многопоточные пересчета книги Excel можно сделать несколько вызовов в то же время или быстро.</span><span class="sxs-lookup"><span data-stu-id="ab240-219">If recalculation of the workbook is multithreaded, Excel can make multiple calls at the same time or in rapid succession.</span></span>
  
<span data-ttu-id="ab240-p113">Если в Excel и на сервере настроено использование одинакового количества потоков (N), при этом топология дерева зависимостей книги позволяет это, общее время пересчета можно сократить до значения, которое стремится к 1/N. Это возможно, даже если у клиентского компьютера (на котором обрабатывается книга) всего один процессор, особенно если время вызова сервера невелико по сравнению с временем обработки вызова сервером.</span><span class="sxs-lookup"><span data-stu-id="ab240-p113">If Excel is configured to use the same number of threads as the server—call it N—and the topology of the dependency tree of the workbook permits it, the total recalculation time could be reduced to something approaching 1/N of the single-threaded calculation time. This may be true even where the client computer (on which the workbook is running) only has one processor, especially where the time taken to make the call to the server is small relative to the time it takes the server to process the call.</span></span> 
  
<span data-ttu-id="ab240-p114">С каждым дополнительным потоком связаны затраты ресурсов операционной системы. Поэтому оптимальное количество потоков, которое должно использовать приложение Excel, для каждой книги, сервера и клиентского компьютера определяется опытным путем.</span><span class="sxs-lookup"><span data-stu-id="ab240-p114">There is operating system overhead for each additional thread. Therefore some experimentation might be required for a given workbook and a given server and client computer to find the optimum number of threads Excel should be told to use.</span></span> 
  
<span data-ttu-id="ab240-p115">Рассмотрим компьютер с одним процессором, на котором запущено приложение Excel и обрабатывается книга, содержащая 1000 ячеек. Она вызывает функцию UDF, которая, в свою очередь, вызывает один или несколько удаленных серверов. Предположим, что 1000 ячеек не зависят друг от друга, поэтому Excel не нужно ожидать завершения одного вызова для совершения другого. (Это условие можно нарушить без последствий для этого примера.) Если серверы могут обрабатывать 100 запросов одновременно, а в Excel настроено использование 100 потоков, время выполнения можно сократить до 1/100 (сотой части от времени выполнения однопотокового пересчета). Чтобы приложение Excel могло распределять вызовы между потоками, а операционная система могла управлять 100 потоками, требуются значительные ресурсы. Это показывает, что на практике такого значительного сокращения времени не будет. Мы также предполагаем, что сервер характеризуется хорошей масштабируемостью, и что одновременная обработка 100 задач сильно не повлияет на время выполнения отдельных задач.</span><span class="sxs-lookup"><span data-stu-id="ab240-p115">For example, consider a single-processor computer that is running Excel and a workbook that contains 1,000 cells. It calls a UDF, which in turn calls one or more remote servers. Assume that the 1,000 cells do not depend upon each other, so that Excel does not have to wait for one call to complete before calling the next. (Some relaxation of this constraint is possible without affecting this example.) If the servers can process 100 requests simultaneously, and Excel is configured to use 100 threads, the execution time can be reduced to as little as 1/100th of that where only one thread is used. The overhead that is associated with Excel allocating calls to each thread and the operating system managing 100 threads means that, in practice, the reduction will not be quite this great. There is also an implicit assumption here that the server scales well, and asking it to process 100 tasks concurrently will not affect individual task completion times significantly.</span></span>
  
<span data-ttu-id="ab240-230">Пример практического применения, при котором этот способ дает отличные результаты, — использование методов Монте-Карло, а также выполнение других ресурсоемких задач, которые можно разделить на более мелкие подзадачи и обработать на серверах.</span><span class="sxs-lookup"><span data-stu-id="ab240-230">One practical application in which this technique can have an important benefit is that of Monte-Carlo methods, as well as other numerically intensive tasks that can be split into smaller sub-tasks that can be farmed out to servers.</span></span>
  
## <a name="excel-services-considerations"></a><span data-ttu-id="ab240-231">Общие сведения о службах Excel</span><span class="sxs-lookup"><span data-stu-id="ab240-231">Excel Services considerations</span></span>
<span data-ttu-id="ab240-232"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="ab240-232"></span></span>

<span data-ttu-id="ab240-p116">Службы Excel поддерживают загрузку, вычисление и обработку электронных таблиц Excel на сервере. Пользователи могут получить доступ к электронным таблицам и работать с ними, используя стандартные средства браузера.</span><span class="sxs-lookup"><span data-stu-id="ab240-p116">Excel Services supports the loading, calculating, and rendering of Excel spreadsheets on a server. Users can then access and interact with the spreadsheets by using standard browser tools.</span></span>
  
<span data-ttu-id="ab240-p117">Пользовательские функции служб Excel созданы с использованием управляемого кода Microsoft .NET Framework и доступны благодаря сборке .NET. XLL-модули не поддерживаются в службах Excel. Ресурс UDF сервера управляемого кода может вызывать XLL-модуль для доступа к его функциональности, что обеспечивает одинаковую функциональность при работе с книгами, загруженными на сервер и локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="ab240-p117">Excel Services UDFs are created using Microsoft .NET Framework managed code and made available though a .NET assembly. XLLs are not supported by Excel Services. A managed code server UDF resource can call into an XLL to access its functionality, so that the user can have the same functionality with a server-loaded workbook as with a client-loaded workbook.</span></span>
  
<span data-ttu-id="ab240-238">Чтобы функции XLL таким образом, они должны таким образом быть заключены в сборке .NET, который преобразует аргументы и возвращаемые значения из собственных типов для типов данных платформы .NET Framework управляемых и, который вызывает функции XLL.</span><span class="sxs-lookup"><span data-stu-id="ab240-238">To make an XLL's functions available in this way, they must therefore be wrapped in a .NET assembly that converts arguments and return values from the native data types to the .NET Framework managed data types, and that calls the XLL functions.</span></span> <span data-ttu-id="ab240-239">Оболочкой .NET может экспортировать один сервер пользовательских Функций для каждой функции XLL, к которому обращается.</span><span class="sxs-lookup"><span data-stu-id="ab240-239">The .NET wrapper would export one server UDF for each XLL function being accessed.</span></span> <span data-ttu-id="ab240-240">Дополнительные требования заключается в том, что все функции XLL вызове таким образом должен быть потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="ab240-240">An additional requirement is that any XLL functions called in this way must be thread safe.</span></span> <span data-ttu-id="ab240-241">Так как функции XLL не зарегистрировано в то, как они являются с клиента Excel, на сервере и оболочкой .NET у нет возможности применение, что они являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="ab240-241">Because the XLL functions are not registered in the way that they are with client Excel, the server and the .NET wrapper have no way of enforcing that they are thread safe.</span></span> <span data-ttu-id="ab240-242">Это ответственность разработчика XLL убедиться в этом.</span><span class="sxs-lookup"><span data-stu-id="ab240-242">It is the responsibility of the XLL developer to ensure this.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ab240-243">См. также</span><span class="sxs-lookup"><span data-stu-id="ab240-243">See also</span></span>

- [<span data-ttu-id="ab240-244">Пересчет в Excel</span><span class="sxs-lookup"><span data-stu-id="ab240-244">Excel Recalculation</span></span>](excel-recalculation.md)  
- [<span data-ttu-id="ab240-245">���������� ������� � Excel</span><span class="sxs-lookup"><span data-stu-id="ab240-245">Memory Management in Excel</span></span>](memory-management-in-excel.md) 
- [<span data-ttu-id="ab240-246">Доступ к XLL-коду в Excel</span><span class="sxs-lookup"><span data-stu-id="ab240-246">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)  
- [<span data-ttu-id="ab240-247">�������� ���������������� � Excel</span><span class="sxs-lookup"><span data-stu-id="ab240-247">Excel Programming Concepts</span></span>](excel-programming-concepts.md)  
- [<span data-ttu-id="ab240-248">���������� �� ������� Excel 2013 XLL SDK API</span><span class="sxs-lookup"><span data-stu-id="ab240-248">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

