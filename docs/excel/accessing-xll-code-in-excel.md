---
title: Доступ к XLL-коду в Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- доступ к xll-коду [excel 2007,] XLL-модулей [Excel 2007], доступ к кода, команды [Excel 2007], регистрация, функции [Excel 2007], регистрация, звонок XLL-модулей для Excel, регистрация команды [Excel 2007], регистрация функций [Excel 2007]
localization_priority: Normal
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1523f9e8213cb955f1bfd995c42f921b001299fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807145"
---
# <a name="accessing-xll-code-in-excel"></a><span data-ttu-id="18ae9-104">Доступ к XLL-коду в Excel</span><span class="sxs-lookup"><span data-stu-id="18ae9-104">Accessing XLL code in Excel</span></span>

<span data-ttu-id="18ae9-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="18ae9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="18ae9-106">Должно быть доступно в Microsoft Excel, функции и команды, которые содержит XLL-модуль:</span><span class="sxs-lookup"><span data-stu-id="18ae9-106">To be accessible in Microsoft Excel, the functions and commands that an XLL contains:</span></span>
  
- <span data-ttu-id="18ae9-107">Необходимо экспортировать с XLL.</span><span class="sxs-lookup"><span data-stu-id="18ae9-107">Must be exported by the XLL.</span></span>
    
- <span data-ttu-id="18ae9-108">Должны быть зарегистрированы в Excel.</span><span class="sxs-lookup"><span data-stu-id="18ae9-108">Must be registered with Excel.</span></span>
    
## <a name="registering-functions-and-commands-with-excel"></a><span data-ttu-id="18ae9-109">Регистрация команды и функций в Excel</span><span class="sxs-lookup"><span data-stu-id="18ae9-109">Registering functions and commands with Excel</span></span>

<span data-ttu-id="18ae9-110">Регистрация сообщает о точки входа библиотеки DLL Excel следующее:</span><span class="sxs-lookup"><span data-stu-id="18ae9-110">Registration tells Excel the following about a DLL entry point:</span></span>
  
- <span data-ttu-id="18ae9-111">Будет ли оно скрыто или, если функция, будет ли это видимы в Мастер функций.</span><span class="sxs-lookup"><span data-stu-id="18ae9-111">Whether it is hidden or, if a function, whether it is visible in the Function Wizard.</span></span>
    
- <span data-ttu-id="18ae9-112">Будет ли это вызывать только из таблицы макросов XLM или из листа.</span><span class="sxs-lookup"><span data-stu-id="18ae9-112">Whether it is callable only from an XLM macro sheet, or also from a worksheet.</span></span>
    
- <span data-ttu-id="18ae9-113">Если команда, будет ли это функция листа или эквивалентную функцию листа макросов.</span><span class="sxs-lookup"><span data-stu-id="18ae9-113">If a command, whether it is a worksheet function or a macro sheet equivalent function.</span></span>
    
- <span data-ttu-id="18ae9-114">Экспорт именем XLL/DLL и введите имя, которое требуется Excel для использования.</span><span class="sxs-lookup"><span data-stu-id="18ae9-114">What its XLL/DLL export name is, and what name you want Excel to use.</span></span>
    
- <span data-ttu-id="18ae9-115">Если функция:</span><span class="sxs-lookup"><span data-stu-id="18ae9-115">If it is a function:</span></span>
    
  - <span data-ttu-id="18ae9-116">Какие данные его тип возвращает и принимает в качестве аргументов.</span><span class="sxs-lookup"><span data-stu-id="18ae9-116">What data types it returns and takes as arguments.</span></span>
    
  - <span data-ttu-id="18ae9-117">Оно возвращает результат путем изменения аргумента на месте.</span><span class="sxs-lookup"><span data-stu-id="18ae9-117">Whether it returns its result by modifying an argument in place.</span></span>
    
  - <span data-ttu-id="18ae9-118">Будет ли это переменные.</span><span class="sxs-lookup"><span data-stu-id="18ae9-118">Whether it is volatile.</span></span>
    
  - <span data-ttu-id="18ae9-119">Будет ли это потокобезопасными (поддерживаемые начиная с версии Excel 2007).</span><span class="sxs-lookup"><span data-stu-id="18ae9-119">Whether it is thread safe (supported starting in Excel 2007).</span></span>
    
  - <span data-ttu-id="18ae9-120">При вызове функции должны отображать какой Мастер функций вставить текст и редактор автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="18ae9-120">What text the Paste Function Wizard and AutoComplete editor should display to help with calling the function.</span></span>
    
  - <span data-ttu-id="18ae9-121">Которой работает, оно должно быть указано в разделе категории.</span><span class="sxs-lookup"><span data-stu-id="18ae9-121">Which function category it should be listed under.</span></span>
    
