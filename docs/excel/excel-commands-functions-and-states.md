---
title: Команды, функции и состояния Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- состояния [excel 2007], команды [Excel 2007], функции листов [Excel 2007], функции листа макросов [Excel 2007], состояния Excel
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: c941ba7445f1f0598bf044b5f177ad576df0137c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716238"
---
# <a name="excel-commands-functions-and-states"></a><span data-ttu-id="e75c4-104">Команды, функции и состояния Excel</span><span class="sxs-lookup"><span data-stu-id="e75c4-104">Excel Commands, Functions, and States</span></span>

 <span data-ttu-id="e75c4-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e75c4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e75c4-106">Microsoft Excel распознает два очень разные типа дополнительных функциональных возможностей: команды и функции.</span><span class="sxs-lookup"><span data-stu-id="e75c4-106">Microsoft Excel recognizes two very different types of added functionality: commands and functions.</span></span>
  
## <a name="commands"></a><span data-ttu-id="e75c4-107">Команды</span><span class="sxs-lookup"><span data-stu-id="e75c4-107">Commands</span></span>

<span data-ttu-id="e75c4-108">В Excel команды имеют следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="e75c4-108">In Excel, commands have the following characteristics:</span></span>
  
- <span data-ttu-id="e75c4-109">Выполняют действия так же, как и пользователи.</span><span class="sxs-lookup"><span data-stu-id="e75c4-109">They perform actions in the same way that users do.</span></span>
    
- <span data-ttu-id="e75c4-110">Могут делать все, что может пользователь (в зависимости от ограничений используемого интерфейса), например изменять параметры Excel, открывать, закрывать и редактировать документы, выполнять пересчеты и т. д.</span><span class="sxs-lookup"><span data-stu-id="e75c4-110">They can do anything a user can do (subject to the limits of the interface used), such as altering Excel settings, opening, closing, and editing documents, initiating recalculations, and so on.</span></span>
    
- <span data-ttu-id="e75c4-111">Могут вызываться, когда происходят определенные обрабатываемые события.</span><span class="sxs-lookup"><span data-stu-id="e75c4-111">They can be set up to be called when certain trapped events occur.</span></span>
    
- <span data-ttu-id="e75c4-112">Могут отображать диалоговые окна и взаимодействовать с пользователем.</span><span class="sxs-lookup"><span data-stu-id="e75c4-112">They can display dialog boxes and interact with the user.</span></span>
    
- <span data-ttu-id="e75c4-113">Могут вызываться при выполнении определенных действиях с объектом, например щелчке левой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="e75c4-113">They can be linked to control objects so that they are called when some action is taken on that object, such as left-clicking.</span></span>
    
- <span data-ttu-id="e75c4-114">Они никогда не вызываются программой Excel во время пересчета.</span><span class="sxs-lookup"><span data-stu-id="e75c4-114">They are never called by Excel during a recalculation.</span></span>
    
- <span data-ttu-id="e75c4-115">Они не вызываются функциями во время пересчета.</span><span class="sxs-lookup"><span data-stu-id="e75c4-115">They cannot be called by functions during a recalculation.</span></span>
    
## <a name="functions"></a><span data-ttu-id="e75c4-116">Функции</span><span class="sxs-lookup"><span data-stu-id="e75c4-116">Functions</span></span>

<span data-ttu-id="e75c4-117">В Excel функции имеют следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="e75c4-117">Functions in Excel do the following:</span></span>
  
- <span data-ttu-id="e75c4-118">Как правило, принимают аргументы и всегда возвращают результат.</span><span class="sxs-lookup"><span data-stu-id="e75c4-118">They usually take arguments and always return a result.</span></span>
    
- <span data-ttu-id="e75c4-119">Могут вводиться в одну или несколько ячеек в составе формулы Excel.</span><span class="sxs-lookup"><span data-stu-id="e75c4-119">They can be entered into one or more cells as part of an Excel formula.</span></span>
    
- <span data-ttu-id="e75c4-120">Могут использоваться в определениях определенных имен.</span><span class="sxs-lookup"><span data-stu-id="e75c4-120">They can be used in defined name definitions.</span></span>
    
- <span data-ttu-id="e75c4-121">Могут использоваться в выражениях лимитов и порогов условного форматирования.</span><span class="sxs-lookup"><span data-stu-id="e75c4-121">They can be used in conditional formatting limit and threshold expressions.</span></span>
    
- <span data-ttu-id="e75c4-122">Могут вызываться командами.</span><span class="sxs-lookup"><span data-stu-id="e75c4-122">They can be called by commands.</span></span>
    
- <span data-ttu-id="e75c4-123">Не могут вызывать команды.</span><span class="sxs-lookup"><span data-stu-id="e75c4-123">They cannot call commands.</span></span>
    
