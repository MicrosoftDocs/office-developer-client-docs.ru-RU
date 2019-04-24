---
title: Обратная совместимость
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Совместимость версий [Excel 2007], совместимость XLL [Excel 2007], обратная совместимость [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e1368ef55b96be947527456e0f01918afec6663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301682"
---
# <a name="backward-compatibility"></a><span data-ttu-id="314d4-104">Обратная совместимость</span><span class="sxs-lookup"><span data-stu-id="314d4-104">Backward compatibility</span></span>

<span data-ttu-id="314d4-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="314d4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="314d4-106">В этой статье рассматриваются проблемы совместимости XLL в различных версиях Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="314d4-106">This topic addresses issues of XLL compatibility in different versions of Microsoft Excel.</span></span>
  
## <a name="useful-constant-definitions"></a><span data-ttu-id="314d4-107">Применимые определения констант</span><span class="sxs-lookup"><span data-stu-id="314d4-107">Useful constant definitions</span></span>

<span data-ttu-id="314d4-108">РасСмотрите возможность включения определений, похожих на эти, в коде проекта XLL и замену всех экземпляров литеральных чисел, используемых в этом контексте.</span><span class="sxs-lookup"><span data-stu-id="314d4-108">Consider including definitions similar to these in your XLL project code and replacing all instances of literal numbers used in this context.</span></span> <span data-ttu-id="314d4-109">Это приводит к уточнению кода, относящегося к версии, и уменьшению вероятности ошибок, связанных с версиями, в форме безвредных номеров.</span><span class="sxs-lookup"><span data-stu-id="314d4-109">This will clarify code that is version specific, and reduce the likelihood of version-related bugs in the form of innocuous-looking numbers.</span></span>
  
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

## <a name="getting-the-running-version"></a><span data-ttu-id="314d4-110">Извлечение запущенной версии</span><span class="sxs-lookup"><span data-stu-id="314d4-110">Getting the running version</span></span>

<span data-ttu-id="314d4-111">Необходимо определить, какая версия выполняется с помощью `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, где `arg` в качестве числового параметра **XLOPER** задано значение 2, а версия — это строка **XLOPER** , которую затем можно привести к целому числу.</span><span class="sxs-lookup"><span data-stu-id="314d4-111">You should detect which version is running using  `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, where  `arg` is a numeric **XLOPER** set to 2 and version is a string **XLOPER** which can then be coerced to an integer.</span></span> <span data-ttu-id="314d4-112">Для Microsoft Excel 2013 это 15,0.</span><span class="sxs-lookup"><span data-stu-id="314d4-112">For Microsoft Excel 2013, this is 15.0.</span></span> <span data-ttu-id="314d4-113">Это следует сделать в функции [xlAutoOpen](xlautoopen.md) .</span><span class="sxs-lookup"><span data-stu-id="314d4-113">You should do this in, or from, the [xlAutoOpen](xlautoopen.md) function.</span></span> <span data-ttu-id="314d4-114">Затем можно задать глобальную переменную, которая информирует все модули в проекте, какая версия Excel работает.</span><span class="sxs-lookup"><span data-stu-id="314d4-114">You can then set a global variable that informs all of the modules in your project which version of Excel is running.</span></span> <span data-ttu-id="314d4-115">В коде можно решить, следует ли вызывать API C с помощью **Excel12** и **XLOPER12**, или с помощью **Excel4** с помощью **XLOPER**s.</span><span class="sxs-lookup"><span data-stu-id="314d4-115">Your code can then decide whether to call the C API using **Excel12** and **XLOPER12**s, or using **Excel4** using **XLOPER**s.</span></span>
  
<span data-ttu-id="314d4-116">Вы можете вызвать **XLCallVer** для обнаружения версии C API, но это не указывает, какие версии пред-Excel 2007 вы используете.</span><span class="sxs-lookup"><span data-stu-id="314d4-116">You can call **XLCallVer** to discover the C API version, but this does not indicate which of the pre-Excel 2007 versions you are running.</span></span> 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a><span data-ttu-id="314d4-117">Создание надстроек, экспортирующих сдвоенные интерфейсы</span><span class="sxs-lookup"><span data-stu-id="314d4-117">Creating add-ins that export dual interfaces</span></span>

<span data-ttu-id="314d4-118">Рассмотрим функцию XLL, которая принимает строку и возвращает значение, которое может быть любым типом данных листа.</span><span class="sxs-lookup"><span data-stu-id="314d4-118">Consider an XLL function that takes a string and returns a value that can be any of the worksheet data types.</span></span> <span data-ttu-id="314d4-119">Вы можете экспортировать функцию, зарегистрированную как тип "PD", и создать прототип, как показано ниже, где строка передается как строка байтов с ограничением длины.</span><span class="sxs-lookup"><span data-stu-id="314d4-119">You could export a function registered as type "PD" and prototyped as follows where the string is passed as a length-counted byte string.</span></span>
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
<span data-ttu-id="314d4-120">Несмотря на то, что это прекрасно работает, существует несколько причин, по которым это не идеальный интерфейс для кода, начиная с Excel 2007:</span><span class="sxs-lookup"><span data-stu-id="314d4-120">Although this works perfectly well, there are several reasons why this is not the ideal interface to your code starting in Excel 2007:</span></span>
  
- <span data-ttu-id="314d4-121">Он подчиняется ограничениям для строк байтов API C и не может получить доступ к длинным строкам Юникода, поддерживаемым начиная с Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="314d4-121">It is subject to the limitations of C API byte strings and cannot access the long Unicode strings supported starting in Excel 2007.</span></span>
    
- <span data-ttu-id="314d4-122">В то же время, начиная с Excel 2007, Excel может передавать и принимать **XLOPER**s, внутренним образом преобразует их в **XLOPER12**s, поэтому существуют неявные неявные преобразования, начиная с версии Excel 2007, которые не отображаются при выполнении кода в более ранних версиях Excel.</span><span class="sxs-lookup"><span data-stu-id="314d4-122">Although, starting in Excel 2007, Excel can pass and accept **XLOPER**s, internally it converts them to **XLOPER12**s, so there is an implicit conversion overhead starting in Excel 2007 that is not there when the code runs in earlier versions of Excel.</span></span>
    
- <span data-ttu-id="314d4-123">Возможно, эта функция может быть совершена потокобезопасным, но если строка типа изменяется на, то регистрация завершается с `PD$`ошибкой до Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="314d4-123">It may be that this function can be made thread safe, but if the type string is changed to  `PD$`, registration fails in starting before Excel 2007.</span></span>
    
<span data-ttu-id="314d4-124">По этим причинам в идеале, начиная с Excel 2007, необходимо экспортировать функцию для пользователей, зарегистрированных как `QD%$`, предполагая, что код является потокобезопасным и имеет прототип, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="314d4-124">For these reasons, ideally, starting in Excel 2007 you should export a function for your users that was registered as  `QD%$`, assuming your code is thread safe and prototyped as follows.</span></span>
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
<span data-ttu-id="314d4-125">Другая причина, по которой вы можете зарегистрировать другую функцию, начинающуюся в Excel 2007, заключается в том, что она позволяет функциям XLL принимать до 255 аргументов, а не 30 символов более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="314d4-125">Another reason why you might want to register a different function starting in Excel 2007 is that it permits XLL functions to take up to 255 arguments, instead of the 30 limit of earlier versions.</span></span>
  
<span data-ttu-id="314d4-126">К счастью, вы можете использовать преимущества обоих вариантов, экспортировав обе версии из проекта.</span><span class="sxs-lookup"><span data-stu-id="314d4-126">Fortunately, you can have the benefits of both by exporting both versions from your project.</span></span> <span data-ttu-id="314d4-127">Затем вы можете определить запущенную версию Excel и условно зарегистрировать наиболее подходящую функцию.</span><span class="sxs-lookup"><span data-stu-id="314d4-127">You can then detect the running Excel version and conditionally register the most appropriate function.</span></span> <span data-ttu-id="314d4-128">Для получения дополнительных сведений и примера реализации, ознакомьтесь со статьей [Разработка надстроек (XLL) в Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).</span><span class="sxs-lookup"><span data-stu-id="314d4-128">For more information and an example implementation, see [Developing Add-ins (XLLs) in Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).</span></span>
  
<span data-ttu-id="314d4-129">Такой подход приводит к тому, что лист, работающий в Excel 2003, может отображать результаты, не превышающие тот же лист, запущенный в Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="314d4-129">This approach leads to the possibility that a worksheet running in Excel 2003 could display different results than the same sheet running starting in Excel 2007.</span></span> <span data-ttu-id="314d4-130">Например, Excel 2003 будет сопоставлять строку Юникода в ячейке листа Excel 2003 с байтовым строкой ASCII и сокращать ее перед передачей в функцию XLL.</span><span class="sxs-lookup"><span data-stu-id="314d4-130">For example, Excel 2003 would map a Unicode string in an Excel 2003 worksheet cell to an ASCII byte-string and truncate it before passing it to an XLL function.</span></span> <span data-ttu-id="314d4-131">Начиная с Excel 2007, Excel передает непреобразованную строку Юникода в функцию XLL, зарегистрированную в правильном виде.</span><span class="sxs-lookup"><span data-stu-id="314d4-131">Starting in Excel 2007, Excel will pass an unconverted Unicode string to an XLL function registered in the right way.</span></span> <span data-ttu-id="314d4-132">Это может привести к другому результату.</span><span class="sxs-lookup"><span data-stu-id="314d4-132">This could lead to a different result.</span></span> <span data-ttu-id="314d4-133">Вы должны знать о такой возможности и последствиях для пользователей, а не только при обновлении.</span><span class="sxs-lookup"><span data-stu-id="314d4-133">You should be aware of this possibility and the consequences to your users, not just in the upgrade.</span></span> <span data-ttu-id="314d4-134">Например, некоторые встроенные числовые функции были улучшены в Excel 2000 и Excel 2003.</span><span class="sxs-lookup"><span data-stu-id="314d4-134">For example, some built-in numeric functions were improved between Excel 2000 and Excel 2003.</span></span>
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a><span data-ttu-id="314d4-135">Новые функции листов и функции пакета анализа</span><span class="sxs-lookup"><span data-stu-id="314d4-135">New Worksheet functions and Analysis Toolpak functions</span></span>

<span data-ttu-id="314d4-136">Функции пакета анализа (ATP) являются частью Excel, начиная с Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="314d4-136">Analysis Toolpak (ATP) functions are part of Excel starting in Excel 2007.</span></span> <span data-ttu-id="314d4-137">Ранее XLL мог вызвать функцию ATP только с помощью [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="314d4-137">Previously, an XLL could only call an ATP function by using [xlUDF](xludf.md).</span></span> <span data-ttu-id="314d4-138">Начиная с Excel 2007, функции ATP должны вызываться с помощью перечислений функций, определенных в Xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="314d4-138">Starting in Excel 2007, the ATP functions should be called using the function enumerations defined in xlcall.h.</span></span> <span data-ttu-id="314d4-139">В примере вызовов пользовательских функций из библиотек DLL показаны два разных метода.</span><span class="sxs-lookup"><span data-stu-id="314d4-139">The example in Calling User-defined Functions from DLLs demonstrates the two different methods.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="314d4-140">См. также</span><span class="sxs-lookup"><span data-stu-id="314d4-140">See also</span></span>

- [<span data-ttu-id="314d4-141">Функции обратного вызова API C: Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="314d4-141">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md) 
- [<span data-ttu-id="314d4-142">Программирование с использованием API C в Excel</span><span class="sxs-lookup"><span data-stu-id="314d4-142">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
- [<span data-ttu-id="314d4-143">Новые возможности API C для Excel</span><span class="sxs-lookup"><span data-stu-id="314d4-143">What's New in the C API for Excel</span></span>](what-s-new-in-the-c-api-for-excel.md)