<span data-ttu-id="18ae9-122">Это все достигается с помощью интерфейса API для C функция [xlfRegister](xlfregister-form-1.md), эквивалентен функции XLM **регистрации**.</span><span class="sxs-lookup"><span data-stu-id="18ae9-122">This is all achieved using the C API function [xlfRegister](xlfregister-form-1.md), equivalent to the XLM function **REGISTER**.</span></span>
  
## <a name="calling-xll-functions-directly-from-excel"></a><span data-ttu-id="18ae9-123">Вызов функции XLL непосредственно из Excel</span><span class="sxs-lookup"><span data-stu-id="18ae9-123">Calling XLL functions directly from Excel</span></span>

<span data-ttu-id="18ae9-124">После регистрации они функции листа XLL листа и макрос можно вызывать из везде, где встроенные функции могут вызываться из:</span><span class="sxs-lookup"><span data-stu-id="18ae9-124">Once they are registered, XLL worksheet and macro sheet functions can be called from anywhere a built-in function can be called from:</span></span>
  
- <span data-ttu-id="18ae9-125">Формула одной ячейки или массив на листе.</span><span class="sxs-lookup"><span data-stu-id="18ae9-125">A single-cell or array formula on a worksheet.</span></span>
    
- <span data-ttu-id="18ae9-126">Формула одной ячейки или массив на листе макросов.</span><span class="sxs-lookup"><span data-stu-id="18ae9-126">A single-cell or array formula on a macro sheet.</span></span>
    
- <span data-ttu-id="18ae9-127">Определение определенного имени.</span><span class="sxs-lookup"><span data-stu-id="18ae9-127">The definition of a defined name.</span></span>
    
- <span data-ttu-id="18ae9-128">Условия и ограничения полей в диалоговом окне Условное форматирование.</span><span class="sxs-lookup"><span data-stu-id="18ae9-128">The condition and limit fields in a conditional format dialog box.</span></span>
    
