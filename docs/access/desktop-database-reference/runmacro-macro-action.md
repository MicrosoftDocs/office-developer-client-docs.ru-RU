---
title: Действия ЗапускМакроса макроса
TOCTitle: RunMacro Macro Action
ms:assetid: 25966f20-8160-0821-b88a-ed08b7786fdc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191868(v=office.15)
ms:contentKeyID: 48543787
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm43195
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 18e31837027f9c861480b738de5e77a0b5e2d13b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867546"
---
# <a name="runmacro-macro-action"></a><span data-ttu-id="651fc-102">Действия ЗапускМакроса макроса</span><span class="sxs-lookup"><span data-stu-id="651fc-102">RunMacro Macro Action</span></span>


<span data-ttu-id="651fc-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="651fc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="651fc-104">**ЗапускМакроса** можно использовать для запуска макроса.</span><span class="sxs-lookup"><span data-stu-id="651fc-104">You can use the **RunMacro** action to run a macro.</span></span> <span data-ttu-id="651fc-105">Макрос может входить в группу макросов.</span><span class="sxs-lookup"><span data-stu-id="651fc-105">The macro can be in a macro group.</span></span>

<span data-ttu-id="651fc-106">Это действие можно использовать:</span><span class="sxs-lookup"><span data-stu-id="651fc-106">You can use this action:</span></span>

  - <span data-ttu-id="651fc-107">Чтобы запустить макрос из другого макроса.</span><span class="sxs-lookup"><span data-stu-id="651fc-107">To run a macro from within another macro.</span></span>

  - <span data-ttu-id="651fc-108">Чтобы запустить макрос при выполнении определенного условия.</span><span class="sxs-lookup"><span data-stu-id="651fc-108">To run a macro based on a certain condition.</span></span>

  - <span data-ttu-id="651fc-109">Связывание макроса на настраиваемом меню команду.</span><span class="sxs-lookup"><span data-stu-id="651fc-109">To attach a macro to a custom menu command.</span></span>

## <a name="setting"></a><span data-ttu-id="651fc-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="651fc-110">Setting</span></span>

<span data-ttu-id="651fc-111">**ЗапускМакроса** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="651fc-111">The **RunMacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="651fc-112">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="651fc-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="651fc-113">Описание</span><span class="sxs-lookup"><span data-stu-id="651fc-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="651fc-114"><strong>Имя макроса</strong></span><span class="sxs-lookup"><span data-stu-id="651fc-114"><strong>Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="651fc-115">Имя макроса для запуска.</span><span class="sxs-lookup"><span data-stu-id="651fc-115">The name of the macro to run.</span></span> <span data-ttu-id="651fc-116">В поле <strong>Имя макроса</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов показывает все макросы (и группы макросов) в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="651fc-116">The <strong>Macro Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all macros (and macro groups) in the current database.</span></span> <span data-ttu-id="651fc-117">Если макрос находится в группе макросов, оно указано в разделе имя группы в списке как <em>ИмяГруппыМакросов</em>. <em>имяМакроса</em>.</span><span class="sxs-lookup"><span data-stu-id="651fc-117">If the macro is in a macro group, it's listed under the macro group name in the list as <em>macrogroupname</em>.<em>macroname</em>.</span></span> <span data-ttu-id="651fc-118">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="651fc-118">This is a required argument.</span></span> <span data-ttu-id="651fc-119">Если макрос, содержащий <strong>ЗапускМакроса в базе данных библиотеки</strong> , Microsoft Access выполняет поиск макроса с этим именем в базе данных библиотеки и не проводит поиск в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="651fc-119">If you run a macro containing the <strong>RunMacro</strong> action in a library database, Microsoft Access looks for the macro with this name in the library database and doesn't look for it in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="651fc-120"><strong>Число повторов</strong></span><span class="sxs-lookup"><span data-stu-id="651fc-120"><strong>Repeat Count</strong></span></span></p></td>
<td><p><span data-ttu-id="651fc-121">Максимальное количество попыток запуска макроса.</span><span class="sxs-lookup"><span data-stu-id="651fc-121">The maximum number of times the macro will run.</span></span> <span data-ttu-id="651fc-122">Если оставить этот аргумент пустым (и <strong>Повторите выражения</strong> -аргумента также не задан), макрос выполняется один раз.</span><span class="sxs-lookup"><span data-stu-id="651fc-122">If you leave this argument blank (and the <strong>Repeat Expression</strong> argument is also blank), the macro runs once.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="651fc-123"><strong>Повторите выражение</strong></span><span class="sxs-lookup"><span data-stu-id="651fc-123"><strong>Repeat Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="651fc-124">Выражение, которое оценивается как <strong>значение True</strong> (– 1) или <strong>False</strong> (0).</span><span class="sxs-lookup"><span data-stu-id="651fc-124">An expression that evaluates to <strong>True</strong> (–1) or <strong>False</strong> (0).</span></span> <span data-ttu-id="651fc-125">Выполнение макроса останавливается, если выражение имеет значение <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="651fc-125">The macro stops running if the expression evaluates to <strong>False</strong>.</span></span> <span data-ttu-id="651fc-126">Выражение каждый раз при выполнении макроса.</span><span class="sxs-lookup"><span data-stu-id="651fc-126">The expression is evaluated each time the macro runs.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="651fc-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="651fc-127">Remarks</span></span>

