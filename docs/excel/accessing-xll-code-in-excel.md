---
title: Доступ к коду XLL в Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- доступ к коду xll [excel 2007], XLL [Excel 2007], доступ к коду, команды [Excel 2007], регистрация, функции [Excel 2007], регистрация, вызов XLL из Excel, регистрация команд [Excel 2007], регистрация функций [Excel 2007]
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d1332b0dffc052404c75c4ec51d94879457c3da0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705283"
---
# <a name="accessing-xll-code-in-excel"></a><span data-ttu-id="ad9fb-104">Доступ к коду XLL в Excel</span><span class="sxs-lookup"><span data-stu-id="ad9fb-104">Accessing XLL code in Excel</span></span>

<span data-ttu-id="ad9fb-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ad9fb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ad9fb-106">Чтобы функции и команды, которые содержит код XLL, были доступны в Microsoft Excel, они:</span><span class="sxs-lookup"><span data-stu-id="ad9fb-106">To be accessible in Microsoft Excel, the functions and commands that an XLL contains:</span></span>
  
- <span data-ttu-id="ad9fb-107">должны быть экспортированы XLL;</span><span class="sxs-lookup"><span data-stu-id="ad9fb-107">Must be exported by the XLL.</span></span>
    
- <span data-ttu-id="ad9fb-108">должны быть зарегистрированы в Excel.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-108">Must be registered with Excel.</span></span>
    
## <a name="registering-functions-and-commands-with-excel"></a><span data-ttu-id="ad9fb-109">Регистрация функций и команд в Excel</span><span class="sxs-lookup"><span data-stu-id="ad9fb-109">Registering functions and commands with Excel</span></span>

<span data-ttu-id="ad9fb-110">Регистрация указывает Excel о точке входа DLL следующее:</span><span class="sxs-lookup"><span data-stu-id="ad9fb-110">Registration tells Excel the following about a DLL entry point:</span></span>
  
- <span data-ttu-id="ad9fb-111">является ли она скрытой или, если речь идет о функции, будет ли она отображаться в "Мастере функций";</span><span class="sxs-lookup"><span data-stu-id="ad9fb-111">Whether it is hidden or, if a function, whether it is visible in the Function Wizard.</span></span>
    
- <span data-ttu-id="ad9fb-112">можно ли будет ее вызвать только из листа макроса XLM или также из рабочего листа;</span><span class="sxs-lookup"><span data-stu-id="ad9fb-112">Whether it is callable only from an XLM macro sheet, or also from a worksheet.</span></span>
    
- <span data-ttu-id="ad9fb-113">если это команда, является ли она функцией рабочего листа или эквивалентной функцией листа макроса;</span><span class="sxs-lookup"><span data-stu-id="ad9fb-113">If a command, whether it is a worksheet function or a macro sheet equivalent function.</span></span>
    
- <span data-ttu-id="ad9fb-114">каким будет ее имя в операции экспорта XLL/DLL и какое имя следует использовать в Excel.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-114">What its XLL/DLL export name is, and what name you want Excel to use.</span></span>
    
- <span data-ttu-id="ad9fb-115">Если это функция:</span><span class="sxs-lookup"><span data-stu-id="ad9fb-115">If it is a function:</span></span>
    
  - <span data-ttu-id="ad9fb-116">какие типы данных она возвращает и принимает в качестве аргументов;</span><span class="sxs-lookup"><span data-stu-id="ad9fb-116">What data types it returns and takes as arguments.</span></span>
    
  - <span data-ttu-id="ad9fb-117">будет ли она возвращать свой результат, изменяя аргумент на месте;</span><span class="sxs-lookup"><span data-stu-id="ad9fb-117">Whether it returns its result by modifying an argument in place.</span></span>
    
  - <span data-ttu-id="ad9fb-118">является ли она постоянной;</span><span class="sxs-lookup"><span data-stu-id="ad9fb-118">Whether it is volatile.</span></span>
    
  - <span data-ttu-id="ad9fb-119">является ли она потокобезопасной (поддерживается начиная с Excel 2007);</span><span class="sxs-lookup"><span data-stu-id="ad9fb-119">Whether it is thread safe (supported starting in Excel 2007).</span></span>
    
  - <span data-ttu-id="ad9fb-120">какой текст "Мастер вставки функций" и редактор "Автозаполнение" должны отображать для поддержки при вызове функции;</span><span class="sxs-lookup"><span data-stu-id="ad9fb-120">What text the Paste Function Wizard and AutoComplete editor should display to help with calling the function.</span></span>
    
  - <span data-ttu-id="ad9fb-121">в какой категории функций они должна приводиться.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-121">Which function category it should be listed under.</span></span>
    
