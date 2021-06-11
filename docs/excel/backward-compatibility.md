---
title: Обратная совместимость
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- совместимость версий [Excel 2007], совместимость XLL [Excel 2007], обратная совместимость [Excel 2007]
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
# <a name="backward-compatibility"></a><span data-ttu-id="9d876-104">Обратная совместимость</span><span class="sxs-lookup"><span data-stu-id="9d876-104">Backward compatibility</span></span>

<span data-ttu-id="9d876-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9d876-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9d876-106">В этом разделе проблемы совместимости XLL в различных версиях Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="9d876-106">This topic addresses issues of XLL compatibility in different versions of Microsoft Excel.</span></span>
  
## <a name="useful-constant-definitions"></a><span data-ttu-id="9d876-107">Полезные определения постоянной</span><span class="sxs-lookup"><span data-stu-id="9d876-107">Useful constant definitions</span></span>

<span data-ttu-id="9d876-108">Рассмотрите возможность включения определений, аналогичных этим, в код проекта XLL и замены всех экземпляров буквальных номеров, используемых в этом контексте.</span><span class="sxs-lookup"><span data-stu-id="9d876-108">Consider including definitions similar to these in your XLL project code and replacing all instances of literal numbers used in this context.</span></span> <span data-ttu-id="9d876-109">Это позволит уточнить конкретный код версии и снизить вероятность ошибок, связанных с версией, в виде безобидных номеров.</span><span class="sxs-lookup"><span data-stu-id="9d876-109">This will clarify code that is version specific, and reduce the likelihood of version-related bugs in the form of innocuous-looking numbers.</span></span>
  
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

## <a name="getting-the-running-version"></a><span data-ttu-id="9d876-110">Получение запущенной версии</span><span class="sxs-lookup"><span data-stu-id="9d876-110">Getting the running version</span></span>

