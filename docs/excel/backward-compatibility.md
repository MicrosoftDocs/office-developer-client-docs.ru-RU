---
title: Обратная совместимость
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- совместимость версий [excel 2007],совместимость XLL [Excel 2007],обратная совместимость [Excel 2007]
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e1368ef55b96be947527456e0f01918afec6663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301682"
---
# <a name="backward-compatibility"></a><span data-ttu-id="3756a-104">Обратная совместимость</span><span class="sxs-lookup"><span data-stu-id="3756a-104">Backward compatibility</span></span>

<span data-ttu-id="3756a-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3756a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3756a-106">В этом разделе исправлены проблемы совместимости XLL в различных версиях Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="3756a-106">This topic addresses issues of XLL compatibility in different versions of Microsoft Excel.</span></span>
  
## <a name="useful-constant-definitions"></a><span data-ttu-id="3756a-107">Полезные определения констант</span><span class="sxs-lookup"><span data-stu-id="3756a-107">Useful constant definitions</span></span>

<span data-ttu-id="3756a-108">Рассмотрите возможность включите определения, похожие на эти, в код проекта XLL и замените все экземпляры литеральных чисел, используемых в этом контексте.</span><span class="sxs-lookup"><span data-stu-id="3756a-108">Consider including definitions similar to these in your XLL project code and replacing all instances of literal numbers used in this context.</span></span> <span data-ttu-id="3756a-109">Это уточнение кода, относящемся к конкретной версии, и снижение вероятности ошибок, связанных с версиями, в виде неявных номеров.</span><span class="sxs-lookup"><span data-stu-id="3756a-109">This will clarify code that is version specific, and reduce the likelihood of version-related bugs in the form of innocuous-looking numbers.</span></span>
  
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

## <a name="getting-the-running-version"></a><span data-ttu-id="3756a-110">Получение запущенной версии</span><span class="sxs-lookup"><span data-stu-id="3756a-110">Getting the running version</span></span>

