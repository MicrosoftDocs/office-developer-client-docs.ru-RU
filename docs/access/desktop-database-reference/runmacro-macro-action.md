---
title: Макрокоманда RunMacro
TOCTitle: RunMacro macro action
ms:assetid: 25966f20-8160-0821-b88a-ed08b7786fdc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191868(v=office.15)
ms:contentKeyID: 48543787
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm43195
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d9e86fb7d60af94d6ecde71b2a857a3cc5b9bcb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306855"
---
# <a name="runmacro-macro-action"></a><span data-ttu-id="a487a-102">Макрокоманда RunMacro</span><span class="sxs-lookup"><span data-stu-id="a487a-102">RunMacro macro action</span></span>

<span data-ttu-id="a487a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a487a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a487a-104">Для запуска макроса можно использовать макрокоманду **ЗапускМакроса** .</span><span class="sxs-lookup"><span data-stu-id="a487a-104">You can use the **RunMacro** action to run a macro.</span></span> <span data-ttu-id="a487a-105">Макрос может находиться в группе макросов.</span><span class="sxs-lookup"><span data-stu-id="a487a-105">The macro can be in a macro group.</span></span>

<span data-ttu-id="a487a-106">Вы можете использовать это действие:</span><span class="sxs-lookup"><span data-stu-id="a487a-106">You can use this action:</span></span>

- <span data-ttu-id="a487a-107">Для запуска макроса в другом макросе.</span><span class="sxs-lookup"><span data-stu-id="a487a-107">To run a macro from within another macro.</span></span>

- <span data-ttu-id="a487a-108">Для запуска макроса на основе определенного условия.</span><span class="sxs-lookup"><span data-stu-id="a487a-108">To run a macro based on a certain condition.</span></span>

- <span data-ttu-id="a487a-109">Присоединение макроса к команде настраиваемого меню.</span><span class="sxs-lookup"><span data-stu-id="a487a-109">To attach a macro to a custom menu command.</span></span>

## <a name="setting"></a><span data-ttu-id="a487a-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="a487a-110">Setting</span></span>

<span data-ttu-id="a487a-111">Макрокоманда **ЗапускМакроса** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="a487a-111">The **RunMacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a487a-112">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="a487a-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a487a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="a487a-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a487a-114"><strong>Имя макроса</strong></span><span class="sxs-lookup"><span data-stu-id="a487a-114"><strong>Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="a487a-115">Имя запускаемого макроса.</span><span class="sxs-lookup"><span data-stu-id="a487a-115">The name of the macro to run.</span></span> <span data-ttu-id="a487a-116">В поле <strong>имя макроса</strong> в разделе <strong>аргументы макрокоманды</strong> области построителя макросов отображаются все макросы (и группы макросов) текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="a487a-116">The <strong>Macro Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all macros (and macro groups) in the current database.</span></span> <span data-ttu-id="a487a-117">Если макрос находится в группе макросов, он отображается в списке под именем группы макросов в виде <em>макрограупнаме</em>. <em>имяМакроса</em>.</span><span class="sxs-lookup"><span data-stu-id="a487a-117">If the macro is in a macro group, it's listed under the macro group name in the list as <em>macrogroupname</em>.<em>macroname</em>.</span></span> <span data-ttu-id="a487a-118">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="a487a-118">This is a required argument.</span></span> <span data-ttu-id="a487a-119">При запуске макроса, содержащего макрокоманду <strong>ЗапускМакроса</strong> , в библиотечной базе данных Microsoft Access ищет макрос с этим именем в базе данных библиотеки и не ищет его в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="a487a-119">If you run a macro containing the <strong>RunMacro</strong> action in a library database, Microsoft Access looks for the macro with this name in the library database and doesn't look for it in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a487a-120"><strong>Число повторов</strong></span><span class="sxs-lookup"><span data-stu-id="a487a-120"><strong>Repeat Count</strong></span></span></p></td>
<td><p><span data-ttu-id="a487a-121">Максимальное число запусков макроса.</span><span class="sxs-lookup"><span data-stu-id="a487a-121">The maximum number of times the macro will run.</span></span> <span data-ttu-id="a487a-122">Если оставить этот аргумент пустым (и аргумент <strong>выражения Repeat</strong> также пуст), макрос будет выполняться один раз.</span><span class="sxs-lookup"><span data-stu-id="a487a-122">If you leave this argument blank (and the <strong>Repeat Expression</strong> argument is also blank), the macro runs once.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a487a-123"><strong>Выражение Repeat</strong></span><span class="sxs-lookup"><span data-stu-id="a487a-123"><strong>Repeat Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="a487a-124">Выражение, которое оценивается как <strong>истинное</strong> (– 1) или <strong>false</strong> (0).</span><span class="sxs-lookup"><span data-stu-id="a487a-124">An expression that evaluates to <strong>True</strong> (–1) or <strong>False</strong> (0).</span></span> <span data-ttu-id="a487a-125">Выполнение макроса завершается, если выражение имеет <strong>значение false</strong>.</span><span class="sxs-lookup"><span data-stu-id="a487a-125">The macro stops running if the expression evaluates to <strong>False</strong>.</span></span> <span data-ttu-id="a487a-126">Выражение оценивается каждый раз при запуске макроса.</span><span class="sxs-lookup"><span data-stu-id="a487a-126">The expression is evaluated each time the macro runs.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="a487a-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="a487a-127">Remarks</span></span>