<span data-ttu-id="ad9fb-122">Все это реализуется с помощью функции C API [xlfRegister](xlfregister-form-1.md), эквивалентной функции XLM **REGISTER**.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-122">This is all achieved using the C API function [xlfRegister](xlfregister-form-1.md), equivalent to the XLM function **REGISTER**.</span></span>
  
## <a name="calling-xll-functions-directly-from-excel"></a><span data-ttu-id="ad9fb-123">Вызов функций XLL непосредственно из Excel</span><span class="sxs-lookup"><span data-stu-id="ad9fb-123">Calling XLL functions directly from Excel</span></span>

<span data-ttu-id="ad9fb-124">После регистрации функции листа макроса и рабочего листа XLL можно вызывать из любого расположения, откуда можно вызвать встроенную функцию:</span><span class="sxs-lookup"><span data-stu-id="ad9fb-124">Once they are registered, XLL worksheet and macro sheet functions can be called from anywhere a built-in function can be called from:</span></span>
  
- <span data-ttu-id="ad9fb-125">формулы массива или одной ячейки на рабочем листе;</span><span class="sxs-lookup"><span data-stu-id="ad9fb-125">A single-cell or array formula on a worksheet.</span></span>
    
- <span data-ttu-id="ad9fb-126">формулы массива или одной ячейки на листе макроса;</span><span class="sxs-lookup"><span data-stu-id="ad9fb-126">A single-cell or array formula on a macro sheet.</span></span>
    
- <span data-ttu-id="ad9fb-127">определения определенного имени;</span><span class="sxs-lookup"><span data-stu-id="ad9fb-127">The definition of a defined name.</span></span>
    
- <span data-ttu-id="ad9fb-128">полей условий и ограничений в диалоговом окне условного форматирования;</span><span class="sxs-lookup"><span data-stu-id="ad9fb-128">The condition and limit fields in a conditional format dialog box.</span></span>
    
- <span data-ttu-id="ad9fb-129">из других надстроек через функцию C API [xlUDF](xludf.md);</span><span class="sxs-lookup"><span data-stu-id="ad9fb-129">From another add-in via the C API function [xlUDF](xludf.md).</span></span>
    
- <span data-ttu-id="ad9fb-130">из Visual Basic для приложений (VBA) через метод **Application.Run**.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-130">From Visual Basic for Applications (VBA) via the **Application.Run** method.</span></span> 
    
