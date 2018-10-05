---
title: Обратная совместимость
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- совместимость версий [excel 2007,] XLL совместимости [Excel 2007], обратной совместимости [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e1368ef55b96be947527456e0f01918afec6663
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387974"
---
# <a name="backward-compatibility"></a><span data-ttu-id="cd654-104">Обратная совместимость</span><span class="sxs-lookup"><span data-stu-id="cd654-104">Backward compatibility</span></span>

<span data-ttu-id="cd654-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cd654-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cd654-106">В данной статье рассматриваются вопросы совместимости XLL в различных версиях Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="cd654-106">This topic addresses issues of XLL compatibility in different versions of Microsoft Excel.</span></span>
  
## <a name="useful-constant-definitions"></a><span data-ttu-id="cd654-107">Полезные определения констант</span><span class="sxs-lookup"><span data-stu-id="cd654-107">Useful constant definitions</span></span>

<span data-ttu-id="cd654-108">Рассмотрите возможность включая определения следующего вида в коде проекта XLL и заменить все экземпляры литерала чисел, используемых в данном контексте.</span><span class="sxs-lookup"><span data-stu-id="cd654-108">Consider including definitions similar to these in your XLL project code and replacing all instances of literal numbers used in this context.</span></span> <span data-ttu-id="cd654-109">Это упростит код, версии и снизить вероятность возникновения ошибки, связанные с версии в виде невинные номеров.</span><span class="sxs-lookup"><span data-stu-id="cd654-109">This will clarify code that is version specific, and reduce the likelihood of version-related bugs in the form of innocuous-looking numbers.</span></span>
  
```cpp
#define MAX_XL11_ROWS            65536
#define MAX_XL11_COLS              256
#define MAX_XL12_ROWS          1048576
#define MAX_XL12_COLS            16384
#define MAX_XL11_UDF_ARGS           30
#define MAX_XL12_UDF_ARGS          255
#define MAX_XL4_STR_LEN           255u
#define MAX_XL12_STR_LEN        32767u
```

## <a name="getting-the-running-version"></a><span data-ttu-id="cd654-110">Получение используемой версии</span><span class="sxs-lookup"><span data-stu-id="cd654-110">Getting the running version</span></span>

<span data-ttu-id="cd654-111">Следует определить, какие версии выполняется с помощью `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, где `arg` — это числовой, **XLOPER** значение 2 и версия — это строка **XLOPER** , который затем может быть преобразован в тип integer.</span><span class="sxs-lookup"><span data-stu-id="cd654-111">You should detect which version is running using  `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, where  `arg` is a numeric **XLOPER** set to 2 and version is a string **XLOPER** which can then be coerced to an integer.</span></span> <span data-ttu-id="cd654-112">Для Microsoft Excel 2013 это 15.0.</span><span class="sxs-lookup"><span data-stu-id="cd654-112">For Microsoft Excel 2013, this is 15.0.</span></span> <span data-ttu-id="cd654-113">Это следует сделать в или из функции [xlAutoOpen](xlautoopen.md) .</span><span class="sxs-lookup"><span data-stu-id="cd654-113">You should do this in, or from, the [xlAutoOpen](xlautoopen.md) function.</span></span> <span data-ttu-id="cd654-114">Затем можно задать глобальную переменную, чтобы сообщить всем модулям в проекте, установленной версии Excel.</span><span class="sxs-lookup"><span data-stu-id="cd654-114">You can then set a global variable that informs all of the modules in your project which version of Excel is running.</span></span> <span data-ttu-id="cd654-115">Код затем могут принять решение для вызова интерфейса API для C помощью **Excel12** и **XLOPER12**или с помощью **Excel4** с помощью **XLOPER**s.</span><span class="sxs-lookup"><span data-stu-id="cd654-115">Your code can then decide whether to call the C API using **Excel12** and **XLOPER12**s, or using **Excel4** using **XLOPER**s.</span></span>
  
<span data-ttu-id="cd654-116">Можно вызвать **XLCallVer** для обнаружения версии интерфейса API для C, но это не указывает, какую из версий до Microsoft Excel 2007, выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd654-116">You can call **XLCallVer** to discover the C API version, but this does not indicate which of the pre-Excel 2007 versions you are running.</span></span> 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a><span data-ttu-id="cd654-117">Создание надстроек, экспортировать двух интерфейсов</span><span class="sxs-lookup"><span data-stu-id="cd654-117">Creating add-ins that export dual interfaces</span></span>

<span data-ttu-id="cd654-118">Рассмотрим функцию XLL, который принимает строку и возвращает значение, которое может быть любой из типов данных на листе.</span><span class="sxs-lookup"><span data-stu-id="cd654-118">Consider an XLL function that takes a string and returns a value that can be any of the worksheet data types.</span></span> <span data-ttu-id="cd654-119">Можно экспортировать функции, зарегистрированные как тип «PD» и создания прототипов следующим образом где строка передается как строка байтов со счетчиком длины.</span><span class="sxs-lookup"><span data-stu-id="cd654-119">You could export a function registered as type "PD" and prototyped as follows where the string is passed as a length-counted byte string.</span></span>
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
<span data-ttu-id="cd654-120">Несмотря на то, что это работает нормально, существует несколько причин, почему это не идеальная интерфейса в код, начиная с версии Excel 2007:</span><span class="sxs-lookup"><span data-stu-id="cd654-120">Although this works perfectly well, there are several reasons why this is not the ideal interface to your code starting in Excel 2007:</span></span>
  
- <span data-ttu-id="cd654-121">Он применяются ограничения строки байтов C API и не может получить доступ к длинных Юникод строк поддерживается начиная с версии Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="cd654-121">It is subject to the limitations of C API byte strings and cannot access the long Unicode strings supported starting in Excel 2007.</span></span>
    
- <span data-ttu-id="cd654-122">Хотя начиная с версии Excel 2007, Excel можно передавать и принимать **XLOPER**s, во внутренней сети его преобразует их в **XLOPER12**, поэтому дополнительная нагрузка неявное преобразование, начиная с версии Excel 2007, не существует при выполнении кода в более ранних версиях Excel.</span><span class="sxs-lookup"><span data-stu-id="cd654-122">Although, starting in Excel 2007, Excel can pass and accept **XLOPER**s, internally it converts them to **XLOPER12**s, so there is an implicit conversion overhead starting in Excel 2007 that is not there when the code runs in earlier versions of Excel.</span></span>
    
- <span data-ttu-id="cd654-123">Возможно, что эта функция может сделать потокобезопасными, но если изменить тип строки для `PD$`, происходит ошибка регистрации в до Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="cd654-123">It may be that this function can be made thread safe, but if the type string is changed to  `PD$`, registration fails in starting before Excel 2007.</span></span>
    
<span data-ttu-id="cd654-124">По этим причинам в идеале, начиная с версии Excel 2007 следует экспортировать функцию для пользователей, зарегистрированных в качестве `QD%$`, при условии кода — это поток надежных и создания прототипов следующим образом.</span><span class="sxs-lookup"><span data-stu-id="cd654-124">For these reasons, ideally, starting in Excel 2007 you should export a function for your users that was registered as  `QD%$`, assuming your code is thread safe and prototyped as follows.</span></span>
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
<span data-ttu-id="cd654-125">Другой причиной, почему может потребоваться регистрации различные функции, начиная с версии Excel 2007 — это, что она позволяет функциям XLL принимать до 255 аргументы, а не 30 ограничение в более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="cd654-125">Another reason why you might want to register a different function starting in Excel 2007 is that it permits XLL functions to take up to 255 arguments, instead of the 30 limit of earlier versions.</span></span>
  
<span data-ttu-id="cd654-126">К счастью можно воспользоваться преимуществами обеих версий путем экспорта обеих версий из проекта.</span><span class="sxs-lookup"><span data-stu-id="cd654-126">Fortunately, you can have the benefits of both by exporting both versions from your project.</span></span> <span data-ttu-id="cd654-127">Можно затем определить используемую версию Excel и условно зарегистрировать наиболее подходящую функцию.</span><span class="sxs-lookup"><span data-stu-id="cd654-127">You can then detect the running Excel version and conditionally register the most appropriate function.</span></span> <span data-ttu-id="cd654-128">Дополнительные сведения и пример реализации в разделе [Разработка надстроек (XLL-модулей) в Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).</span><span class="sxs-lookup"><span data-stu-id="cd654-128">For more information and an example implementation, see [Developing Add-ins (XLLs) in Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).</span></span>
  
<span data-ttu-id="cd654-129">Этот подход может привести к тому, что на листе, открытом в Excel 2003 может отображать результаты, отличные от одного листа, выполнение, начиная с версии Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="cd654-129">This approach leads to the possibility that a worksheet running in Excel 2003 could display different results than the same sheet running starting in Excel 2007.</span></span> <span data-ttu-id="cd654-130">К примеру приложение Excel 2003 будет сопоставить строки Юникод в строку в ячейке таблицы Excel 2003 в строку байтов ASCII и усекать перед передачей их в функцию XLL.</span><span class="sxs-lookup"><span data-stu-id="cd654-130">For example, Excel 2003 would map a Unicode string in an Excel 2003 worksheet cell to an ASCII byte-string and truncate it before passing it to an XLL function.</span></span> <span data-ttu-id="cd654-131">Начиная с версии Excel 2007, Excel передает непреобразованных строка Юникода функцию XLL, зарегистрированную надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="cd654-131">Starting in Excel 2007, Excel will pass an unconverted Unicode string to an XLL function registered in the right way.</span></span> <span data-ttu-id="cd654-132">Это может привести к другой результат.</span><span class="sxs-lookup"><span data-stu-id="cd654-132">This could lead to a different result.</span></span> <span data-ttu-id="cd654-133">Следует иметь в виду такой возможности и последствия для пользователей, не только в обновления.</span><span class="sxs-lookup"><span data-stu-id="cd654-133">You should be aware of this possibility and the consequences to your users, not just in the upgrade.</span></span> <span data-ttu-id="cd654-134">Например некоторые числовые функции были улучшены между Excel 2000 и Excel 2003.</span><span class="sxs-lookup"><span data-stu-id="cd654-134">For example, some built-in numeric functions were improved between Excel 2000 and Excel 2003.</span></span>
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a><span data-ttu-id="cd654-135">Новые функции и функции пакета</span><span class="sxs-lookup"><span data-stu-id="cd654-135">New Worksheet functions and Analysis Toolpak functions</span></span>

<span data-ttu-id="cd654-136">Функции ПАКЕТА анализа являются частью Excel, начиная с версии Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="cd654-136">Analysis Toolpak (ATP) functions are part of Excel starting in Excel 2007.</span></span> <span data-ttu-id="cd654-137">Раньше XLL-модуль только может вызывать функцию ATP с помощью [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="cd654-137">Previously, an XLL could only call an ATP function by using [xlUDF](xludf.md).</span></span> <span data-ttu-id="cd654-138">Начиная с версии Excel 2007, функции анализа должен быть вызван с помощью функция перечислений, определенных в xlcall.h.</span><span class="sxs-lookup"><span data-stu-id="cd654-138">Starting in Excel 2007, the ATP functions should be called using the function enumerations defined in xlcall.h.</span></span> <span data-ttu-id="cd654-139">В примере в вызов пользовательских функций из библиотек DLL показано двумя различными способами.</span><span class="sxs-lookup"><span data-stu-id="cd654-139">The example in Calling User-defined Functions from DLLs demonstrates the two different methods.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cd654-140">См. также</span><span class="sxs-lookup"><span data-stu-id="cd654-140">See also</span></span>

- [<span data-ttu-id="cd654-141">Функции обратного вызова API C: Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="cd654-141">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md) 
- [<span data-ttu-id="cd654-142">Программирование с использованием API C в Excel</span><span class="sxs-lookup"><span data-stu-id="cd654-142">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
- [<span data-ttu-id="cd654-143">Новые возможности API C для Excel</span><span class="sxs-lookup"><span data-stu-id="cd654-143">What's New in the C API for Excel</span></span>](what-s-new-in-the-c-api-for-excel.md)