<span data-ttu-id="a487a-128">Если ввести имя группы макросов для аргумента **имя макроса** , Access выполняет первый макрос в группе макросов.</span><span class="sxs-lookup"><span data-stu-id="a487a-128">If you enter a macro group name for the **Macro Name** argument, Access runs the first macro in the macro group.</span></span>

<span data-ttu-id="a487a-129">Это действие аналогично нажатию кнопки **выполнить макрос** на вкладке **Работа с базами данных** , выбором макроса и нажатием кнопки **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a487a-129">This action is similar to clicking **Run Macro** on the **Database Tools** tab, selecting a macro, and clicking **OK**.</span></span> <span data-ttu-id="a487a-130">Тем не менее, эта команда выполняет макрос только один раз, а Макрокоманда **ЗапускМакроса** может выполнять макрос произвольное количество раз.</span><span class="sxs-lookup"><span data-stu-id="a487a-130">However, this command runs the macro only once, whereas the **RunMacro** action can run a macro as many times as you want.</span></span>

> [!TIP]
> <span data-ttu-id="a487a-131">Вы можете использовать аргументы **Repeat Count** и **Repeat Expression** , чтобы определить, сколько раз будет выполняться макрос:</span><span class="sxs-lookup"><span data-stu-id="a487a-131">You can use the **Repeat Count** and **Repeat Expression** arguments to determine how many times the macro runs:</span></span>
> - <span data-ttu-id="a487a-132">Если оставить оба аргумента пустыми, макрос будет выполняться один раз.</span><span class="sxs-lookup"><span data-stu-id="a487a-132">If you leave both arguments blank, the macro runs once.</span></span>
> - <span data-ttu-id="a487a-133">Если ввести число **повторных** попыток, но оставить **выражение Repeat** пустым, макрос будет выполняться указанное число раз.</span><span class="sxs-lookup"><span data-stu-id="a487a-133">If you enter a number for **Repeat Count** but leave **Repeat Expression** blank, the macro runs the specified number of times.</span></span>
> - <span data-ttu-id="a487a-134">Если оставить **число повторов** пустым, но ввести выражение для **выражения Repeat**, макрос будет выполняться до тех пор, пока выражение не станет равно **false**.</span><span class="sxs-lookup"><span data-stu-id="a487a-134">If you leave **Repeat Count** blank but enter an expression for **Repeat Expression**, the macro runs until the expression evaluates to **False**.</span></span>
> - <span data-ttu-id="a487a-135">Если вы вводите значения для обоих аргументов, макрос запустится количество раз, указанное в поле **число повторов** или пока **выражение Repeat** не будет равно **false**, что происходит в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="a487a-135">If you enter values for both arguments, the macro runs the number of times specified in **Repeat Count** or until **Repeat Expression** evaluates to **False**, whichever occurs first.</span></span>

<span data-ttu-id="a487a-136">При запуске макроса, содержащего макрокоманду **ЗапускМакроса** , и достижении макрокоманды **ЗапускМакроса** , Access запускает вызываемый макрос.</span><span class="sxs-lookup"><span data-stu-id="a487a-136">When you run a macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called macro.</span></span> <span data-ttu-id="a487a-137">После завершения вызванного макроса Access возвращается к исходному макросу и выполняет следующее действие.</span><span class="sxs-lookup"><span data-stu-id="a487a-137">When the called macro has finished, Access returns to the original macro and runs the next action.</span></span>

> [!NOTE]
> - <span data-ttu-id="a487a-138">Вы можете вызвать макрос в той же группе макросов или в другой группе макросов.</span><span class="sxs-lookup"><span data-stu-id="a487a-138">You can call a macro in the same macro group or in another macro group.</span></span>
> - <span data-ttu-id="a487a-139">Вы можете вложить макросы.</span><span class="sxs-lookup"><span data-stu-id="a487a-139">You can nest macros.</span></span> <span data-ttu-id="a487a-140">То есть вы можете запустить макрос A, который, в свою очередь, вызывает макрос B и т. д.</span><span class="sxs-lookup"><span data-stu-id="a487a-140">That is, you can run macro A, which in turn calls macro B, and so on.</span></span> <span data-ttu-id="a487a-141">В каждом случае, когда вызванный макрос закончился, доступ возвращается к макросу, который вызывает его, и выполняет следующее действие в этом макросе.</span><span class="sxs-lookup"><span data-stu-id="a487a-141">In each case, when the called macro has finished, Access returns to the macro that called it and runs the next action in that macro.</span></span>

<span data-ttu-id="a487a-142">Чтобы выполнить макрокоманду **ЗапускМакроса** в модуле Visual Basic для приложений (VBA), используйте метод **RunMacro** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="a487a-142">To run the **RunMacro** action in a Visual Basic for Applications (VBA) module, use the **RunMacro** method of the **DoCmd** object.</span></span>

