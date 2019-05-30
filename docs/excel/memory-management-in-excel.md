---
title: Управление памятью в Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- память xloper12 [excel 2007],управление памятью в Excel,стек Excel,строки [Excel 2007], управление памятью,управление памятью в Excel,память XLOPER [Excel 2007],память [Excel 2007], рекомендации по управлению
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f129dac2971f01c8ada15f0028958132b1945746
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419543"
---
# <a name="memory-management-in-excel"></a><span data-ttu-id="19512-104">Управление памятью в Excel</span><span class="sxs-lookup"><span data-stu-id="19512-104">Memory Management in Excel</span></span>

 <span data-ttu-id="19512-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="19512-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="19512-p101">Если вы хотите создавать эффективные и стабильные XLL-надстройки, особого внимания требует управление памятью. Неправильное управление памятью может привести к целому ряду проблем в Microsoft Excel — от незначительных, таких как небольшие утечки памяти или ее неэффективное распределение и инициализация, до серьезных, таких как дестабилизация Excel.</span><span class="sxs-lookup"><span data-stu-id="19512-p101">Memory management is the most important concern if you want to create efficient and stable XLLs. Failure to manage memory well can lead to a range of problems in Microsoft Excel—from minor problems such as inefficient memory allocation and initialization and small memory leaks, to major problems such as the destabilization of Excel.</span></span>
  
<span data-ttu-id="19512-p102">Неправильное управление памятью — наиболее распространенная причина серьезных проблем, связанных с надстройками. Следовательно, создавайте проект только при наличии хорошо продуманной и последовательной стратегии управления памятью.</span><span class="sxs-lookup"><span data-stu-id="19512-p102">Mismanagement of memory is the most common source of serious add-in-related problems. Therefore, you should build your project with a consistent and well-thought-through strategy on memory management.</span></span> 
  
<span data-ttu-id="19512-p103">С появлением многопоточного пересчета книг в Microsoft Office Excel 2007 управлять памятью стало сложнее. Если вы хотите создавать и экспортировать потокобезопасные функции листов, необходимо разрешать конфликты, которые могут возникать, если несколько потоков конкурируют за доступ.</span><span class="sxs-lookup"><span data-stu-id="19512-p103">Memory management became more complex in Microsoft Office Excel 2007 with the introduction of multithreaded workbook recalculation. If you want to create and export thread-safe worksheet functions, you must manage the resulting conflicts that can occur when multiple threads compete for access.</span></span>
  
<span data-ttu-id="19512-112">Ниже приведены рекомендации для следующих трех типов структуры данных:</span><span class="sxs-lookup"><span data-stu-id="19512-112">There are memory considerations for the following three data structure types:</span></span>
  
- <span data-ttu-id="19512-113">**XLOPER** и **XLOPER12**;</span><span class="sxs-lookup"><span data-stu-id="19512-113">**XLOPER**s and **XLOPER12**s</span></span>
    
- <span data-ttu-id="19512-114">строки, не входящие в состав **XLOPER** или **XLOPER12**;</span><span class="sxs-lookup"><span data-stu-id="19512-114">Strings that are not in an **XLOPER** or **XLOPER12**</span></span>
    
- <span data-ttu-id="19512-115">массивы **FP** и **FP12**.</span><span class="sxs-lookup"><span data-stu-id="19512-115">**FP** and **FP12** arrays</span></span> 
    
## <a name="xloperxloper12-memory"></a><span data-ttu-id="19512-116">Память XLOPER и XLOPER12</span><span class="sxs-lookup"><span data-stu-id="19512-116">XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="19512-117">Структура данных **XLOPER**/ **XLOPER12** включает несколько подтипов, содержащих указатели на блоки памяти, в частности строки (**xltypeStr**), массивы (**xltypeMulti**) и внешние ссылки (**xltypeRef**).</span><span class="sxs-lookup"><span data-stu-id="19512-117">The XLOPER/XLOPER12 data structure has a few sub-types that contain pointers to blocks of memory, namely strings (xltypeStr), arrays (xltypeMulti) and external references (xltypeRef).</span></span> <span data-ttu-id="19512-118">Кроме того, обратите внимание, что массивы **xltypeMulti** могут содержать строку **XLOPER**/ **XLOPER12**, которая указывает на другие блоки памяти.</span><span class="sxs-lookup"><span data-stu-id="19512-118">Note also that **xltypeMulti** arrays can contain string **XLOPER**/ **XLOPER12s** that in turn point to other blocks of memory.</span></span> 
  
<span data-ttu-id="19512-119">Структуру **XLOPER**/ **XLOPER12** можно создать несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="19512-119">An **XLOPER**/ **XLOPER12** can be created in several ways:</span></span> 
  
- <span data-ttu-id="19512-120">в Excel при подготовке аргументов для передачи в функцию XLL;</span><span class="sxs-lookup"><span data-stu-id="19512-120">By Excel when preparing arguments to be passed to an XLL function</span></span>
    
- <span data-ttu-id="19512-121">в Excel при возвращении **XLOPER** или **XLOPER12** во время вызова API C;</span><span class="sxs-lookup"><span data-stu-id="19512-121">By Excel when returning an **XLOPER** or **XLOPER12** in a C API call</span></span> 
    
- <span data-ttu-id="19512-122">в DLL при создании аргументов для передачи во время вызова API C;</span><span class="sxs-lookup"><span data-stu-id="19512-122">By your DLL when creating arguments to be passed to a C API call</span></span>
    
- <span data-ttu-id="19512-123">в DLL при создании возвращаемого значения функции XLL.</span><span class="sxs-lookup"><span data-stu-id="19512-123">By your DLL when creating an XLL function return value</span></span>
    
<span data-ttu-id="19512-124">Блок памяти, принадлежащий к типу указателей на память, можно выделить под что-то несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="19512-124">A block of memory within one of the memory-pointing types can be allocated in several ways:</span></span>
  
- <span data-ttu-id="19512-125">как статический блок в библиотеке DLL за пределами кода функции (в этом случае необязательно выделять или освобождать память);</span><span class="sxs-lookup"><span data-stu-id="19512-125">It can be a static block within your DLL outside any function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="19512-126">как статический блок в библиотеке DLL, входящий в код функции (в этом случае необязательно выделять или освобождать память);</span><span class="sxs-lookup"><span data-stu-id="19512-126">It can be a static block within your DLL within some function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="19512-127">с помощью динамического выделения и освобождения в библиотеке DLL (**malloc** и **free**, **new** и **delete** и т. д.);</span><span class="sxs-lookup"><span data-stu-id="19512-127">It can be dynamically allocated and freed by your DLL in several possible ways: **malloc** and **free**, **new** and **delete**, and so on.</span></span>
    
- <span data-ttu-id="19512-128">с помощью динамического выделения в Excel.</span><span class="sxs-lookup"><span data-stu-id="19512-128">It can be dynamically allocated by Excel.</span></span>
    
<span data-ttu-id="19512-p105">Учитывая число возможных источников памяти **XLOPER**/ **XLOPER12** и количество ситуаций, в которых для структур данных **XLOPER**/ **XLOPER12** выделяется эта память, неудивительно, что эта тема может быть очень сложной. Тем не менее, если следовать нескольким правилам и рекомендациям, ее можно значительно упростить.</span><span class="sxs-lookup"><span data-stu-id="19512-p105">Given the number of possible origins for **XLOPER**/ **XLOPER12** memory and the number of situations in which the **XLOPER**/ **XLOPER12** might have had that memory assigned, it is not surprising that this subject can seem very difficult. However, the complexity can be greatly reduced if you follow several rules and guidelines.</span></span> 
  