<span data-ttu-id="ad9fb-131">Можно получить ссылку на ячейку или диапазон ячеек вызова в нужной функции с помощью функции C API **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-131">You can obtain a reference to the calling cell or range of cells within your function using the C API function **xlfCaller**.</span></span> <span data-ttu-id="ad9fb-132">Если функция вызывалась из выражения условного форматирования ячейки, все равно возвращается ссылка на связанную ячейку или несколько ячеек, поэтому нельзя предположить, что формула с ячейкой содержит функцию XLL.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-132">If the function was called from the cell's conditional format expression, you are still returned a reference to the associated cell or cells, so you cannot assume that the cell's formula contains the XLL function.</span></span> <span data-ttu-id="ad9fb-133">Если функция вызывалась из пользовательской функции VBA (UDF), **xlfCaller** снова возвращает адрес ячеек, которые вызывали функцию VBA.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-133">If your function was called from a VBA user-defined function (UDF), **xlfCaller** again returns the address of the cells that called the VBA function.</span></span> <span data-ttu-id="ad9fb-134">Дополнительные сведения см. в статье [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="ad9fb-134">For more information, see [](xlfcaller.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="ad9fb-135">Excel также вызывает код функции XLL из диалоговых окон **Мастер вставки функции** и **Замена**.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-135">Excel also calls XLL function code from the **Paste Function Wizard** and **Replace** dialog boxes.</span></span> <span data-ttu-id="ad9fb-136">Может потребоваться ограничить обычное выполнение вашего кода в случае диалогового окна **Вставка аргументов функции**, особенно в тех случаях, когда выполнение функции может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-136">You might need to restrict your code's normal running in the case of the **Paste Function Arguments** dialog box, especially where your function can take a long time to execute.</span></span> <span data-ttu-id="ad9fb-137">Чтобы обнаружить, вызывается ли функция из одного из таких диалоговых окон, вам необходимо реализовать определенный код в вашем проекте, который будет просматривать все открытые окна, чтобы определить является ли окно переднего плана одним из таких диалоговых окон, и, если да, какое именно.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-137">To detect if your function is being called from either of these dialog boxes, you must implement some code in your project that iterates through all the open windows to determine if the front window is one of these dialog boxes, and, if so, which one.</span></span> 
  
## <a name="calling-xll-commands-directly-from-excel"></a><span data-ttu-id="ad9fb-138">Вызов команд XLL непосредственно из Excel</span><span class="sxs-lookup"><span data-stu-id="ad9fb-138">Calling DLL commands directly from Excel</span></span>

<span data-ttu-id="ad9fb-139">После регистрации команды XLL можно вызывать всеми способами, которыми можно вызвать другие пользовательские макросы:</span><span class="sxs-lookup"><span data-stu-id="ad9fb-139">Once they are registered, XLL commands can be called in all the ways that other user-defined macros can be called:</span></span>
  
- <span data-ttu-id="ad9fb-140">посредством связывания с объектом элемента управления, встроенным в рабочий лист;</span><span class="sxs-lookup"><span data-stu-id="ad9fb-140">By being associated with a control object embedded on a worksheet.</span></span>
    
- <span data-ttu-id="ad9fb-141">из диалогового окна "Выполнить макрос";</span><span class="sxs-lookup"><span data-stu-id="ad9fb-141">From the Run Macro dialog box.</span></span>
    
- <span data-ttu-id="ad9fb-142">из пользовательского макроса VBA с использованием метода **Application.Run**;</span><span class="sxs-lookup"><span data-stu-id="ad9fb-142">From a VBA user-defined macro using the **Application.Run** method.</span></span> 
    
- <span data-ttu-id="ad9fb-143">из настраиваемого элемента меню или панели инструментов;</span><span class="sxs-lookup"><span data-stu-id="ad9fb-143">From a customized menu item or toolbar.</span></span>
    
- <span data-ttu-id="ad9fb-144">с помощью сочетаний клавиш, заданных при регистрации команды;</span><span class="sxs-lookup"><span data-stu-id="ad9fb-144">Using a shortcut keystroke set up when registering the command.</span></span>
    
- <span data-ttu-id="ad9fb-145">в качестве команды, которую следует выполнять при обработке указанного события.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-145">As the command to be run when a specified event is trapped.</span></span>
    
> [!NOTE]
> <span data-ttu-id="ad9fb-146">Команды XLL являются скрытыми таким образом, что они не отображаются в списке доступных макросов в диалоговых окнах Excel.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-146">XLL commands are hidden in that they do not appear on the list of available macros in Excel dialog boxes.</span></span> <span data-ttu-id="ad9fb-147">Но они могут быть введены вручную в поле имени макроса.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-147">But they can be entered manually into the macro name field.</span></span> <span data-ttu-id="ad9fb-148">Excel ожидает заданное при регистрации имя в таких диалоговых окнах, а не имя операции экспорта DLL.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-148">Excel expects the registered-as name in these dialog boxes, not the DLL export name.</span></span> 
  