<span data-ttu-id="e75c4-p101">В Excel выделяются пользовательские функции листа и пользовательские функции, предназначенные для работы на листах макросов. Excel не ограничивает использование функций пользовательского листа макроса только листами макросов: эти функции можно использовать там, где используется обычная функция листа.</span><span class="sxs-lookup"><span data-stu-id="e75c4-p101">Excel makes a further distinction between user-defined worksheet functions and user-defined functions that are designed to work on macro sheets. Excel does not limit user-defined macro sheet functions only to being used on macro sheets: these functions can be used anywhere a normal worksheet function can be used.</span></span>
  
### <a name="worksheet-functions"></a><span data-ttu-id="e75c4-126">Функции листа</span><span class="sxs-lookup"><span data-stu-id="e75c4-126">Worksheet Functions</span></span>

<span data-ttu-id="e75c4-127">В Excel функции листа имеют следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="e75c4-127">The following is true of Excel worksheet functions:</span></span>
  
- <span data-ttu-id="e75c4-128">Не имеют доступа к информационным функциям листа макросов.</span><span class="sxs-lookup"><span data-stu-id="e75c4-128">They cannot access macro sheet information functions.</span></span>
    
- <span data-ttu-id="e75c4-129">Не могут получать значения невычисленных ячеек.</span><span class="sxs-lookup"><span data-stu-id="e75c4-129">They cannot obtain the values of uncalculated cells.</span></span>
    
- <span data-ttu-id="e75c4-130">Могут записываться и регистрироваться как потокобезопасные, начиная с Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="e75c4-130">They can be written and registered as thread-safe starting in Excel 2007.</span></span>
    
### <a name="macro-sheet-functions"></a><span data-ttu-id="e75c4-131">Функции листа макросов</span><span class="sxs-lookup"><span data-stu-id="e75c4-131">Macro-Sheet Functions</span></span>

<span data-ttu-id="e75c4-132">В Excel функции листа макросов имеют следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="e75c4-132">The following is true of Excel macro-sheet functions:</span></span>
  
- <span data-ttu-id="e75c4-133">Имеют доступ к информационным функциям листа макросов.</span><span class="sxs-lookup"><span data-stu-id="e75c4-133">They can access macro sheet information functions.</span></span>
    
- <span data-ttu-id="e75c4-134">Могут получать значения невычисленных ячеек, в том числе значения вызывающих ячеек.</span><span class="sxs-lookup"><span data-stu-id="e75c4-134">They can obtain the values of uncalculated cells including the values of the calling cells.</span></span>
    
- <span data-ttu-id="e75c4-135">Не считаются потокобезопасными, начиная с Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="e75c4-135">They are not considered thread safe starting in Excel 2007.</span></span>
    
<span data-ttu-id="e75c4-p102">То, как Excel обрабатывает пользовательскую функцию (user-defined function, UDF), что позволяет ей делать и как пересчитывает, определяется при регистрации. Если функция зарегистрирована как функция листа, но пытается выполнить неразрешенное действие, произойдет ошибка. Начиная с Excel 2007, если функция листа, зарегистрированная как потокобезопасная, пытается вызвать функцию листа макросов, происходит ошибка.</span><span class="sxs-lookup"><span data-stu-id="e75c4-p102">How Excel treats a user-defined function (UDF), what it permits the function to do, and how it recalculates the function are all determined when you register the function. If a function is registered as a worksheet function but tries to do something that only a macro-sheet function can do, the operation fails. Starting in Excel 2007, if a worksheet function registered as thread safe tries to call a macro sheet function, again, the operation fails.</span></span>
  
<span data-ttu-id="e75c4-139">Excel обрабатывает функции UDF Microsoft Visual Basic для приложений как функции листа макросов, в том плане, что они имеют доступ к информации рабочей области и значению невычисленных ячеек, и не считаются потокобезопасными, начиная с Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="e75c4-139">Excel treats Microsoft Visual Basic for Applications (VBA) UDFs as macro sheet-equivalent functions, in that they can access workspace information and the value of uncalculated cells, and they are not considered as thread safe starting in Excel 2007.</span></span>
  
## <a name="excel-states"></a><span data-ttu-id="e75c4-140">Состояния Excel</span><span class="sxs-lookup"><span data-stu-id="e75c4-140">Excel States</span></span>

<span data-ttu-id="e75c4-141">Excel может находится в одном из нескольких состояний в любое время в зависимости от действий пользователя, внешнего процесса, обработанного события, запустившего макрос, или запланированного события, такого как **Автосохранение**.</span><span class="sxs-lookup"><span data-stu-id="e75c4-141">Excel can be in one of a number of states at any given time depending on the actions of the user, an external process, a trapped event running a macro, or a timed Excel housekeeping event such as **Autosave**.</span></span>
  