- <span data-ttu-id="18ae9-129">Из другой надстройки с помощью функции интерфейса API для C [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="18ae9-129">From another add-in via the C API function [xlUDF](xludf.md).</span></span>
    
- <span data-ttu-id="18ae9-130">В Visual Basic для приложений (VBA) с помощью метода **Application.Run** .</span><span class="sxs-lookup"><span data-stu-id="18ae9-130">From Visual Basic for Applications (VBA) via the **Application.Run** method.</span></span> 
    
<span data-ttu-id="18ae9-131">Можно получить ссылку на вызывающий ячейки или диапазона ячеек в функции с помощью функции интерфейса API для C **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="18ae9-131">You can obtain a reference to the calling cell or range of cells within your function using the C API function **xlfCaller**.</span></span> <span data-ttu-id="18ae9-132">При вызове функции из ячейки условное форматирование в выражение, вы по-прежнему возвращаются ссылку на связанный одну или несколько ячеек, поэтому нельзя предполагается, что формула ячейки содержит функции XLL.</span><span class="sxs-lookup"><span data-stu-id="18ae9-132">If the function was called from the cell's conditional format expression, you are still returned a reference to the associated cell or cells, so you cannot assume that the cell's formula contains the XLL function.</span></span> <span data-ttu-id="18ae9-133">Если функция вызван из VBA пользовательской функции (UDF), **xlfCaller** еще раз возвращает адрес ячейки, вызывать функцию VBA.</span><span class="sxs-lookup"><span data-stu-id="18ae9-133">If your function was called from a VBA user-defined function (UDF), **xlfCaller** again returns the address of the cells that called the VBA function.</span></span> <span data-ttu-id="18ae9-134">Для получения дополнительных сведений см [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="18ae9-134">For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="18ae9-135">Excel также вызывает функции XLL-коду в диалоговых окнах **Мастер функции вставки** и **замены** .</span><span class="sxs-lookup"><span data-stu-id="18ae9-135">Excel also calls XLL function code from the **Paste Function Wizard** and **Replace** dialog boxes.</span></span> <span data-ttu-id="18ae9-136">Может потребоваться ограничить в случае диалогового окна **Вставить функцию аргументов** , особенно где функции может занять много времени на выполнение обычных выполнение вашего кода.</span><span class="sxs-lookup"><span data-stu-id="18ae9-136">You might need to restrict your code's normal running in the case of the **Paste Function Arguments** dialog box, especially where your function can take a long time to execute.</span></span> <span data-ttu-id="18ae9-137">Для определения, если функция вызывается с помощью одной из этих диалоговых окон, необходимо реализовать часть кода в проекте, который выполняет итерацию всех открытых окон, чтобы определить, если окно переднего один из этих диалоговых окон и если да, какой из них.</span><span class="sxs-lookup"><span data-stu-id="18ae9-137">To detect if your function is being called from either of these dialog boxes, you must implement some code in your project that iterates through all the open windows to determine if the front window is one of these dialog boxes, and, if so, which one.</span></span> 
  
## <a name="calling-xll-commands-directly-from-excel"></a><span data-ttu-id="18ae9-138">Вызов команд XLL непосредственно из Excel</span><span class="sxs-lookup"><span data-stu-id="18ae9-138">Calling XLL commands directly from Excel</span></span>

<span data-ttu-id="18ae9-139">После регистрации они XLL команды можно вызвать одним из способов, что можно вызвать другие пользовательские макросы:</span><span class="sxs-lookup"><span data-stu-id="18ae9-139">Once they are registered, XLL commands can be called in all the ways that other user-defined macros can be called:</span></span>
  
- <span data-ttu-id="18ae9-140">Связанного с объектом управления внедренным в лист.</span><span class="sxs-lookup"><span data-stu-id="18ae9-140">By being associated with a control object embedded on a worksheet.</span></span>
    
- <span data-ttu-id="18ae9-141">В диалоговом окне выполнить макрос.</span><span class="sxs-lookup"><span data-stu-id="18ae9-141">From the Run Macro dialog box.</span></span>
    
- <span data-ttu-id="18ae9-142">Из пользовательских макроса VBA с помощью метода **Application.Run** .</span><span class="sxs-lookup"><span data-stu-id="18ae9-142">From a VBA user-defined macro using the **Application.Run** method.</span></span> 
    
- <span data-ttu-id="18ae9-143">Элемент настраиваемого меню или панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="18ae9-143">From a customized menu item or toolbar.</span></span>
    
- <span data-ttu-id="18ae9-144">С помощью сочетания клавиш настроить при регистрации команда.</span><span class="sxs-lookup"><span data-stu-id="18ae9-144">Using a shortcut keystroke set up when registering the command.</span></span>
    
- <span data-ttu-id="18ae9-145">Перехват что команда выполняется, если указанный события.</span><span class="sxs-lookup"><span data-stu-id="18ae9-145">As the command to be run when a specified event is trapped.</span></span>
    
> [!NOTE]
> <span data-ttu-id="18ae9-146">Команды XLL скрыты, в том, что они не отображаются в списке доступных макросов в Excel диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="18ae9-146">XLL commands are hidden in that they do not appear on the list of available macros in Excel dialog boxes.</span></span> <span data-ttu-id="18ae9-147">Однако они могут быть введены вручную в поле имя макроса.</span><span class="sxs-lookup"><span data-stu-id="18ae9-147">But they can be entered manually into the macro name field.</span></span> <span data-ttu-id="18ae9-148">Предполагается, что имя зарегистрирована как в этих диалоговых окнах, а не имя DLL-файла экспорта.</span><span class="sxs-lookup"><span data-stu-id="18ae9-148">Excel expects the registered-as name in these dialog boxes, not the DLL export name.</span></span> 
  
<span data-ttu-id="18ae9-149">Все команды XLL, зарегистрированных в Excel предполагается, что в Excel, чтобы иметь следующий вид:</span><span class="sxs-lookup"><span data-stu-id="18ae9-149">All XLL commands registered with Excel are assumed by Excel to be of the following form:</span></span>
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

<span data-ttu-id="18ae9-p104">Excel игнорирует возвращаемое значение, если оно не вызывается с листа макросов XLM. В этом случае возвращаемое значение преобразуется в значение **TRUE** или **FALSE**. Таким образом, следует возвращать значение 1, если команда выполнена успешно, и 0, если она завершилась с ошибкой или была отменена пользователем.</span><span class="sxs-lookup"><span data-stu-id="18ae9-p104">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span>
  
<span data-ttu-id="18ae9-152">Вы можете получить сведения о вызов команду с помощью интерфейса API для C работать **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="18ae9-152">You can obtain information about how your command was invoked using the C API function **xlfCaller**.</span></span> <span data-ttu-id="18ae9-153">Для получения дополнительных сведений см [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="18ae9-153">For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
<span data-ttu-id="18ae9-154">Начиная с версии Excel 2007 пользовательского интерфейса очень отличается от более ранних версий.</span><span class="sxs-lookup"><span data-stu-id="18ae9-154">Starting in Excel 2007 user interface is very different from earlier versions.</span></span> <span data-ttu-id="18ae9-155">Функции интерфейса API для C, которые разрешают Добавление и удаление настраиваемых меню, меню, подменю, элементов меню, настраиваемые панели инструментов и кнопки панели инструментов по-прежнему поддерживается в большинстве случаев.</span><span class="sxs-lookup"><span data-stu-id="18ae9-155">The C API functions that permit the addition and deletion of custom menu bars, menus, submenus, menu items, custom toolbars and toolbar buttons are still supported in most cases.</span></span> <span data-ttu-id="18ae9-156">Тем не менее они могут не всегда вносить добавленного элемента недоступны, чтобы пользователи знакомы с.</span><span class="sxs-lookup"><span data-stu-id="18ae9-156">However, they may not always make the added item available in a way that your users are familiar with.</span></span> <span data-ttu-id="18ae9-157">Следует тщательно проверять по-прежнему доступны любые дополнительные функции или реализовать настройки разных версий.</span><span class="sxs-lookup"><span data-stu-id="18ae9-157">You should carefully check that any added functionality is still accessible, or implement a version-specific customization.</span></span> <span data-ttu-id="18ae9-158">Начиная с версии Excel 2007 пользовательского интерфейса лучше всего настроить с помощью модуля управляемого кода, который может затем быть тесно связаны с вашим командам XLL.</span><span class="sxs-lookup"><span data-stu-id="18ae9-158">Starting in Excel 2007 the user interface is best customized by using a managed code module that can then be tightly coupled to your XLL commands.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="18ae9-159">См. также</span><span class="sxs-lookup"><span data-stu-id="18ae9-159">See also</span></span>

- [<span data-ttu-id="18ae9-160">Создание XLL-файлов</span><span class="sxs-lookup"><span data-stu-id="18ae9-160">Creating XLLs</span></span>](creating-xlls.md)
- [<span data-ttu-id="18ae9-161">Вызов функций XLL из диалоговых окон "Мастер функций" и "Замена"</span><span class="sxs-lookup"><span data-stu-id="18ae9-161">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [<span data-ttu-id="18ae9-162">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="18ae9-162">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
- [<span data-ttu-id="18ae9-163">���������� XLL-������� ��� Excel 2013</span><span class="sxs-lookup"><span data-stu-id="18ae9-163">Developing Excel XLLs</span></span>](developing-excel-xlls.md)