<span data-ttu-id="ad9fb-149">Приложение Excel обрабатывает все команды XLL, зарегистрированные в нем, как имеющие такой вид:</span><span class="sxs-lookup"><span data-stu-id="ad9fb-149">All XLL commands that are registered with Excel are assumed by Excel to be of the following form.</span></span>
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

<span data-ttu-id="ad9fb-p104">Excel игнорирует возвращаемое значение, если оно не вызывается с листа макросов XLM. В этом случае возвращаемое значение преобразуется в значение **TRUE** или **FALSE**. Таким образом, следует возвращать значение 1, если команда выполнена успешно, и 0, если она завершилась с ошибкой или была отменена пользователем.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-p104">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span>
  
<span data-ttu-id="ad9fb-152">Можно получить сведения о том, как команда была вызвана, с помощью функции C API **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-152">You can obtain information about how your command was invoked using the C API function **xlfCaller**.</span></span> <span data-ttu-id="ad9fb-153">Дополнительные сведения см. в статье [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="ad9fb-153">For more information, see [](xlfcaller.md).</span></span>
  
<span data-ttu-id="ad9fb-154">Начиная с Excel 2007 пользовательский интерфейс существенно отличается от более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-154">Starting in Excel 2007 user interface is very different from earlier versions.</span></span> <span data-ttu-id="ad9fb-155">В большинстве случаев по-прежнему поддерживаются функции C API, позволяющие выполнять операции добавления и удаления настраиваемых строк меню, меню, вложенных меню, элементов меню, настраиваемых панелей инструментов и кнопок панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-155">The C API functions that permit the addition and deletion of custom menu bars, menus, submenus, menu items, custom toolbars and toolbar buttons are still supported in most cases.</span></span> <span data-ttu-id="ad9fb-156">Тем не менее, они не всегда могут обеспечить доступность добавляемого элемента способом, который знаком вашим пользователям.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-156">However, they may not always make the added item available in a way that your users are familiar with.</span></span> <span data-ttu-id="ad9fb-157">Следует тщательно проверить, является ли любая добавленная функция по-прежнему доступной, или реализовать пользовательскую настройку под определенную версию.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-157">You should carefully check that any added functionality is still accessible, or implement a version-specific customization.</span></span> <span data-ttu-id="ad9fb-158">Начиная с Excel 2007 пользовательский интерфейс наилучшим образом настраивается с использованием модуля управляемого кода, который затем можно тесно связать с вашими командами XLL.</span><span class="sxs-lookup"><span data-stu-id="ad9fb-158">Starting in Excel 2007 the user interface is best customized by using a managed code module that can then be tightly coupled to your XLL commands.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ad9fb-159">См. также</span><span class="sxs-lookup"><span data-stu-id="ad9fb-159">See also</span></span>

- [<span data-ttu-id="ad9fb-160">Создание XLL-файлов</span><span class="sxs-lookup"><span data-stu-id="ad9fb-160">Creating XLLs</span></span>](creating-xlls.md)
- [<span data-ttu-id="ad9fb-161">Вызов функций XLL из диалоговых окон "Мастер функций" и "Замена"</span><span class="sxs-lookup"><span data-stu-id="ad9fb-161">Call XLL functions from the Function Wizard or Replace dialog boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [<span data-ttu-id="ad9fb-162">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="ad9fb-162">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
- [<span data-ttu-id="ad9fb-163">Разработка XLL-файлов для Excel</span><span class="sxs-lookup"><span data-stu-id="ad9fb-163">Developing Excel XLLs</span></span>](developing-excel-xlls.md)