<span data-ttu-id="e75c4-142">Ниже описаны возможные состояния.</span><span class="sxs-lookup"><span data-stu-id="e75c4-142">The states that the user experiences are as follows:</span></span>
  
- <span data-ttu-id="e75c4-p103">**Состояние готовности:** ни команды, ни макросы не выполняются. Диалоговые окна не отображаются. Ячейки не редактируются. Пользователь не вырезал/не скопировал объект для вставки. Внедренные объекты не находятся в фокусе.</span><span class="sxs-lookup"><span data-stu-id="e75c4-p103">**Ready state:** No commands or macros are being run. No dialog boxes are being displayed. No cells are being edited and the user is not in the middle of a cut/copy and paste operation. No embedded object has focus.</span></span> 
    
- <span data-ttu-id="e75c4-147">**Режим правки:** пользователь начал вводить допустимые символы в незаблокированную или незащищенную ячейку, или нажал клавишу **F2** для одной или нескольких незаблокированных или незащищенных ячеек.</span><span class="sxs-lookup"><span data-stu-id="e75c4-147">**Edit mode:** The user has started to type valid input characters into an unlocked or unprotected cell, or has pressed **F2** on one or more unlocked or unprotected cells.</span></span> 
    
- <span data-ttu-id="e75c4-148">**Режим вырезания/копирования и вставки:** пользователя вырезал или скопировал ячейку или ряд ячеек и еще не вставил их или вставил с помощью диалогового окна "Специальная вставка", позволяющего выполнять несколько операций вставки.</span><span class="sxs-lookup"><span data-stu-id="e75c4-148">**Cut/copy and paste mode:** The user has cut or copied a cell or range of cells and has not yet pasted them, or has pasted them using the paste-special dialog box, which enables multiple paste operations.</span></span> 
    
- <span data-ttu-id="e75c4-149">**Режим указания:** пользователь редактирует формулу и выбирает ячейки, адреса которых будут добавлены в редактируемую формулу.</span><span class="sxs-lookup"><span data-stu-id="e75c4-149">**Point mode:** The user is editing a formula and is selecting cells whose addresses are added to the formula being edited.</span></span> 
    
<span data-ttu-id="e75c4-p104">Пользователь может выйти из режима редактирования, указания, вырезания или копирования, нажав клавишу **ESC**, которая возвращает Excel в состояние готовности. Другие события также могут вывести Excel из этих состояний:</span><span class="sxs-lookup"><span data-stu-id="e75c4-p104">The user can clear the edit, point, and cut/copy modes by pressing the **ESC** key, which returns Excel to its ready state. Other events can clear these states, such as the following:</span></span> 
  
- <span data-ttu-id="e75c4-152">Пользователь открывает встроенное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e75c4-152">The user opens a built-in dialog box.</span></span>
    
- <span data-ttu-id="e75c4-153">Пользователь инициирует пересчет.</span><span class="sxs-lookup"><span data-stu-id="e75c4-153">The user initiates a recalculation.</span></span>
    
- <span data-ttu-id="e75c4-154">Пользователь выполняет команду.</span><span class="sxs-lookup"><span data-stu-id="e75c4-154">The user runs a command.</span></span>
    
- <span data-ttu-id="e75c4-155">Excel выполняет операцию **Автосохранение**.</span><span class="sxs-lookup"><span data-stu-id="e75c4-155">Excel performs an **Autosave** operation.</span></span> 
    
- <span data-ttu-id="e75c4-156">Обработано событие-таймер.</span><span class="sxs-lookup"><span data-stu-id="e75c4-156">A timer event is trapped.</span></span>
    
<span data-ttu-id="e75c4-p105">Последний пример важен для разработчиков надстроек. Обратите внимание на влияние обычных уровней использования Excel, когда устанавливаются и используются частые ловушки событий-таймеров. Если это важная часть функционала ваших надстроек, вы должны предоставить пользователям легких способ его приостановки, чтобы они могли вырезать, копировать и вставлять, когда это необходимо.</span><span class="sxs-lookup"><span data-stu-id="e75c4-p105">The last example is of importance to add-in developers. You should consider the impact of the normal usability of Excel where frequent timer event traps are being set and executed. When this is an important part of your add-in's functionality, you should provide users with an easily accessible way of suspending it, so that they can cut/copy and paste normally when they need to.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e75c4-160">См. также</span><span class="sxs-lookup"><span data-stu-id="e75c4-160">See also</span></span>



[<span data-ttu-id="e75c4-161">Понятия, связанные с программированием для Excel</span><span class="sxs-lookup"><span data-stu-id="e75c4-161">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
[<span data-ttu-id="e75c4-162">Разрешение прерывания длительных операций пользователем</span><span class="sxs-lookup"><span data-stu-id="e75c4-162">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)