### <a name="rules-for-working-with-xloperxloper12"></a><span data-ttu-id="19512-131">Правила работы с XLOPER/XLOPER12</span><span class="sxs-lookup"><span data-stu-id="19512-131">Rules for Working with XLOPER/XLOPER12</span></span>

- <span data-ttu-id="19512-p106">Не пытайтесь освободить память или перезаписать структуры данных **XLOPERs**/ **XLOPER12**, которые передаются как аргументы в функцию XLL. Эти аргументы предназначены только для чтения. Дополнительные сведения см. в разделе "Возвращение **XLOPER** или **XLOPER12** путем изменения аргументов на месте" статьи [Известные проблемы с разработкой XLL в Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="19512-p106">Do not try to free memory or overwrite **XLOPERs**/ **XLOPER12**s that are passed as arguments to your XLL function. You should treat such arguments as read-only. For more information, see "Returning **XLOPER** or **XLOPER12** by Modifying Arguments in Place" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
    
- <span data-ttu-id="19512-135">Если приложение Excel выделило память для структуры данных **XLOPER**/ **XLOPER12**, возвращаемой в DLL во время вызова API C:</span><span class="sxs-lookup"><span data-stu-id="19512-135">If Excel has allocated memory for an **XLOPER**/ **XLOPER12** returned to your DLL in a call to the C API:</span></span> 
    
  - <span data-ttu-id="19512-p107">Когда структура **XLOPER**/ **XLOPER12** больше не будет вам нужна, необходимо освободить память, вызвав функцию [xlFree](xlfree.md). Не используйте для этого другие методы, например free или delete.</span><span class="sxs-lookup"><span data-stu-id="19512-p107">You must free the memory when you no longer need the **XLOPER**/ **XLOPER12** using a call to [xlFree](xlfree.md). Do not use any other method, such as free or delete, to release the memory.</span></span>
    
  - <span data-ttu-id="19512-138">Если возвращается тип **xltypeMulti**, не перезаписывайте структуры данных **XLOPER**/ **XLOPER12** в массиве, особенно если они содержат строки или вы пробуете перезаписать их строкой.</span><span class="sxs-lookup"><span data-stu-id="19512-138">If the returned type is **xltypeMulti**, do not overwrite any **XLOPER**/ **XLOPER12**s within the array, especially if they contain strings, and especially not where you are trying to overwrite with a string.</span></span>
    
  - <span data-ttu-id="19512-139">Чтобы получить в Excel структуру **XLOPER**/ **XLOPER12** как возвращаемое значение функции DLL, необходимо сообщить приложению Excel о памяти, которую необходимо освободить после завершения работы.</span><span class="sxs-lookup"><span data-stu-id="19512-139">If you want to return the **XLOPER**/ **XLOPER12** to Excel as your DLL function's return value, you must tell Excel that there is memory that Excel must release when done.</span></span> 
    
- <span data-ttu-id="19512-140">Функцию **xlFree** необходимо вызывать только для структуры данных **XLOPER**/ **XLOPER12**, созданной в качестве возвращаемого значения при вызове API C.</span><span class="sxs-lookup"><span data-stu-id="19512-140">You must only call **xlFree** on an **XLOPER**/ **XLOPER12** that was created as the return value to a C API call.</span></span> 
    
- <span data-ttu-id="19512-141">Если библиотека DLL выделила память для структуры данных **XLOPER**/ **XLOPER12**, которую нужно получить в Excel в качестве возвращаемого значения функции DLL, необходимо сообщить приложению Excel, что библиотека DLL должна освободить память.</span><span class="sxs-lookup"><span data-stu-id="19512-141">If your DLL has allocated memory for an **XLOPER**/ **XLOPER12** that you want to return to Excel as your DLL function's return value, you must tell Excel that there is memory that the DLL must release.</span></span> 
    
### <a name="guidelines-for-memory-management"></a><span data-ttu-id="19512-142">Рекомендации по управлению памятью</span><span class="sxs-lookup"><span data-stu-id="19512-142">Guidelines for Memory Management</span></span>

- <span data-ttu-id="19512-p108">Используйте определенный метод для выделения и освобождения памяти в библиотеке DLL. Не смешивайте методы. Рекомендуем использовать нужный метод как структуру или класс памяти, где его можно изменять, не изменяя код в других местах.</span><span class="sxs-lookup"><span data-stu-id="19512-p108">Be consistent in your DLL in the method that you use to allocate and release memory. Avoid mixing methods. A good approach is to wrap the method that you are using up in a memory class or structure, within which you can change the method used without altering your code in many places.</span></span>
    
- <span data-ttu-id="19512-p109">При создании массивов **xltypeMulti** в библиотеке DLL выделяйте память для строк определенным способом: всегда выделяйте память динамически или всегда используйте статическую память. В этом случае, освобождая память, вы будете знать, что необходимо всегда освобождать строки или никогда этого не делать.</span><span class="sxs-lookup"><span data-stu-id="19512-p109">When you create **xltypeMulti** arrays within your DLL, be consistent in the way that you allocate memory for strings: always dynamically allocate the memory for them or always use static memory. If you do this, when you are freeing the memory, you will know that you must either always or never free the strings.</span></span> 
    
- <span data-ttu-id="19512-148">Создавайте глубокие копии выделенной приложением Excel памяти при копировании созданной с помощью Excel структуры данных **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="19512-148">Make deep copies of Excel-allocated memory when you are copying an Excel-created **XLOPER**/ **XLOPER12**.</span></span>
    
- <span data-ttu-id="19512-p110">Не помещайте выделенные приложением Excel строки **XLOPER**/ **XLOPER12** в массивы **xltypeMulti**. Создавайте глубокие копии строк и храните указатели на эти копии в массиве.</span><span class="sxs-lookup"><span data-stu-id="19512-p110">Do not put Excel-allocated string **XLOPER**/ **XLOPER12**s within **xltypeMulti** arrays. Make deep copies of the strings and store pointers to the copies in the array.</span></span> 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a><span data-ttu-id="19512-151">Освобождение выделенной приложением Excel памяти XLOPER/XLOPER12</span><span class="sxs-lookup"><span data-stu-id="19512-151">Freeing Excel-Allocated XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="19512-152">В приведенной ниже команде XLL используется функция **xlGetName** для получения строки, содержащей имя DLL-файла и путь к нему, и функция **xlcAlert** для ее отображения в диалоговом окне оповещения.</span><span class="sxs-lookup"><span data-stu-id="19512-152">Consider the following XLL command, which uses **xlGetName** to obtain a string containing the path and file name of the DLL and displays it in an alert dialog box using **xlcAlert**.</span></span>
  
```cs
int WINAPI show_DLL_name(void)
{
    XLOPER12 xDllName;
    if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
    {
        // Display the name.
        Excel12(xlcAlert, 0, 1, &xDllName);
        // Free the memory that Excel allocated for the string.
        Excel12(xlFree, 0, 1, &xDllName);
    }
    return 1;
}

```

<span data-ttu-id="19512-153">Когда функции больше не нужна память, на которую указывает **xDllName**, она может освободить ее, вызвав [функцию xlFree](xlfree.md), одну из функций API C, предназначенную исключительно для библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="19512-153">When the function no longer needs the memory pointed to by **xDllName**, it can free it using a call to the [xlFree function](xlfree.md), one of the DLL-only C API functions.</span></span> 
  
<span data-ttu-id="19512-154">Функция **xlFree** подробно описана в справочнике по функциям (см. статью [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), но обратите внимание на следующее:</span><span class="sxs-lookup"><span data-stu-id="19512-154">The **xlFree** function is fully documented in the function reference section (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), but be aware of the following:</span></span>
  
- <span data-ttu-id="19512-155">Вы можете передавать указатели нескольким структурам данных **XLOPER**/ **XLOPER12** во время одного вызова функции **xlFree**. Единственное ограничение при этом — количество аргументов функции, которое поддерживается в используемой версии Excel (30 в Excel 2003, 255 в Excel 2007 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="19512-155">You can pass pointers to more than one **XLOPER**/ **XLOPER12**s in a single call to **xlFree**, limited only by the number of function arguments supported in the running version of Excel (30 in Excel 2003, 255 starting in Excel 2007).</span></span>
    
- <span data-ttu-id="19512-p111">Функция **xlFree** задает для содержащегося указателя значение **NULL**, чтобы обеспечить безопасность при попытке освобождения уже освобожденной структуры данных **XLOPER**/ **XLOPER12**. **xlFree** — это единственная функция API C, которая изменяет свои аргументы.</span><span class="sxs-lookup"><span data-stu-id="19512-p111">**xlFree** sets the contained pointer to **NULL** to ensure that an attempt to free an **XLOPER**/ **XLOPER12** that has already been freed is safe. **xlFree** is the only C API function that modifies its arguments.</span></span> 
    
- <span data-ttu-id="19512-158">Вы можете безопасно вызывать функцию **xlFree** для любой структуры данных **XLOPER**/ **XLOPER12**, которая используется для получения возвращаемого значения при вызове API C, независимо от того, есть ли в ней указатель на память.</span><span class="sxs-lookup"><span data-stu-id="19512-158">You can safely call **xlFree** on any **XLOPER**/ **XLOPER12** used for the return value of a call to the C API, regardless of whether it contains a pointer to memory.</span></span> 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a><span data-ttu-id="19512-159">Возвращение структур данных XLOPER или XLOPER12 для освобождения в Excel</span><span class="sxs-lookup"><span data-stu-id="19512-159">Returning XLOPER/XLOPER12s to be freed by Excel</span></span>

<span data-ttu-id="19512-p112">Предположим, вы хотите заменить команду, приведенную в качестве примера в предыдущем разделе, на функцию листа, которая возвращает имя DLL-файла и путь к нему, если передается аргумент типа **Boolean** со значением **true**, и **#Н/Д**, если он не передается. Вы не можете вызвать функцию **xlFree**, чтобы освободить память строк, прежде чем возвращать ее в Microsoft Excel. Если ее не освободить, при каждом вызове функции работа надстройки будет приводить к утечке памяти. Чтобы обойти эту проблему, можно в поле **xltype** структуры данных **XLOPER**/ **XLOPER12** задать значение **xlbitXLFree** в файле xlcall.h. В результате Excel получит указание освобождать возвращаемую память после копирования выходного значения.</span><span class="sxs-lookup"><span data-stu-id="19512-p112">Suppose you wanted to modify the example command in the previous section and change it to a worksheet function that returns the DLL path and file name when passed a **Boolean** **true** argument, and **#N/A** otherwise. Clearly you cannot call **xlFree** to release the string memory before returning it to Excel. However, if it is not freed at some point, the add-in will leak memory every time the function is called. To work around this problem, you can set a bit in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitXLFree** in xlcall.h. Setting this tells Excel that it must free the returned memory when it has finished copying the value out.</span></span> 
  
### <a name="example"></a><span data-ttu-id="19512-165">Пример</span><span class="sxs-lookup"><span data-stu-id="19512-165">Example</span></span>

<span data-ttu-id="19512-166">В следующем примере кода показано преобразование команды XLL из предыдущего раздела в функцию листа XLL.</span><span class="sxs-lookup"><span data-stu-id="19512-166">The following code example shows the XLL command in the previous section converted into an XLL worksheet function.</span></span>
  
```cs
LPXLOPER12 WINAPI get_DLL_name(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype == xltypeStr)
    {
// Tell Excel to free the string memory after
// it has copied out the return value.
        xRtnValue.xltype |= xlbitXLFree;
    }
    return &xRtnValue;
}
```

<span data-ttu-id="19512-p113">Функции XLL, которые используют структуры **XLOPER**/ **XLOPER12**, необходимо объявить как такие, которые принимают и возвращают указатели на **XLOPER**/ **XLOPER12**. Использование в этом примере статической памяти **XLOPER12** в функции не является потокобезопасным. Вы можете неправильно зарегистрировать эту функцию как потокобезопасную, но существует риск того, что значения **xRtnValue** будет заменено одним потоком до того, как другой поток завершит работу с ним.</span><span class="sxs-lookup"><span data-stu-id="19512-p113">XLL functions that use **XLOPER**/ **XLOPER12**s must be declared as taking and returning pointers to **XLOPER**/ **XLOPER12**s. The use in this example of a static **XLOPER12** within the function is not thread safe. You could incorrectly register this function as thread safe, but you would risk **xRtnValue** being overwritten by one thread before another thread had finished with it.</span></span> 
  
<span data-ttu-id="19512-p114">Значение **xlbitXLFree** необходимо задавать после вызова функции обратного вызова Excel, которая его выделяет. Если задать его до этого, оно будет перезаписано и не даст нужного эффекта. Если вы хотите использовать это значение в качестве аргумента во время вызова другой функции API C до его возвращения на лист, это значение следует задавать после такого вызова. В противном случае вы перепутаете функции, которые не маскируют это значение до проверки типа **XLOPER**/ **XLLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="19512-p114">You must set **xlbitXLFree** after the call to the Excel callback that allocates it. If you set it before this, it is overwritten and does not have the effect that you want. If you intend to use the value as an argument in a call to another C API function before returning it to the worksheet, you should set this bit after any such call. Otherwise, you will confuse functions that do not mask this bit before checking the **XLOPER**/ **XLLOPER12** type.</span></span> 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a><span data-ttu-id="19512-174">Возвращение структур данных XLOPER или XLOPER12 для освобождения в библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="19512-174">Returning XLOPER/XLOPER12s to be freed by the DLL</span></span>

<span data-ttu-id="19512-p115">Аналогичная проблема возникает, когда надстройка XLL выделяет память **XLOPER**/ **XLOPER12** и хочет возвратить ее в Excel. Excel распознает еще одно значение, которое можно задать в поле **xltype** структуры данных **XLOPER**/ **XLOPER12**, — **xlbitDLLFree** в файле xlcall.h.</span><span class="sxs-lookup"><span data-stu-id="19512-p115">A similar problem to this occurs when your XLL has allocated memory for an **XLOPER**/ **XLOPER12** and wants to return it to Excel. Excel recognizes another bit that can be set in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitDLLFree** in xlcall.h.</span></span> 
  
<span data-ttu-id="19512-p116">Получая структуру **XLOPER**/ **XLOPER12** с этим значением, Excel пытается вызвать функцию [xlAutoFree](xlautofree-xlautofree12.md) (для **XLOPER**) или **xlAutoFree12** (для **XLOPER12**), которую должна экспортировать надстройка XLL. Эта функция более подробно описана в справочнике по функциям (см. статью [Функции диспетчера надстроек и интерфейса XLL](add-in-manager-and-xll-interface-functions.md)), но пример минимальной реализации приведен здесь. Она предназначена для освобождения памяти **XLOPER**/ **XLOPER12** тем же способом, которым она изначально была выделена.</span><span class="sxs-lookup"><span data-stu-id="19512-p116">When Excel receives **an XLOPER**/ **XLOPER12** with this bit set, it tries to call a function that should be exported by the XLL called [xlAutoFree](xlautofree-xlautofree12.md) (for **XLOPER**s) or **xlAutoFree12** (for **XLOPER12**s). This function is described more fully in the function reference (see [Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)), but an example minimal implementation is given here. Its purpose is to free the **XLOPER**/ **XLOPER12** memory in a way that is consistent with how it was originally allocated.</span></span> 
  
### <a name="examples"></a><span data-ttu-id="19512-180">Примеры</span><span class="sxs-lookup"><span data-stu-id="19512-180">Examples</span></span>

<span data-ttu-id="19512-181">Действие функции в приведенном ниже примере аналогично действию предыдущей функции (за исключением того, что она содержит текст "The full pathname for this DLL is" перед именем DLL).</span><span class="sxs-lookup"><span data-stu-id="19512-181">The following example function does the same as the previous function except that it includes the text "The full pathname for this DLL is " before the DLL name.</span></span>
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_2(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype != xltypeStr)
        return &xRtnValue;
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = xRtnValue.val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, xRtnValue.val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, &xRtnValue);
// Now reuse the XLOPER12 for the new string.
    xRtnValue.val.str = msg_text;
// Tell Excel to call back into the DLL to free the string
// memory after it has copied out the return value.
    xRtnValue.xltype     = xltypeStr | xlbitDLLFree;
    return &xRtnValue;
}
```

<span data-ttu-id="19512-182">Ниже показана минимальная реализация функции **xlAutoFree12** в надстройке XLL, экспортировавшей предыдущую функцию.</span><span class="sxs-lookup"><span data-stu-id="19512-182">A minimally sufficient implementation of **xlAutoFree12** in the XLL that exported the previous function would be as follows.</span></span> 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

<span data-ttu-id="19512-p117">Этой реализации достаточно, только если надстройка XLL возвращает строки **XLOPER12** и они выделяются с помощью функции **malloc**. Обратите внимание, что в этом случае тест</span><span class="sxs-lookup"><span data-stu-id="19512-p117">This implementation is only sufficient if the XLL only returns **XLOPER12** strings, and those strings are only allocated using **malloc**. Note that the test</span></span> 
  
 ` if(p_oper->xltype == xltypeStr) `
  
<span data-ttu-id="19512-185">даст сбой, так как задано значение **xlbitDLLFree**.</span><span class="sxs-lookup"><span data-stu-id="19512-185">would fail in this case because **xlbitDLLFree** is set.</span></span> 
  
<span data-ttu-id="19512-186">В общем, функции **xlAutoFree** и **xlAutoFree12** необходимо реализовать так, чтобы они освобождали память, связанную с созданными при помощи XLL массивами **xltypeMulti** и внешними ссылками **xltypeRef**.</span><span class="sxs-lookup"><span data-stu-id="19512-186">In general, **xlAutoFree** and **xlAutoFree12** should be implemented so that they free memory associated with XLL-created **xltypeMulti** arrays and **xltypeRef** external references.</span></span> 
  
<span data-ttu-id="19512-p118">Вы можете реализовать функции XLL так, чтобы ВСЕ они возвращали динамически выделяемые структуры данных **XLOPER** и **XLOPER12**. В этом случае потребуется задать значение **xlbitDLLFree** для всех таких структур данных **XLOPER** и **XLOPER12** независимо от подтипа. Кроме того, необходимо реализовать функции **xlAutoFree** и **xlAutoFree12**, чтобы освободить эту память, а также память, указанную в **XLOPER**/ **XLOPER12**. Это один из способов сделать возвращаемое значение потокобезопасным. Например, предыдущую функцию можно переписать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="19512-p118">You might decide to implement your XLL functions so that they ALL return dynamically allocated **XLOPER**s and **XLOPER12**s. In this case, you would need to set **xlbitDLLFree** on all such **XLOPER**s and **XLOPER12**s regardless of the sub-type. You would also need to implement **xlAutoFree** and **xlAutoFree12** so that this memory was freed and also any memory pointed to within the **XLOPER**/ **XLOPER12**. This approach is one way to make the return value thread safe. For example, the previous function could be rewritten as follows.</span></span>
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_3(int calculation_trigger)
{
// Thread-safe
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
    Excel12(xlfGetName, pxRtnValue, 0);
// If xlfGetName failed, pxRtnValue will be #VALUE!
    if(pxRtnValue->xltype != xltypeStr)
    {
// Even though an error type does not point to memory,
// Excel needs to pass this oper to xlAutoFree12 to
// free pxRtnValue itself.
        pxRtnValue->xltype |= xlbitDLLFree;
        return pxRtnValue;
    }
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = pxRtnValue->val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, pxRtnValue->val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, pxRtnValue);
// Now reuse the XLOPER12 for the new string.
    pxRtnValue->val.str = msg_text;
    pxRtnValue->xltype = xltypeStr | xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
    free(p_oper);
}
```

<span data-ttu-id="19512-192">Дополнительные сведения о функциях **xlAutoFree** и **xlAutoFree12** см. в статье [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).</span><span class="sxs-lookup"><span data-stu-id="19512-192">For more information about **xlAutoFree** and **xlAutoFree12**, see [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).</span></span>
  
## <a name="returning-modify-in-place-arguments"></a><span data-ttu-id="19512-193">Возвращение аргументов, изменяемых на месте</span><span class="sxs-lookup"><span data-stu-id="19512-193">Returning Modify-in-Place Arguments</span></span>

<span data-ttu-id="19512-p119">В Excel функция XLL может возвращать значение, изменяя аргумент на месте. Это возможно, только если аргумент передается в виде указателя. Для этого функцию необходимо зарегистрировать так, чтобы указать Excel, какой аргумент будет изменяться.</span><span class="sxs-lookup"><span data-stu-id="19512-p119">Excel allows an XLL function to return a value by modifying an argument in place. You can only do this with an argument passed in as a pointer. To work like this, the function must be registered in a way that tells Excel which argument will be modified.</span></span> 
  
<span data-ttu-id="19512-197">Этот метод для возвращения значения поддерживается для всех типов данных, которые можно передавать с помощью указателя, но особенно полезен для следующих типов:</span><span class="sxs-lookup"><span data-stu-id="19512-197">This method of returning a value is supported for all data types that can be passed by pointer but is especially useful for the following types:</span></span>
  
- <span data-ttu-id="19512-198">строки байтов ASCII, для которых предусмотрен счетчик длины и которые оканчиваются нулем;</span><span class="sxs-lookup"><span data-stu-id="19512-198">Length-counted and null-terminated ASCII byte strings</span></span>
    
- <span data-ttu-id="19512-199">строки расширенных символов Юникода со счетчиком длины, оканчивающиеся нулем (в Excel 2007 и более поздних версий);</span><span class="sxs-lookup"><span data-stu-id="19512-199">Length-counted and null-terminated Unicode wide character strings (starting in Excel 2007)</span></span>
    
- <span data-ttu-id="19512-200">массивы **FP** с плавающей запятой;</span><span class="sxs-lookup"><span data-stu-id="19512-200">**FP** floating-point arrays</span></span> 
    
- <span data-ttu-id="19512-201">массивы **FP12** с плавающей запятой (в Excel 2007 и более поздних версий).</span><span class="sxs-lookup"><span data-stu-id="19512-201">**FP12** floating-point arrays (starting in Excel 2007)</span></span> 
    
> [!NOTE]
> <span data-ttu-id="19512-p120">Не следует пытаться возвращать таким образом структуру **XLOPER** или **XLOPER12**. Дополнительные сведения см. в статье [Известные проблемы с разработкой XLL в Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="19512-p120">You should not try to return **XLOPER**s or **XLOPER12**s in this manner. For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span> 
  
<span data-ttu-id="19512-p121">Преимущество этого способа над использованием оператора возвращения заключается в том, что Excel выделяет память для возвращаемых значений. Завершив чтение возвращаемых данных, Excel освобождает память. Это освобождает функцию XLL от управления памятью. Этот способ потокобезопасен: когда функция в Excel вызывается одновременно в различных потоках, для каждого такого вызова предусмотрен свой буфер.</span><span class="sxs-lookup"><span data-stu-id="19512-p121">The advantage of using this technique, instead of just using the return statement, is that Excel allocates the memory for the return values. Once Excel has finished reading the returned data, it releases the memory. This takes the memory management tasks away from the XLL function. This technique is thread safe: If called concurrently by Excel on different threads, each function call on each thread has its own buffer.</span></span>
  
<span data-ttu-id="19512-p122">Это удобно при использовании приведенных выше типов данных, потому что механизм обратного вызова DLL для освобождения памяти после возвращения, который используется для структуры **XLOPER**/ **XLOPER12**, не существует для простых строк и массивов **FP**/ **FP12**. Следовательно, при возвращении созданной с помощью DLL строки или массива с плавающей запятой у вас есть приведенные ниже варианты.</span><span class="sxs-lookup"><span data-stu-id="19512-p122">It is useful for the previously listed data types in particular because the mechanism for calling back into the DLL to free memory post-return that exists for **XLOPER**/ **XLOPER12**s does not exist for simple strings and **FP**/ **FP12** arrays. Therefore, when returning a DLL-created string or floating-point array, you have the following choices:</span></span> 
  
- <span data-ttu-id="19512-p123">Установите постоянный указатель для динамически выделяемого буфера, возвратите указатель. Во время следующего вызова функции (1) убедитесь, что значение указателя — не ноль, (2) освободите ресурсы, выделенные во время предыдущего вызова, и обнулите значение указателя, (3) повторно используйте указатель для нового выделенного блока памяти.</span><span class="sxs-lookup"><span data-stu-id="19512-p123">Set a persistent pointer to a dynamically allocated buffer, return the pointer. On the next call to the function (1) check that the pointer is not null, (2) free the resources allocated on the previous call and reset the pointer to null, (3) reuse the pointer for a newly allocated block of memory.</span></span>
    
- <span data-ttu-id="19512-212">Создайте строки и массивы в статическом буфере, который не нужно освобождать, и возвратите указатель в него.</span><span class="sxs-lookup"><span data-stu-id="19512-212">Create your strings and arrays in a static buffer that does not need to be freed, and return a pointer to that.</span></span>
    
- <span data-ttu-id="19512-213">Измените аргументы на месте, записав строку или массив непосредственно в пространство, выделенное приложением Excel.</span><span class="sxs-lookup"><span data-stu-id="19512-213">Modify an argument in place, writing your string or array directly into the space set aside by Excel.</span></span>
    
<span data-ttu-id="19512-214">В противном случае необходимо создать **XLOPER**/ **XLOPER12** и использовать функцию **xlbitDLLFree**, а также **xlAutoFree**/ **xlAutoFree12** для освобождения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19512-214">Otherwise, you must create an **XLOPER**/ **XLOPER12**, and use **xlbitDLLFree** and **xlAutoFree**/ **xlAutoFree12** to release the resources.</span></span> 
  
<span data-ttu-id="19512-p124">Последний вариант может быть самым простым, если передается аргумент того же типа, что и возвращаемое значение. Обратите внимание, что размеры буферов ограничены и его не следует переполнять (это может вызвать сбой Excel). Размеры буфера для строк и массивов **FP**/ **FP12** приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="19512-p124">The last option might be the simplest in those cases in which you are being passed an argument of the same type as the return value. The key point to remember is that the buffer sizes are limited and you must be very careful not to overrun them. Getting this wrong could crash Excel. Buffer sizes for strings and **FP**/ **FP12** arrays are discussed next.</span></span> 
  
## <a name="strings"></a><span data-ttu-id="19512-219">Строки</span><span class="sxs-lookup"><span data-stu-id="19512-219">Strings</span></span>

<span data-ttu-id="19512-220">Проблемы с управлением памятью строк — наиболее распространенная причина нестабильной работы приложений и надстроек. Это понятно, учитывая множество различных типов строк и способов обработки. Есть строки, которые оканчиваются нулем или для которых используется счетчик длины (а еще строки, для которых выполняются оба эти условия); статические или динамические буферы; строки фиксированной длины или практически неограниченной длины; память, управляемая операционной системой (например, OLE Bstr), или неуправляемые строки, а также другие варианты.</span><span class="sxs-lookup"><span data-stu-id="19512-220">Problems with the management of string memory are arguably the most common cause of instability in applications and add-ins. It is understandable perhaps, given the variety of ways in which strings are handled: null-terminated or length-counted (or both); static or dynamic buffers; fixed length or almost unlimited length; operating-system managed memory (for example, OLE Bstr) or unmanaged strings; and so on.</span></span>
  
<span data-ttu-id="19512-p125">Программисты C/C++ чаще всего используют строки, оканчивающиеся нулем. Стандартная библиотека C предназначена для работы с такими строками. Статические строковые литералы в коде компилируются в строки, оканчивающиеся нулем. Кроме того, Excel работает со строками со счетчиком длины, которые обычно не оканчиваются нулем. Сочетание этих фактов требует четкого и последовательного подхода к обработке строк и памяти строк в DLL и XLL.</span><span class="sxs-lookup"><span data-stu-id="19512-p125">C/C++ programmers are most familiar with null-terminated strings. The standard C library is designed to work with such strings. Static string literals in code are compiled into null-terminated strings. Alternatively, Excel works with length-counted strings that are not in general null-terminated. The combination of these facts requires a clear and consistent approach within your DLL/XLL regarding how you handle strings and string memory.</span></span>
  
<span data-ttu-id="19512-226">Ниже приведены наиболее распространенные проблемы.</span><span class="sxs-lookup"><span data-stu-id="19512-226">The most common problems are as follows:</span></span>
  
- <span data-ttu-id="19512-227">Передача пустого или недопустимого указателя в функцию, которая ожидает допустимый указатель и не проверяет или не может проверить его допустимость.</span><span class="sxs-lookup"><span data-stu-id="19512-227">The passing of a null or invalid pointer to a function that expects a valid pointer and does not or cannot check the pointer's validity itself.</span></span>
    
- <span data-ttu-id="19512-228">Переполнение буфера строки функцией, которая не сопоставляет или не может сопоставить размер буфера и длину записываемой строки.</span><span class="sxs-lookup"><span data-stu-id="19512-228">The overrunning of the bounds of a string buffer by a function that does not or cannot check the length of the buffer against the length of the string being written.</span></span>
    
- <span data-ttu-id="19512-229">Попытка освободить память буфера строки, если он статический или уже освобожденный, а также если способы освобождения и выделения не совпадают.</span><span class="sxs-lookup"><span data-stu-id="19512-229">Trying to free string buffer memory that is either static, or has been freed already, or was not allocated in a way that is consistent with how it is being freed.</span></span>
    
- <span data-ttu-id="19512-230">Утечки памяти в результате выделения без последующего освобождения строк (обычно в часто вызываемой функции).</span><span class="sxs-lookup"><span data-stu-id="19512-230">Memory leaks that result from strings being allocated and then not freed, usually in a frequently called function.</span></span>
    
### <a name="rules-for-strings"></a><span data-ttu-id="19512-231">Правила для строк</span><span class="sxs-lookup"><span data-stu-id="19512-231">Rules for Strings</span></span>

<span data-ttu-id="19512-p126">Как и для **XLOPER**/ **XLOPER**, для строк существуют правила и рекомендации, которым необходимо следовать. Рекомендации не отличаются от приведенных в предыдущем разделе. Дополнительные правила для строк приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="19512-p126">As with **XLOPER**/ **XLOPER**s, there are rules and guidelines you should follow. The guidelines are the same as given in the previous section. The rules here are an extension of the rules specifically for strings.</span></span>
  
 <span data-ttu-id="19512-235">**Правила:**</span><span class="sxs-lookup"><span data-stu-id="19512-235">**Rules:**</span></span>
  
- <span data-ttu-id="19512-p127">Не пытайтесь освободить память или перезаписать строки **XLOPER**/ **XLOPER12**, а также простые строки со счетчиком длины или строки, оканчивающиеся нулем, которые передаются как аргументы в функцию XLL. Такие аргументы предназначены только для чтения.</span><span class="sxs-lookup"><span data-stu-id="19512-p127">Do not try to free memory or overwrite string **XLOPER**/ **XLOPER12**s or simple length-counted or null-terminated strings passed as arguments to your XLL function. You should treat such arguments as read-only.</span></span>
    
- <span data-ttu-id="19512-238">Если Excel выделяет память для строки **XLOPER**/ **XLOPER12** с возвращаемым значением функции обратного вызова API C, освободите ее с помощью функции **xlFree** или задайте значение **xlbitXLFree** при ее возвращении в Excel из функции XLL.</span><span class="sxs-lookup"><span data-stu-id="19512-238">Where Excel allocates memory for a string **XLOPER**/ **XLOPER12** for the return value of a C API callback function, use **xlFree** to free it, or set **xlbitXLFree** if returning it to Excel from an XLL function.</span></span> 
    
- <span data-ttu-id="19512-239">Если библиотека DLL динамически выделяет буфер строк для **XLOPER**/ **XLOPER12**, после завершения работы освободите его тем же способом, который использовался для выделения, или задайте **xlbitDLLFree** при его возвращении в Excel из функции XLL, а затем освободите его с помощью функции **xlAutoFree**/ **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="19512-239">Where your DLL dynamically allocates a string buffer for an **XLOPER**/ **XLOPER12**, free it in a way consistent with how you allocated it when done, or set **xlbitDLLFree** if returning it to Excel from an XLL function and then free it in **xlAutoFree**/ **xlAutoFree12**.</span></span>
    
- <span data-ttu-id="19512-p128">Если Excel выделяет память для массива **xltypeMulti**, возвращаемого в библиотеку DLL во время вызова API C, не перезаписывайте строки **XLOPER**/ **XLOPER12** в массиве. Для освобождения этих массивов необходимо использовать только функцию **xlFree** или значение **xlbitXLFree** при возвращении из функции XLL.</span><span class="sxs-lookup"><span data-stu-id="19512-p128">If Excel has allocated memory for an **xltypeMulti** array returned to your DLL in a call to the C API, do not overwrite any string **XLOPER**/ **XLOPER12**s within the array. Such arrays must only be freed using **xlFree**, or, if being returned by an XLL function, by setting **xlbitXLFree**.</span></span>
    
### <a name="string-types-supported"></a><span data-ttu-id="19512-242">Поддерживаемые типы строк</span><span class="sxs-lookup"><span data-stu-id="19512-242">String Types Supported</span></span>

<span data-ttu-id="19512-243">**Строки xltypeStr для XLOPER/XLOPER12 в API C**</span><span class="sxs-lookup"><span data-stu-id="19512-243">**C API xltypeStr XLOPER/XLOPER12s**</span></span>

|<span data-ttu-id="19512-244">\*\*Строка байтов: \*\*XLOPER\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="19512-244">\*\*Byte strings: \*\*XLOPER\*\*\*\*</span></span>|<span data-ttu-id="19512-245">\*\*Строки расширенных символов: \*\*XLOPER12\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="19512-245">\*\*Wide character strings: \*\*XLOPER12\*\*\*\*</span></span>|
|:-----|:-----|
|<span data-ttu-id="19512-246">Все версии Excel</span><span class="sxs-lookup"><span data-stu-id="19512-246">All versions of Excel</span></span>  <br/> |<span data-ttu-id="19512-247">Начиная с Excel 2007</span><span class="sxs-lookup"><span data-stu-id="19512-247">Starting in Excel 2007</span></span>  <br/> |
|<span data-ttu-id="19512-248">Максимальная длина: 255 байтов расширенного кода ASCII</span><span class="sxs-lookup"><span data-stu-id="19512-248">Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="19512-249">Максимальная длина: 32 767 символов Юникода</span><span class="sxs-lookup"><span data-stu-id="19512-249">Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="19512-250">Первый байт (без знака) = длина</span><span class="sxs-lookup"><span data-stu-id="19512-250">First (unsigned) byte = length</span></span>  <br/> |<span data-ttu-id="19512-251">Первый символ Юникода = длина</span><span class="sxs-lookup"><span data-stu-id="19512-251">First Unicode character = length</span></span>  <br/> |
   
> [!IMPORTANT]
> <span data-ttu-id="19512-252">Строки **XLOPER** или **XLOPER12** не должны оканчиваться нулем.</span><span class="sxs-lookup"><span data-stu-id="19512-252">Do not assume null termination of **XLOPER** or **XLOPER12** strings.</span></span> 
  
<span data-ttu-id="19512-253">**Строки C/C++**</span><span class="sxs-lookup"><span data-stu-id="19512-253">**C/C++ strings**</span></span>

|<span data-ttu-id="19512-254">**Строки байтов**</span><span class="sxs-lookup"><span data-stu-id="19512-254">**Byte strings**</span></span>|<span data-ttu-id="19512-255">**Строки расширенных символов**</span><span class="sxs-lookup"><span data-stu-id="19512-255">**Wide character strings**</span></span>|
|:-----|:-----|
|<span data-ttu-id="19512-256">Оканчивающиеся нулем (**char** \*), тип "C", максимальная длина составляет 255 байтов расширенного кода ASCII</span><span class="sxs-lookup"><span data-stu-id="19512-256">Null-terminated (**char** \*) "C" Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="19512-257">Оканчивающиеся нулем (**wchar_t** \*), тип "C%", максимальная длина составляет 32 767 символов Юникода</span><span class="sxs-lookup"><span data-stu-id="19512-257">Null-terminated (**wchar_t** \*) "C%" Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="19512-258">Со счетчиком длины (**unsigned char** \*) "D"</span><span class="sxs-lookup"><span data-stu-id="19512-258">Length-counted (**unsigned char** \*) "D"</span></span>  <br/> |<span data-ttu-id="19512-259">Со счетчиком длины (**wchar_t** \*) "D%"</span><span class="sxs-lookup"><span data-stu-id="19512-259">Length-counted (**wchar_t** \*) "D%"</span></span>  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a><span data-ttu-id="19512-260">Строки в массивах XLOPER/XLOPER12 xltypeMulti</span><span class="sxs-lookup"><span data-stu-id="19512-260">Strings in xltypeMulti XLOPER/XLOPER12 Arrays</span></span>

<span data-ttu-id="19512-p129">В некоторых случаях Excel создает массив **xltypeMulti** для использования в библиотеках DLL и XLL. Несколько информационных функций XLM возвращают такие массивы. Например, функция API C **xlfGetWorkspace** при передаче ей аргумента *44* возвращает массив, содержащий строки, которые описывают все зарегистрированные процедуры DLL. Функция API C **xlfDialogBox** возвращает измененную копию аргумента массива, содержащую глубокие копии строк. Возможно, чаще всего библиотека XLL обнаруживает массив **xltypeMulti** при его передаче в качестве аргумента в функцию XLL или преобразовании в этот тип из типа ссылок на диапазон. В таких случаях Excel создает глубокие копии строк в исходных ячейках и указывает на них в массиве.</span><span class="sxs-lookup"><span data-stu-id="19512-p129">In several cases, Excel creates an **xltypeMulti** array for use in your DLL/XLL. Several of the XLM information functions return such arrays. For example, the C API function **xlfGetWorkspace**, when passed the argument  *44*  , returns an array containing strings that describe all the currently registered DLL procedures. The C API function **xlfDialogBox** returns a modified copy of its array argument, containing deep copies of the strings. Perhaps the most common way an XLL encounters an **xltypeMulti** array is where it has been passed as an argument to an XLL function, or it has been coerced to this type from a range reference. In these latter cases, Excel creates deep copies of the strings in the source cells and points to these within the array.</span></span> 
  
<span data-ttu-id="19512-p130">Если вы хотите изменить эти строки в библиотеке DLL, следует создать собственные глубокие копии. При создании собственных массивов **xltypeMulti** не следует помещать в них выделенные приложением Excel строки **XLOPER**/ **XLOPER12**. Существует риск того, что они будут освобождены неправильно или не освобождены вообще. Кроме того, следует создавать глубокие копии строк и хранить указатели на копии в массиве.</span><span class="sxs-lookup"><span data-stu-id="19512-p130">Where you want to modify these strings in your DLL, you should make your own deep copies. When you are creating your own **xltypeMulti** arrays, you should not place Excel-allocated string **XLOPER**/ **XLOPER12**s within them. This risks you not freeing them correctly later, or not freeing them at all. Again, you should make deep copies of the strings and store pointers to the copies in the array.</span></span>
  
 <span data-ttu-id="19512-271">**Примеры**</span><span class="sxs-lookup"><span data-stu-id="19512-271">**Examples**</span></span>
  
<span data-ttu-id="19512-p131">В следующем примере функция создает динамически выделяемую копию строки Юникода со счетчиком длины. Обратите внимание, что вызывающая сторона в конечном счете должна освободить память, выделяемую в этом примере, с помощью оператора **delete**[], а исходная строка не должна оканчиваться нулем. Строка копии усекается, если это необходимо для безопасности, и не оканчивается нулем.</span><span class="sxs-lookup"><span data-stu-id="19512-p131">The following example function creates a dynamically allocated copy of a length-counted Unicode string. Note that the caller must ultimately free the memory allocated in this example using **delete**[], and that the source string is not assumed to be null terminated. The copy string is truncated if necessary for safety, and is not null terminated.</span></span>
  
```cs
#include <string.h>
#define MAX_V12_STRBUFFLEN    32678
    
wchar_t * deep_copy_wcs(const wchar_t *p_source)
{
    if(!p_source)
        return NULL;
    size_t source_len = p_source[0];
    bool truncated = false;
    if(source_len >= MAX_V12_STRBUFFLEN)
    {
        source_len = MAX_V12_STRBUFFLEN - 1; // Truncate the copy
        truncated = true;
    }
    wchar_t *p_copy = new wchar_t[source_len + 1];
    wcsncpy_s(p_copy, p_source, source_len + 1);
    if(truncated)
        p_copy[0] = source_len;
    return p_copy;
}
```

<span data-ttu-id="19512-p132">Затем с помощью этой функции можно безопасно копировать **XLOPER12**, как показано на примере следующей экспортируемой функции XLL, возвращающей копию аргумента, если это строка. Все другие типы возвращаются как пустая строка. Обратите внимание, что диапазоны не обрабатываются — функция возвращает **#ЗНАЧ!**. Эту функцию необходимо зарегистрировать как такую, которая принимает аргумент типа "U", для передачи ссылок в виде значений. Она эквивалентна встроенной функции листа **T()** (за исключением того, что **AsText** также преобразует ошибки в пустые строки). В этом примере кода предполагается, что **xlAutoFree12** освобождает переданный указатель, а также его содержимое, с помощью оператора **delete**.</span><span class="sxs-lookup"><span data-stu-id="19512-p132">This function can then be safely used to copy an **XLOPER12**, as shown in the following exportable XLL function that returns a copy of its argument if it is a string. All other types are returned as a zero-length string. Note that ranges are not handled—the function returns **#VALUE!**. The function must be registered as taking a type U argument so that references are passed in as values. This is equivalent to the built-in worksheet function **T()** except that **AsText** also converts errors to zero-length strings. This code example assumes that **xlAutoFree12** frees the passed-in pointer, and also its contents, using **delete**.</span></span>
  
```cs
LPXLOPER12 WINAPI AsText(LPXLOPER12 pArg)
{
    LPXLOPER12 pRtnVal = new XLOPER12;
// If the input was an array, only operate on the top-left element.
    LPXLOPER *pTemp;
    if(pArg->xltype == xltypeMulti)
        pTemp = pArg->val.array.lparray;
    else
        pTemp = pArg;
    switch(pTemp->xltype)
    {
        case xltypeErr:
        case xltypeNum:
        case xltypeMissing:
        case xltypeNil:
        case xltypeBool:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(L"\000");
            return pRtnVal;
        case xltypeStr:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(pTemp->val.str);
            return pRtnVal;
        
        default: // xltypeSRef, xltypeRef, xltypeFlow, xltypeInt
            pRtnVal->xltype = xltypeErr | xlbitDLLFree;
            pRtnVal->val.err = xlerrValue;
            return pRtnVal;
    }
}
```

### <a name="returning-modify-in-place-string-arguments"></a><span data-ttu-id="19512-281">Возвращение строковых аргументов, изменяемых на месте</span><span class="sxs-lookup"><span data-stu-id="19512-281">Returning Modify-in-Place String Arguments</span></span>

<span data-ttu-id="19512-p133">Аргументы, зарегистрированные как аргументы типов **F**, **G**, **F%** и **G%**, можно изменять на месте. Подготавливая строковые аргументы для этих типов, Excel создает буфер максимального размера. Затем Excel копирует в него строку аргумента, даже если она значительно короче. Это позволяет функции XLL записывать возвращаемое значение непосредственно в ту же память.</span><span class="sxs-lookup"><span data-stu-id="19512-p133">Arguments registered as types **F**, **G**, **F%**, and **G%** can be modified in place. When Excel is preparing string arguments for these types, it creates a maximum length buffer. Then it copies the argument string into that, even if this string is very much shorter. This enables the XLL function to write its return value directly into the same memory.</span></span> 
  
<span data-ttu-id="19512-286">Ниже приведены размеры буфера, установленные для этих типов.</span><span class="sxs-lookup"><span data-stu-id="19512-286">Buffer sizes set apart for these types are as follows:</span></span>
  
- <span data-ttu-id="19512-287">**Строки байтов:** 256 байтов, включая счетчик длины (тип "G") или завершающий символ нуля (тип "F").</span><span class="sxs-lookup"><span data-stu-id="19512-287">**Byte strings:** 256 bytes including the length counter (type G) or null-termination (type F).</span></span> 
    
- <span data-ttu-id="19512-288">**Строки в кодировке Юникод:** 32 768 расширенных символов (65 536 байтов), включая счетчик длины (тип "G%") или завершающий символ нуля (тип "F%").</span><span class="sxs-lookup"><span data-stu-id="19512-288">**Unicode strings:** 32,768 wide characters (65,536 bytes) including the length counter (type G%) or null-termination (type F%).</span></span> 
    
> [!NOTE]
> <span data-ttu-id="19512-p134">Эту функцию невозможно вызвать непосредственно из Visual Basic для приложений (VBA), так как вы не можете гарантировать выделение буфера достаточно большого размера. Безопасно эту функцию можно вызвать только из другой библиотеки DLL, если вы явно выделили достаточно большой буфер.</span><span class="sxs-lookup"><span data-stu-id="19512-p134">You cannot call such a function directly from Visual Basic for Applications (VBA) because you cannot ensure that a sufficiently large buffer has been allocated. You can only call such a function from another DLL safely if you have explicitly passed a big enough buffer.</span></span> 
  
<span data-ttu-id="19512-p135">Ниже приведен пример функции XLL, которая обращает последовательность расширенных символов в переданной строке, оканчивающейся нулем, используя стандартную функцию библиотеки **wcsrev**. Аргумент в этом случае будет зарегистрирован как аргумент типа **F%**.</span><span class="sxs-lookup"><span data-stu-id="19512-p135">Here is an example of an XLL function that reverses a passed-in null-terminated wide character string using the standard library function **wcsrev**. The argument in this case would be registered as type **F%**.</span></span>
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a><span data-ttu-id="19512-293">Постоянное хранилище (двоичные имена)</span><span class="sxs-lookup"><span data-stu-id="19512-293">Persistent Storage (Binary Names)</span></span>

<span data-ttu-id="19512-294">Двоичные имена определяются и связываются с блоками двоичных (то есть неструктурированных) данных, хранящихся вместе с книгой.</span><span class="sxs-lookup"><span data-stu-id="19512-294">Binary names are defined and associated with blocks of binary, that is, unstructured, data that is stored together with the workbook.</span></span> <span data-ttu-id="19512-295">Они создаются с помощью функции [xlDefineBinaryName](xldefinebinaryname.md), а для получения данных используется функция [xlGetBinaryName](xlgetbinaryname.md).</span><span class="sxs-lookup"><span data-stu-id="19512-295">They are created using the function [xlDefineBinaryName](xldefinebinaryname.md), and the data is retrieved using the function [xlGetBinaryName](xlgetbinaryname.md).</span></span> <span data-ttu-id="19512-296">Подробные описания обеих функций представлены в справочнике по функциям (см. статью [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)). Обе эти функции используют **XLOPER**/ **XLOPER12** для **xltypeBigData**.</span><span class="sxs-lookup"><span data-stu-id="19512-296">Both functions are described in more detail in the function reference (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), and both use the **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> 
  
<span data-ttu-id="19512-297">Сведения об известных проблемах, которые ограничивают практическое применение двоичных имен, см. в статье [Известные проблемы](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="19512-297">For information about known issues that limit the practical applications of binary names, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="excel-stack"></a><span data-ttu-id="19512-298">Стек Excel</span><span class="sxs-lookup"><span data-stu-id="19512-298">Excel Stack</span></span>

<span data-ttu-id="19512-p137">Excel использует стек вместе со всеми загруженными библиотеками DLL. Места в стеке обычно более чем достаточно для обычного использования. О нем не нужно беспокоиться, если вы выполняете следующие рекомендации:</span><span class="sxs-lookup"><span data-stu-id="19512-p137">Excel shares its stack space with all the DLLs it has loaded. Stack space is usually more than adequate for ordinary use, and you do not need to be concerned about it as long as you follow a few guidelines:</span></span> 
  
- <span data-ttu-id="19512-p138">Не передавайте очень большие структуры в качестве аргументов функций в виде значений в стеке. Передавайте указатели или ссылки.</span><span class="sxs-lookup"><span data-stu-id="19512-p138">Do not pass very large structures as arguments to functions by value on the stack. Pass pointers or references instead.</span></span>
    
- <span data-ttu-id="19512-p139">Не возвращайте большие структуры в стеке. Возвращайте указатели на статическую или динамически выделяемую память или используйте аргументы, передаваемые с использованием ссылки.</span><span class="sxs-lookup"><span data-stu-id="19512-p139">Do not return large structures on the stack. Return pointers to static or dynamically allocated memory, or use arguments passed by reference.</span></span>
    
- <span data-ttu-id="19512-p140">Не объявляйте очень большие структуры автоматических переменных в коде функции. Если необходимо, объявите их как статические.</span><span class="sxs-lookup"><span data-stu-id="19512-p140">Do not declare very large automatic variable structures in the function code. If you need them, declare them as static.</span></span>
    
- <span data-ttu-id="19512-p141">Не вызывайте функции рекурсивно, если не уверены, что рекурсия всегда будет неполной. Вместо этого используйте цикл.</span><span class="sxs-lookup"><span data-stu-id="19512-p141">Do not call functions recursively unless you are sure the depth of recursion will always be shallow. Try using a loop instead.</span></span>
    
<span data-ttu-id="19512-p142">Получая обратный вызов от библиотеки DLL с помощью API C, Excel сначала проверяет, достаточно ли места в стеке для самого худшего сценария. Если Excel посчитает, что свободного места может быть недостаточно, он обработает вызов как небезопасный, даже если на самом деле места достаточно. В этом случае при обратном вызове возвращается код **xlretFailed**. При обычном использовании API C и стека сбой вызова API C вряд ли произойдет по этой причине.</span><span class="sxs-lookup"><span data-stu-id="19512-p142">When a DLL calls back into Excel using the C API, Excel first checks whether there is enough space on the stack for the worst-case usage call that could be made. If it thinks there might be insufficient room, it will fail the call to be safe, even though there might actually have been enough space for that particular call. In this case, the callbacks return the code **xlretFailed**. For ordinary use of the C API and the stack, this is an unlikely cause of the failure of a C API call.</span></span>
  
<span data-ttu-id="19512-313">Если вы хотите исключить недостаток места в стеке из возможных причин сбоя, узнайте объем стека, вызвав функцию [xlStack](xlstack.md).</span><span class="sxs-lookup"><span data-stu-id="19512-313">If you are concerned, or just curious, or you want to eliminate lack of stack space as a reason for an unexplained failure, you can find out how much stack space there is with a call to the [xlStack](xlstack.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="19512-314">См. также</span><span class="sxs-lookup"><span data-stu-id="19512-314">See also</span></span>



[<span data-ttu-id="19512-315">Многопоточный пересчет в Excel</span><span class="sxs-lookup"><span data-stu-id="19512-315">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="19512-316">Многопоточность и конфликты памяти в Excel</span><span class="sxs-lookup"><span data-stu-id="19512-316">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
  
[<span data-ttu-id="19512-317">Разработка XLL-файлов для Excel</span><span class="sxs-lookup"><span data-stu-id="19512-317">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

