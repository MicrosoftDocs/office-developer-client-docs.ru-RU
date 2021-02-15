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
# <a name="runmacro-macro-action"></a><span data-ttu-id="4b705-102">Макрокоманда RunMacro</span><span class="sxs-lookup"><span data-stu-id="4b705-102">RunMacro macro action</span></span>

<span data-ttu-id="4b705-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b705-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b705-104">Для запуска макроса можно использовать действие **RunMacro.**</span><span class="sxs-lookup"><span data-stu-id="4b705-104">You can use the **RunMacro** action to run a macro.</span></span> <span data-ttu-id="4b705-105">Макрос может быть в группе макроса.</span><span class="sxs-lookup"><span data-stu-id="4b705-105">The macro can be in a macro group.</span></span>

<span data-ttu-id="4b705-106">Можно использовать это действие:</span><span class="sxs-lookup"><span data-stu-id="4b705-106">You can use this action:</span></span>

- <span data-ttu-id="4b705-107">Запуск макроса из другого макроса.</span><span class="sxs-lookup"><span data-stu-id="4b705-107">To run a macro from within another macro.</span></span>

- <span data-ttu-id="4b705-108">Запуск макроса на основе определенного условия.</span><span class="sxs-lookup"><span data-stu-id="4b705-108">To run a macro based on a certain condition.</span></span>

- <span data-ttu-id="4b705-109">Присоединение макроса к настраиваемой команде меню.</span><span class="sxs-lookup"><span data-stu-id="4b705-109">To attach a macro to a custom menu command.</span></span>

## <a name="setting"></a><span data-ttu-id="4b705-110">Setting</span><span class="sxs-lookup"><span data-stu-id="4b705-110">Setting</span></span>

<span data-ttu-id="4b705-111">Действие **RunMacro** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="4b705-111">The **RunMacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b705-112">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="4b705-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4b705-113">Описание</span><span class="sxs-lookup"><span data-stu-id="4b705-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b705-114"><strong>Имя макроса</strong></span><span class="sxs-lookup"><span data-stu-id="4b705-114"><strong>Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="4b705-115">Имя запускаемого макроса.</span><span class="sxs-lookup"><span data-stu-id="4b705-115">The name of the macro to run.</span></span> <span data-ttu-id="4b705-116">В <strong>поле "Имя макроса"</strong> в разделе <strong>"Аргументы</strong> действий" области построитель макроса показаны все макросы (и группы макроса) в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="4b705-116">The <strong>Macro Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all macros (and macro groups) in the current database.</span></span> <span data-ttu-id="4b705-117">Если макрос находится в группе макроса, он будет указан под именем группы макроса в списке в качестве <em>имени макрогруппы.</em> <em>macroname</em>.</span><span class="sxs-lookup"><span data-stu-id="4b705-117">If the macro is in a macro group, it's listed under the macro group name in the list as <em>macrogroupname</em>.<em>macroname</em>.</span></span> <span data-ttu-id="4b705-118">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="4b705-118">This is a required argument.</span></span> <span data-ttu-id="4b705-119">При запуске макроса, содержащего действие <strong>RunMacro</strong> в базе данных библиотеки, Microsoft Access ищет макрос с этим именем в базе данных библиотеки и не ищет его в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="4b705-119">If you run a macro containing the <strong>RunMacro</strong> action in a library database, Microsoft Access looks for the macro with this name in the library database and doesn't look for it in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b705-120"><strong>Repeat Count</strong></span><span class="sxs-lookup"><span data-stu-id="4b705-120"><strong>Repeat Count</strong></span></span></p></td>
<td><p><span data-ttu-id="4b705-121">Максимальное количество запусков макроса.</span><span class="sxs-lookup"><span data-stu-id="4b705-121">The maximum number of times the macro will run.</span></span> <span data-ttu-id="4b705-122">Если оставить этот аргумент пустым (а аргумент <strong>repeat Expression</strong> также пустой), макрос выполняется один раз.</span><span class="sxs-lookup"><span data-stu-id="4b705-122">If you leave this argument blank (and the <strong>Repeat Expression</strong> argument is also blank), the macro runs once.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b705-123"><strong>Повторяют выражение</strong></span><span class="sxs-lookup"><span data-stu-id="4b705-123"><strong>Repeat Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="4b705-124">Выражение, которое оценивается как <strong>True</strong> (–1) или <strong>False</strong> (0).</span><span class="sxs-lookup"><span data-stu-id="4b705-124">An expression that evaluates to <strong>True</strong> (–1) or <strong>False</strong> (0).</span></span> <span data-ttu-id="4b705-125">Макрос перестает работать, если выражение оценивается как <strong>False.</strong></span><span class="sxs-lookup"><span data-stu-id="4b705-125">The macro stops running if the expression evaluates to <strong>False</strong>.</span></span> <span data-ttu-id="4b705-126">Выражение вычисляется при каждом запуске макроса.</span><span class="sxs-lookup"><span data-stu-id="4b705-126">The expression is evaluated each time the macro runs.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="4b705-127">Заметки</span><span class="sxs-lookup"><span data-stu-id="4b705-127">Remarks</span></span>