<span data-ttu-id="651fc-128">Если ввести имя группы макросов для аргумента **Имя макроса** доступа запуска первого макроса в группе макросов.</span><span class="sxs-lookup"><span data-stu-id="651fc-128">If you enter a macro group name for the **Macro Name** argument, Access runs the first macro in the macro group.</span></span>

<span data-ttu-id="651fc-129">Это действие аналогично выберите **Выполнить макрос** на вкладке **Инструменты для баз данных** , выберите макрос и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="651fc-129">This action is similar to clicking **Run Macro** on the **Database Tools** tab, selecting a macro, and clicking **OK**.</span></span> <span data-ttu-id="651fc-130">Тем не менее эта команда выполняется макрос только один раз, тогда как макрос можно запустить **ЗапускМакроса** столько раз.</span><span class="sxs-lookup"><span data-stu-id="651fc-130">However, this command runs the macro only once, whereas the **RunMacro** action can run a macro as many times as you want.</span></span>


> [!TIP]
> <P><span data-ttu-id="651fc-131">Чтобы определить, сколько раз запускает макрос можно использовать <STRONG>Число повторов</STRONG> и <STRONG>повторите выражение</STRONG> аргументы:</span><span class="sxs-lookup"><span data-stu-id="651fc-131">You can use the <STRONG>Repeat Count</STRONG> and <STRONG>Repeat Expression</STRONG> arguments to determine how many times the macro runs:</span></span></P>



  - <span data-ttu-id="651fc-132">Если оба аргумента оставлено пустым, макрос выполняется один раз.</span><span class="sxs-lookup"><span data-stu-id="651fc-132">If you leave both arguments blank, the macro runs once.</span></span>

  - <span data-ttu-id="651fc-133">Если ввести номер **Число повторов** , но оставить пустым **Повторите выражение** , макрос выполняется указанное число раз.</span><span class="sxs-lookup"><span data-stu-id="651fc-133">If you enter a number for **Repeat Count** but leave **Repeat Expression** blank, the macro runs the specified number of times.</span></span>

  - <span data-ttu-id="651fc-134">Если оставить пустым **Число повторов** , но введите выражение для **Повторите выражение**, макрос выполняется только после вычисление выражения дает значение **False**.</span><span class="sxs-lookup"><span data-stu-id="651fc-134">If you leave **Repeat Count** blank but enter an expression for **Repeat Expression**, the macro runs until the expression evaluates to **False**.</span></span>

  - <span data-ttu-id="651fc-135">При вводе значения обоих аргументов, запускается макрос количество времени, указанного в **Число повторов** или пока **Условие повтора** вычисляющий значение **False**, что происходит первым.</span><span class="sxs-lookup"><span data-stu-id="651fc-135">If you enter values for both arguments, the macro runs the number of times specified in **Repeat Count** or until **Repeat Expression** evaluates to **False**, whichever occurs first.</span></span>

<span data-ttu-id="651fc-136">Если макрос, содержащий **ЗапускМакроса** достигает **ЗапускМакроса** , Access запускает макрос называемое.</span><span class="sxs-lookup"><span data-stu-id="651fc-136">When you run a macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called macro.</span></span> <span data-ttu-id="651fc-137">По завершении вызванного макроса доступа возвращает исходное макрос и выполняется следующее действие.</span><span class="sxs-lookup"><span data-stu-id="651fc-137">When the called macro has finished, Access returns to the original macro and runs the next action.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="651fc-138">Можно вызвать макроса в той же группе макросов или в другой группы макросов.</span><span class="sxs-lookup"><span data-stu-id="651fc-138">You can call a macro in the same macro group or in another macro group.</span></span></P>
> <LI>
> <P><span data-ttu-id="651fc-139">Можно вкладывать макросов.</span><span class="sxs-lookup"><span data-stu-id="651fc-139">You can nest macros.</span></span> <span data-ttu-id="651fc-140">То есть можно запустить макрос A, которая, в свою очередь вызывает макрос B и т. д.</span><span class="sxs-lookup"><span data-stu-id="651fc-140">That is, you can run macro A, which in turn calls macro B, and so on.</span></span> <span data-ttu-id="651fc-141">По завершении вызванного макроса в каждом случае доступа возвращает макрос, который вызвал ее и выполняется следующее действие в этот макрос.</span><span class="sxs-lookup"><span data-stu-id="651fc-141">In each case, when the called macro has finished, Access returns to the macro that called it and runs the next action in that macro.</span></span></P></LI></UL>



<span data-ttu-id="651fc-142">Чтобы запустить **ЗапускМакроса** в Visual Basic для приложений (VBA) модуль, используйте метод **RunMacro** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="651fc-142">To run the **RunMacro** action in a Visual Basic for Applications (VBA) module, use the **RunMacro** method of the **DoCmd** object.</span></span>