<span data-ttu-id="3756a-111">Необходимо определить, какая версия запущена с помощью , где числовой XLOPER задайте 2, а версия — строку `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)` `arg` **XLOPER,**  которую затем можно привести к числу.</span><span class="sxs-lookup"><span data-stu-id="3756a-111">You should detect which version is running using  `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, where  `arg` is a numeric **XLOPER** set to 2 and version is a string **XLOPER** which can then be coerced to an integer.</span></span> <span data-ttu-id="3756a-112">Для Microsoft Excel 2013 это 15.0.</span><span class="sxs-lookup"><span data-stu-id="3756a-112">For Microsoft Excel 2013, this is 15.0.</span></span> <span data-ttu-id="3756a-113">Это следует сделать в функции [xlAutoOpen](xlautoopen.md) или из нее.</span><span class="sxs-lookup"><span data-stu-id="3756a-113">You should do this in, or from, the [xlAutoOpen](xlautoopen.md) function.</span></span> <span data-ttu-id="3756a-114">Затем можно установить глобальную переменную, которая сообщает всем модулям в проекте, какая версия Excel запущена.</span><span class="sxs-lookup"><span data-stu-id="3756a-114">You can then set a global variable that informs all of the modules in your project which version of Excel is running.</span></span> <span data-ttu-id="3756a-115">Затем код может решить, следует ли вызывать API C с помощью **Excel12** и **XLOPER12** или **Excel4** с помощью **XLOPER.**</span><span class="sxs-lookup"><span data-stu-id="3756a-115">Your code can then decide whether to call the C API using **Excel12** and **XLOPER12** s, or using **Excel4** using **XLOPER** s.</span></span>
  
<span data-ttu-id="3756a-116">Вы можете вызвать **XLCallVer,** чтобы обнаружить версию API C, но это не указывает, какая из запущенных версий до Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="3756a-116">You can call **XLCallVer** to discover the C API version, but this does not indicate which of the pre-Excel 2007 versions you are running.</span></span> 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a><span data-ttu-id="3756a-117">Создание надстройки, экспортируют два интерфейса</span><span class="sxs-lookup"><span data-stu-id="3756a-117">Creating add-ins that export dual interfaces</span></span>

<span data-ttu-id="3756a-118">Рассмотрим функцию XLL, которая принимает строку и возвращает значение, которое может быть любым из типов данных таблицы.</span><span class="sxs-lookup"><span data-stu-id="3756a-118">Consider an XLL function that takes a string and returns a value that can be any of the worksheet data types.</span></span> <span data-ttu-id="3756a-119">Можно экспортировать функцию, зарегистрированную как тип "PD" и прототипируемую следующим образом, где строка передается в виде строки с подсчетом длины.</span><span class="sxs-lookup"><span data-stu-id="3756a-119">You could export a function registered as type "PD" and prototyped as follows where the string is passed as a length-counted byte string.</span></span>
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
<span data-ttu-id="3756a-120">Хотя это хорошо работает, существует несколько причин, по которым этот интерфейс не является идеальным интерфейсом для кода, начиная с Excel 2007:</span><span class="sxs-lookup"><span data-stu-id="3756a-120">Although this works perfectly well, there are several reasons why this is not the ideal interface to your code starting in Excel 2007:</span></span>
  
- <span data-ttu-id="3756a-121">На него накладываются ограничения на строки byte C API, и он не может получить доступ к длинным строкам Юникода, поддерживаемых начиная с Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="3756a-121">It is subject to the limitations of C API byte strings and cannot access the long Unicode strings supported starting in Excel 2007.</span></span>
    
- <span data-ttu-id="3756a-122">Хотя, начиная с Excel 2007, Excel может передавать и принимать **S XLOPER,** внутренне преобразует их в **XLOPER12,** поэтому, начиная с Excel 2007, существует неявная накладная часть преобразования, которая не существует, когда код выполняется в предыдущих версиях Excel.</span><span class="sxs-lookup"><span data-stu-id="3756a-122">Although, starting in Excel 2007, Excel can pass and accept **XLOPER** s, internally it converts them to **XLOPER12** s, so there is an implicit conversion overhead starting in Excel 2007 that is not there when the code runs in earlier versions of Excel.</span></span>
    
- <span data-ttu-id="3756a-123">Возможно, эту функцию можно сделать потокобезопасной, но если строка типа изменена на , регистрация не будет выполнена, начиная  `PD$` с Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="3756a-123">It may be that this function can be made thread safe, but if the type string is changed to  `PD$`, registration fails in starting before Excel 2007.</span></span>
    
<span data-ttu-id="3756a-124">По этим причинам в идеале, начиная с Excel 2007, следует экспортировать функцию для пользователей, зарегистрированных как , предполагая, что ваш код потокобезопасн и прототипов, как поется в  `QD%$` примере.</span><span class="sxs-lookup"><span data-stu-id="3756a-124">For these reasons, ideally, starting in Excel 2007 you should export a function for your users that was registered as  `QD%$`, assuming your code is thread safe and prototyped as follows.</span></span>
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
<span data-ttu-id="3756a-125">Еще одна причина, по которой можно зарегистрировать другую функцию, начиная с Excel 2007, заключается в том, что она позволяет функциям XLL принимать до 255 аргументов вместо 30 ограничений более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="3756a-125">Another reason why you might want to register a different function starting in Excel 2007 is that it permits XLL functions to take up to 255 arguments, instead of the 30 limit of earlier versions.</span></span>
  
<span data-ttu-id="3756a-126">К счастью, вы можете получить преимущества обеих версий, экспортив обе версии из проекта.</span><span class="sxs-lookup"><span data-stu-id="3756a-126">Fortunately, you can have the benefits of both by exporting both versions from your project.</span></span> <span data-ttu-id="3756a-127">Затем можно определить запущенную версию Excel и условно зарегистрировать наиболее подместимую функцию.</span><span class="sxs-lookup"><span data-stu-id="3756a-127">You can then detect the running Excel version and conditionally register the most appropriate function.</span></span> <span data-ttu-id="3756a-128">Дополнительные сведения и пример внедрения см. в примере разработки надстроек [(XLL) в Excel 2007.](https://msdn.microsoft.com/library/aa730920.aspx)</span><span class="sxs-lookup"><span data-stu-id="3756a-128">For more information and an example implementation, see [Developing Add-ins (XLLs) in Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).</span></span>
  
<span data-ttu-id="3756a-129">Такой подход приводит к тому, что на листе, запущенном в Excel 2003, могут отображаться результаты, отличае от результатов, запущенных на одном листе, начиная с Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="3756a-129">This approach leads to the possibility that a worksheet running in Excel 2003 could display different results than the same sheet running starting in Excel 2007.</span></span> <span data-ttu-id="3756a-130">Например, Excel 2003 соединит строку Юникода в ячейке листа Excel 2003 со строкой byte-string ASCII и усекает ее перед передачей в функцию XLL.</span><span class="sxs-lookup"><span data-stu-id="3756a-130">For example, Excel 2003 would map a Unicode string in an Excel 2003 worksheet cell to an ASCII byte-string and truncate it before passing it to an XLL function.</span></span> <span data-ttu-id="3756a-131">Начиная с Excel 2007, Excel передает невербированную строку Юникода функции XLL, зарегистрированной правильным способом.</span><span class="sxs-lookup"><span data-stu-id="3756a-131">Starting in Excel 2007, Excel will pass an unconverted Unicode string to an XLL function registered in the right way.</span></span> <span data-ttu-id="3756a-132">Это может привести к другому результату.</span><span class="sxs-lookup"><span data-stu-id="3756a-132">This could lead to a different result.</span></span> <span data-ttu-id="3756a-133">Следует помнить об этой возможности и последствиях для пользователей, а не только при обновлении.</span><span class="sxs-lookup"><span data-stu-id="3756a-133">You should be aware of this possibility and the consequences to your users, not just in the upgrade.</span></span> <span data-ttu-id="3756a-134">Например, в Excel 2000 и Excel 2003 улучшены некоторые встроенные числимые функции.</span><span class="sxs-lookup"><span data-stu-id="3756a-134">For example, some built-in numeric functions were improved between Excel 2000 and Excel 2003.</span></span>
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a><span data-ttu-id="3756a-135">Новые функции worksheet и analysis Toolpak</span><span class="sxs-lookup"><span data-stu-id="3756a-135">New Worksheet functions and Analysis Toolpak functions</span></span>

<span data-ttu-id="3756a-136">Функции анализа toolpak (ATP) являются частью Excel, начиная с Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="3756a-136">Analysis Toolpak (ATP) functions are part of Excel starting in Excel 2007.</span></span> <span data-ttu-id="3756a-137">Ранее XLL могла вызывать функцию ATP только с помощью [xlUDF.](xludf.md)</span><span class="sxs-lookup"><span data-stu-id="3756a-137">Previously, an XLL could only call an ATP function by using [xlUDF](xludf.md).</span></span> <span data-ttu-id="3756a-138">Начиная с Excel 2007, функции ATP должны быть вызваны с помощью функций, которые определены в xlcall.h.</span><span class="sxs-lookup"><span data-stu-id="3756a-138">Starting in Excel 2007, the ATP functions should be called using the function enumerations defined in xlcall.h.</span></span> <span data-ttu-id="3756a-139">В примере вызова пользовательских функций из DLL демонстрируются два разных метода.</span><span class="sxs-lookup"><span data-stu-id="3756a-139">The example in Calling User-defined Functions from DLLs demonstrates the two different methods.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3756a-140">См. также</span><span class="sxs-lookup"><span data-stu-id="3756a-140">See also</span></span>

- [<span data-ttu-id="3756a-141">Функции обратного вызова API C: Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="3756a-141">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md) 
- [<span data-ttu-id="3756a-142">Программирование с использованием API C в Excel</span><span class="sxs-lookup"><span data-stu-id="3756a-142">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
- [<span data-ttu-id="3756a-143">Новые возможности API C для Excel</span><span class="sxs-lookup"><span data-stu-id="3756a-143">What's New in the C API for Excel</span></span>](what-s-new-in-the-c-api-for-excel.md)