<span data-ttu-id="4b705-128">Если ввести имя группы макроса для аргумента **"Имя** макроса", Access запускает первый макрос в группе макроса.</span><span class="sxs-lookup"><span data-stu-id="4b705-128">If you enter a macro group name for the **Macro Name** argument, Access runs the first macro in the macro group.</span></span>

<span data-ttu-id="4b705-129">Это действие аналогично нажатию кнопки "Выполнить макрос" на вкладке **"Инструменты** базы данных", выбору макроса и нажатию кнопки  **"ОК".**</span><span class="sxs-lookup"><span data-stu-id="4b705-129">This action is similar to clicking **Run Macro** on the **Database Tools** tab, selecting a macro, and clicking **OK**.</span></span> <span data-ttu-id="4b705-130">Однако эта команда выполняет макрос только один раз, тогда как действие **RunMacro** может запускать макрос столько раз, сколько нужно.</span><span class="sxs-lookup"><span data-stu-id="4b705-130">However, this command runs the macro only once, whereas the **RunMacro** action can run a macro as many times as you want.</span></span>

> [!TIP]
> <span data-ttu-id="4b705-131">Вы можете использовать **аргументы Repeat Count** и **Repeat Expression,** чтобы определить, сколько раз выполняется макрос:</span><span class="sxs-lookup"><span data-stu-id="4b705-131">You can use the **Repeat Count** and **Repeat Expression** arguments to determine how many times the macro runs:</span></span>
> - <span data-ttu-id="4b705-132">Если оставить оба аргумента пустыми, макрос выполняется один раз.</span><span class="sxs-lookup"><span data-stu-id="4b705-132">If you leave both arguments blank, the macro runs once.</span></span>
> - <span data-ttu-id="4b705-133">Если ввести число для repeat **Count,** но оставить **выражение "Repeat Expression"** пустым, макрос выполняет указанное количество раз.</span><span class="sxs-lookup"><span data-stu-id="4b705-133">If you enter a number for **Repeat Count** but leave **Repeat Expression** blank, the macro runs the specified number of times.</span></span>
> - <span data-ttu-id="4b705-134">Если оставить **"Repeat Count"** пустым, но ввести выражение для **выражения "Repeat Expression",** макрос будет проходить до тех пор, пока выражение не будет равно **False.**</span><span class="sxs-lookup"><span data-stu-id="4b705-134">If you leave **Repeat Count** blank but enter an expression for **Repeat Expression**, the macro runs until the expression evaluates to **False**.</span></span>
> - <span data-ttu-id="4b705-135">Если вы вводите значения для обоих аргументов, макрос  выполняет количество  повторов или до тех пор, пока повторяемого выражения не будет оценено как **False**, в зависимости от того, что происходит в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="4b705-135">If you enter values for both arguments, the macro runs the number of times specified in **Repeat Count** or until **Repeat Expression** evaluates to **False**, whichever occurs first.</span></span>

<span data-ttu-id="4b705-136">При запуске макроса, содержащего действие **RunMacro,** и он достигает действия **RunMacro,** Access запускает называемый макрос.</span><span class="sxs-lookup"><span data-stu-id="4b705-136">When you run a macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called macro.</span></span> <span data-ttu-id="4b705-137">После завершения называемого макроса Access возвращается к исходному макросу и выполняет следующее действие.</span><span class="sxs-lookup"><span data-stu-id="4b705-137">When the called macro has finished, Access returns to the original macro and runs the next action.</span></span>

> [!NOTE]
> - <span data-ttu-id="4b705-138">Макрос можно вызывать в той же группе макроса или в другой группе макроса.</span><span class="sxs-lookup"><span data-stu-id="4b705-138">You can call a macro in the same macro group or in another macro group.</span></span>
> - <span data-ttu-id="4b705-139">Вы можете вложенные макросы.</span><span class="sxs-lookup"><span data-stu-id="4b705-139">You can nest macros.</span></span> <span data-ttu-id="4b705-140">То есть можно запустить макрос A, который, в свою очередь, вызывает макрос B и так далее.</span><span class="sxs-lookup"><span data-stu-id="4b705-140">That is, you can run macro A, which in turn calls macro B, and so on.</span></span> <span data-ttu-id="4b705-141">В каждом случае, когда называемый макрос будет завершен, Access возвращается к макросу, который его вызвал, и выполняет следующее действие в этом макросе.</span><span class="sxs-lookup"><span data-stu-id="4b705-141">In each case, when the called macro has finished, Access returns to the macro that called it and runs the next action in that macro.</span></span>

<span data-ttu-id="4b705-142">Чтобы запустить действие **RunMacro** в модуле Visual Basic для приложений (VBA), используйте метод **RunMacro** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="4b705-142">To run the **RunMacro** action in a Visual Basic for Applications (VBA) module, use the **RunMacro** method of the **DoCmd** object.</span></span>