<span data-ttu-id="9d876-111">Вы должны определить, какая версия работает с помощью, где числовой XLOPER набор 2 и версия `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)` `arg` **строки XLOPER,**  которые затем могут быть принуждены к integer.</span><span class="sxs-lookup"><span data-stu-id="9d876-111">You should detect which version is running using  `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, where  `arg` is a numeric **XLOPER** set to 2 and version is a string **XLOPER** which can then be coerced to an integer.</span></span> <span data-ttu-id="9d876-112">Для Microsoft Excel 2013 это 15.0.</span><span class="sxs-lookup"><span data-stu-id="9d876-112">For Microsoft Excel 2013, this is 15.0.</span></span> <span data-ttu-id="9d876-113">Вы должны сделать это в функции [xlAutoOpen](xlautoopen.md) или из нее.</span><span class="sxs-lookup"><span data-stu-id="9d876-113">You should do this in, or from, the [xlAutoOpen](xlautoopen.md) function.</span></span> <span data-ttu-id="9d876-114">Затем можно установить глобальную переменную, которая информирует все модули в проекте, какая Excel запущена.</span><span class="sxs-lookup"><span data-stu-id="9d876-114">You can then set a global variable that informs all of the modules in your project which version of Excel is running.</span></span> <span data-ttu-id="9d876-115">Затем код может решить, вызывать API C с помощью **Excel12** и **XLOPER12** s или использовать **Excel4** с помощью **XLOPER** s.</span><span class="sxs-lookup"><span data-stu-id="9d876-115">Your code can then decide whether to call the C API using **Excel12** and **XLOPER12** s, or using **Excel4** using **XLOPER** s.</span></span>
  
<span data-ttu-id="9d876-116">Вы можете **вызвать XLCallVer,** чтобы узнать версию API C, но это не указывает, какая из Excel 2007 года запущена.</span><span class="sxs-lookup"><span data-stu-id="9d876-116">You can call **XLCallVer** to discover the C API version, but this does not indicate which of the pre-Excel 2007 versions you are running.</span></span> 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a><span data-ttu-id="9d876-117">Создание надстройок, экспортируют двойные интерфейсы</span><span class="sxs-lookup"><span data-stu-id="9d876-117">Creating add-ins that export dual interfaces</span></span>

<span data-ttu-id="9d876-118">Рассмотрим функцию XLL, которая принимает строку и возвращает значение, которое может быть любым из типов данных таблицы.</span><span class="sxs-lookup"><span data-stu-id="9d876-118">Consider an XLL function that takes a string and returns a value that can be any of the worksheet data types.</span></span> <span data-ttu-id="9d876-119">Можно экспортировать функцию, зарегистрированную как тип "PD" и прототипируемую следующим образом, где строка передается в виде строки byte с учетом длины.</span><span class="sxs-lookup"><span data-stu-id="9d876-119">You could export a function registered as type "PD" and prototyped as follows where the string is passed as a length-counted byte string.</span></span>
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
<span data-ttu-id="9d876-120">Хотя это отлично работает, существует несколько причин, по которым это не идеальный интерфейс для кода, начиная с Excel 2007 г.:</span><span class="sxs-lookup"><span data-stu-id="9d876-120">Although this works perfectly well, there are several reasons why this is not the ideal interface to your code starting in Excel 2007:</span></span>
  
- <span data-ttu-id="9d876-121">Он подвержен ограничениям строк byte API C и не может получить доступ к длинным строкам Юникод, поддерживаемым начиная с Excel 2007 года.</span><span class="sxs-lookup"><span data-stu-id="9d876-121">It is subject to the limitations of C API byte strings and cannot access the long Unicode strings supported starting in Excel 2007.</span></span>
    
- <span data-ttu-id="9d876-122">Хотя, начиная с Excel 2007 г., Excel может передавать и принимать **XLOPER** s, внутренне он преобразует их в **XLOPER12** s, поэтому накладные расходы на неявное преобразование, начиная с Excel 2007 г., не существуют, когда код выполняется в более ранних версиях Excel.</span><span class="sxs-lookup"><span data-stu-id="9d876-122">Although, starting in Excel 2007, Excel can pass and accept **XLOPER** s, internally it converts them to **XLOPER12** s, so there is an implicit conversion overhead starting in Excel 2007 that is not there when the code runs in earlier versions of Excel.</span></span>
    
- <span data-ttu-id="9d876-123">Возможно, эта функция может быть безопасной, но если строка типа изменена на, регистрация не будет выполнена до начала Excel `PD$` 2007 года.</span><span class="sxs-lookup"><span data-stu-id="9d876-123">It may be that this function can be made thread safe, but if the type string is changed to  `PD$`, registration fails in starting before Excel 2007.</span></span>
    
<span data-ttu-id="9d876-124">По этим причинам, в идеале, начиная с Excel 2007 г. необходимо экспортировать функцию для пользователей, зарегистрированных в качестве, если ваш код является нитью безопасной и прототипируется следующим `QD%$` образом.</span><span class="sxs-lookup"><span data-stu-id="9d876-124">For these reasons, ideally, starting in Excel 2007 you should export a function for your users that was registered as  `QD%$`, assuming your code is thread safe and prototyped as follows.</span></span>
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
<span data-ttu-id="9d876-125">Еще одна причина, по которой можно зарегистрировать другую функцию, начиная с Excel 2007 г., заключается в том, что она позволяет функциям XLL принимать до 255 аргументов вместо 30 ограничений предыдущих версий.</span><span class="sxs-lookup"><span data-stu-id="9d876-125">Another reason why you might want to register a different function starting in Excel 2007 is that it permits XLL functions to take up to 255 arguments, instead of the 30 limit of earlier versions.</span></span>
  
<span data-ttu-id="9d876-126">К счастью, вы можете использовать преимущества обоих версий, экспортировать обе версии из проекта.</span><span class="sxs-lookup"><span data-stu-id="9d876-126">Fortunately, you can have the benefits of both by exporting both versions from your project.</span></span> <span data-ttu-id="9d876-127">Затем можно обнаружить запущенную Excel и условно зарегистрировать наиболее подходящие функции.</span><span class="sxs-lookup"><span data-stu-id="9d876-127">You can then detect the running Excel version and conditionally register the most appropriate function.</span></span> <span data-ttu-id="9d876-128">Дополнительные сведения и пример реализации см. в [примере Developing Add-ins (XLLs) в Excel 2007 г.](https://msdn.microsoft.com/library/aa730920.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d876-128">For more information and an example implementation, see [Developing Add-ins (XLLs) in Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).</span></span>
  
<span data-ttu-id="9d876-129">Этот подход приводит к тому, что лист, запущенный в 2003 Excel 2003 г., может отображать различные результаты, чем один и тот же лист, запущенный с Excel 2007 г.</span><span class="sxs-lookup"><span data-stu-id="9d876-129">This approach leads to the possibility that a worksheet running in Excel 2003 could display different results than the same sheet running starting in Excel 2007.</span></span> <span data-ttu-id="9d876-130">Например, Excel 2003 г. наметит строку Юникода в ячейке таблицы Excel 2003 г. в строку byte-string ASCII и усечена до передачи ее функции XLL.</span><span class="sxs-lookup"><span data-stu-id="9d876-130">For example, Excel 2003 would map a Unicode string in an Excel 2003 worksheet cell to an ASCII byte-string and truncate it before passing it to an XLL function.</span></span> <span data-ttu-id="9d876-131">Начиная с Excel 2007 Excel будет передавать неконвертированную строку Юникод в функцию XLL, зарегистрированную правильно.</span><span class="sxs-lookup"><span data-stu-id="9d876-131">Starting in Excel 2007, Excel will pass an unconverted Unicode string to an XLL function registered in the right way.</span></span> <span data-ttu-id="9d876-132">Это может привести к иному результату.</span><span class="sxs-lookup"><span data-stu-id="9d876-132">This could lead to a different result.</span></span> <span data-ttu-id="9d876-133">Вы должны знать об этой возможности и последствиях для пользователей, а не только в обновлении.</span><span class="sxs-lookup"><span data-stu-id="9d876-133">You should be aware of this possibility and the consequences to your users, not just in the upgrade.</span></span> <span data-ttu-id="9d876-134">Например, в период с 200 Excel 0 по Excel 2003 г. некоторые встроенные числимые функции были улучшены.</span><span class="sxs-lookup"><span data-stu-id="9d876-134">For example, some built-in numeric functions were improved between Excel 2000 and Excel 2003.</span></span>
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a><span data-ttu-id="9d876-135">Функции нового таблицы и функции toolpak analysis</span><span class="sxs-lookup"><span data-stu-id="9d876-135">New Worksheet functions and Analysis Toolpak functions</span></span>

<span data-ttu-id="9d876-136">Функции Toolpak analysis (ATP) являются частью Excel начиная с Excel 2007 г.</span><span class="sxs-lookup"><span data-stu-id="9d876-136">Analysis Toolpak (ATP) functions are part of Excel starting in Excel 2007.</span></span> <span data-ttu-id="9d876-137">Ранее XLL мог вызывать функцию ATP только с помощью [xlUDF.](xludf.md)</span><span class="sxs-lookup"><span data-stu-id="9d876-137">Previously, an XLL could only call an ATP function by using [xlUDF](xludf.md).</span></span> <span data-ttu-id="9d876-138">Начиная с Excel 2007 г. функции ATP должны называться с помощью функций, определяемой в xlcall.h.</span><span class="sxs-lookup"><span data-stu-id="9d876-138">Starting in Excel 2007, the ATP functions should be called using the function enumerations defined in xlcall.h.</span></span> <span data-ttu-id="9d876-139">В примере "Вызов функций, определенных пользователем" из DLLs, демонстрируются два различных метода.</span><span class="sxs-lookup"><span data-stu-id="9d876-139">The example in Calling User-defined Functions from DLLs demonstrates the two different methods.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9d876-140">См. также</span><span class="sxs-lookup"><span data-stu-id="9d876-140">See also</span></span>

- [<span data-ttu-id="9d876-141">Функции обратного вызова API C: Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="9d876-141">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md) 
- [<span data-ttu-id="9d876-142">Программирование с использованием API C в Excel</span><span class="sxs-lookup"><span data-stu-id="9d876-142">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
- [<span data-ttu-id="9d876-143">Новые возможности API C для Excel</span><span class="sxs-lookup"><span data-stu-id="9d876-143">What's New in the C API for Excel</span></span>](what-s-new-in-the-c-api-for-excel.md)

