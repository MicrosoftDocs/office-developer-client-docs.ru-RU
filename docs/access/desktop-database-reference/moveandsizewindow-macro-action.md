---
title: Макрокоманда MoveAndSizeWindow
TOCTitle: MoveAndSizeWindow macro action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1b127995a2f9a0af7da80e9df862259b570870e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288808"
---
# <a name="moveandsizewindow-macro-action"></a><span data-ttu-id="aa10c-102">Макрокоманда MoveAndSizeWindow</span><span class="sxs-lookup"><span data-stu-id="aa10c-102">MoveAndSizeWindow macro action</span></span>

<span data-ttu-id="aa10c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa10c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aa10c-104">Если параметры окна документа настроены на использование перекрывающихся окон вместо документов с вкладками, можно использовать действие **MoveAndSizeWindow** для перемещения или настройки активного окна.</span><span class="sxs-lookup"><span data-stu-id="aa10c-104">If you have set your document window options to use overlapping windows instead of tabbed documents, you can use the **MoveAndSizeWindow** action to move or resize the active window.</span></span> <span data-ttu-id="aa10c-105">Сведения о том, как настроить параметры окна документа, см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="aa10c-105">For information on how to set document window options, see the Remarks section.</span></span>

## <a name="setting"></a><span data-ttu-id="aa10c-106">Setting</span><span class="sxs-lookup"><span data-stu-id="aa10c-106">Setting</span></span>

<span data-ttu-id="aa10c-107">Действие **MoveAndSizeWindow** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="aa10c-107">The **MoveAndSizeWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aa10c-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="aa10c-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="aa10c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="aa10c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa10c-110"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="aa10c-110"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="aa10c-111">Новое горизонтальное положение левого верхнего угла окна, измеряемого от левого края окна, содержащего его.</span><span class="sxs-lookup"><span data-stu-id="aa10c-111">The new horizontal position of the window's upper-left corner, measured from the left edge of its containing window.</span></span> <span data-ttu-id="aa10c-112">Введите положение в правом <strong>поле</strong> в разделе <strong>"Аргументы действий"</strong> области построитель макроса.</span><span class="sxs-lookup"><span data-stu-id="aa10c-112">Enter the position in the <strong>Right</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa10c-113"><strong>Вниз</strong></span><span class="sxs-lookup"><span data-stu-id="aa10c-113"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="aa10c-114">Новое вертикальное положение левого верхнего угла окна, измеряемого от верхнего края окна, содержащего его.</span><span class="sxs-lookup"><span data-stu-id="aa10c-114">The new vertical position of the window's upper-left corner, measured from the top edge of its containing window.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa10c-115"><strong>Width</strong></span><span class="sxs-lookup"><span data-stu-id="aa10c-115"><strong>Width</strong></span></span></p></td>
<td><p><span data-ttu-id="aa10c-116">Новая ширина окна.</span><span class="sxs-lookup"><span data-stu-id="aa10c-116">The window's new width.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa10c-117"><strong>Height</strong></span><span class="sxs-lookup"><span data-stu-id="aa10c-117"><strong>Height</strong></span></span></p></td>
<td><p><span data-ttu-id="aa10c-118">Новая высота окна.</span><span class="sxs-lookup"><span data-stu-id="aa10c-118">The window's new height.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa10c-119">Если оставить аргумент пустым, Microsoft Access использует текущий параметр окна.</span><span class="sxs-lookup"><span data-stu-id="aa10c-119">If you leave an argument blank, Microsoft Access uses the window's current setting.</span></span>

<span data-ttu-id="aa10c-120">Необходимо ввести значение по крайней мере для одного аргумента.</span><span class="sxs-lookup"><span data-stu-id="aa10c-120">You must enter a value for at least one argument.</span></span>

> [!NOTE]
> <span data-ttu-id="aa10c-121">Размер каждого измерения зависит от региональных параметров панели управления Windows в дюймах или см.</span><span class="sxs-lookup"><span data-stu-id="aa10c-121">Each measurement is in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa10c-122">Заметки</span><span class="sxs-lookup"><span data-stu-id="aa10c-122">Remarks</span></span>

<span data-ttu-id="aa10c-123">Чтобы настроить приложение для использования перекрывающихся окон вместо документов с вкладками, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="aa10c-123">To set up an application to use overlapping windows instead of tabbed documents, use the following procedure:</span></span>

1.  <span data-ttu-id="aa10c-124">Параметры **щелчка**</span><span class="sxs-lookup"><span data-stu-id="aa10c-124">Click **Options**</span></span>

2.  <span data-ttu-id="aa10c-125">Щелкните **"Текущая база данных".**</span><span class="sxs-lookup"><span data-stu-id="aa10c-125">Click **Current Database**.</span></span>

3.  <span data-ttu-id="aa10c-126">В разделе **"Параметры приложения"** в разделе **"Параметры окна документа"** щелкните **"Перекрывающиеся окна Windows".**</span><span class="sxs-lookup"><span data-stu-id="aa10c-126">In the **Application Options** section, under **Document Window Options**, click **Overlapping Windows**.</span></span>

4.  <span data-ttu-id="aa10c-127">Нажмите **кнопку "ОК",** а затем закроем и снова откроете базу данных.</span><span class="sxs-lookup"><span data-stu-id="aa10c-127">Click **OK**, and then close and reopen the database.</span></span>

<span data-ttu-id="aa10c-128">Это действие аналогично нажатию кнопки **"Переместить"** или **"Размер"** в меню **"Управление" окна.**</span><span class="sxs-lookup"><span data-stu-id="aa10c-128">This action is similar to clicking **Move** or **Size** on the window's **Control** menu.</span></span> <span data-ttu-id="aa10c-129">С помощью команд меню можно использовать клавиши со стрелками клавиатуры для перемещения или настройки окна.</span><span class="sxs-lookup"><span data-stu-id="aa10c-129">With the menu commands, you use the keyboard's arrow keys to move or resize the window.</span></span> <span data-ttu-id="aa10c-130">С помощью **действия MoveAndSizeWindow** вы вводите измерения положения и размера напрямую.</span><span class="sxs-lookup"><span data-stu-id="aa10c-130">With the **MoveAndSizeWindow** action, you enter the position and size measurements directly.</span></span> <span data-ttu-id="aa10c-131">Вы также можете использовать мышь для перемещения и размера окон.</span><span class="sxs-lookup"><span data-stu-id="aa10c-131">You can also use the mouse to move and size windows.</span></span>

<span data-ttu-id="aa10c-132">Это действие можно использовать в любом окне, в любом представлении.</span><span class="sxs-lookup"><span data-stu-id="aa10c-132">You can use this action on any window, in any view.</span></span>

> [!TIP]
> - <span data-ttu-id="aa10c-133">Чтобы переместить окно без его размеров, введите  значения для аргументов **"Право"** и "Вниз", но оставьте аргументы **Width** и **Height** пустыми.</span><span class="sxs-lookup"><span data-stu-id="aa10c-133">To move a window without resizing it, enter values for the **Right** and **Down** arguments but leave the **Width** and **Height** arguments blank.</span></span>
> - <span data-ttu-id="aa10c-134">Чтобы не перемещать окно, введите значения аргументов **Width** и **Height,** но оставьте аргументы **Right** и **Down** пустыми.</span><span class="sxs-lookup"><span data-stu-id="aa10c-134">To resize a window without moving it, enter values for the **Width** and **Height** arguments but leave the **Right** and **Down** arguments blank.</span></span>

<span data-ttu-id="aa10c-135">Чтобы запустить действие **MoveAndSizeWindow** в модуле Visual Basic для приложений (VBA), используйте метод **MoveSize** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="aa10c-135">To run the **MoveAndSizeWindow** action in a Visual Basic for Applications (VBA) module, use the **MoveSize** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="aa10c-136">Пример</span><span class="sxs-lookup"><span data-stu-id="aa10c-136">Example</span></span>

<span data-ttu-id="aa10c-137">**Синхронизация форм с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="aa10c-137">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="aa10c-138">Следующий макрос открывает форму "Список продуктов" в правом нижнем углу формы "Поставщики", отображая продукты текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="aa10c-138">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="aa10c-139">Здесь показано использование действий **Echo,** **MessageBox,** **GoToControl,** **StopMacro,** **OpenForm** и **MoveAndSizeWindow.**</span><span class="sxs-lookup"><span data-stu-id="aa10c-139">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="aa10c-140">Здесь также показано использование условного выражения с действиями **MessageBox,** **GoToControl** и **StopMacro.**</span><span class="sxs-lookup"><span data-stu-id="aa10c-140">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="aa10c-141">Этот макрос следует прикрепить к кнопке "Обзор продуктов" в форме "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="aa10c-141">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aa10c-142">Condition</span><span class="sxs-lookup"><span data-stu-id="aa10c-142">Condition</span></span></p></th>
<th><p><span data-ttu-id="aa10c-143">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="aa10c-143">Action</span></span></p></th>
<th><p><span data-ttu-id="aa10c-144">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="aa10c-144">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="aa10c-145">Примечание</span><span class="sxs-lookup"><span data-stu-id="aa10c-145">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="aa10c-146"><strong>ВыводНаЭкран</strong></span><span class="sxs-lookup"><span data-stu-id="aa10c-146"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="aa10c-147"><strong>Включить вывод</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="aa10c-147"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="aa10c-148">Приостанавливает обновление экрана, пока выполняется макрос.</span><span class="sxs-lookup"><span data-stu-id="aa10c-148">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa10c-149">IsNull([ИД поставщика])</span><span class="sxs-lookup"><span data-stu-id="aa10c-149">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="aa10c-150"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="aa10c-150"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="aa10c-151"><strong>Сообщение:</strong>перейдите к записи поставщика, продукты которой вы хотите просмотреть, а затем снова нажмите кнопку "Просмотреть продукты".</span><span class="sxs-lookup"><span data-stu-id="aa10c-151"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="aa10c-152"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span><span class="sxs-lookup"><span data-stu-id="aa10c-152"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="aa10c-153">Если в форме "Поставщики" нет текущего поставщика, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="aa10c-153">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="aa10c-154"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="aa10c-154"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="aa10c-155"><strong>Имя управления</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="aa10c-155"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="aa10c-156">Переместите фокус на управление CompanyName.</span><span class="sxs-lookup"><span data-stu-id="aa10c-156">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa10c-157">...</span><span class="sxs-lookup"><span data-stu-id="aa10c-157">...</span></span></p></td>
<td><p><span data-ttu-id="aa10c-158"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="aa10c-158"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="aa10c-159">Остановите макрос.</span><span class="sxs-lookup"><span data-stu-id="aa10c-159">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="aa10c-160"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="aa10c-160"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="aa10c-161"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]! [Поставщики]! [SupplierID] <strong>Режим данных:</strong> <strong>режим только чтенияWindow</strong>: <strong>обычный</strong></span><span class="sxs-lookup"><span data-stu-id="aa10c-161"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="aa10c-162">Откройте форму "Список продуктов" и откажите продукты текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="aa10c-162">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="aa10c-163"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="aa10c-163"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="aa10c-164"><strong>Right</strong>: 0.7799 &quot; <strong>Down</strong>: 1.8&quot;</span><span class="sxs-lookup"><span data-stu-id="aa10c-164"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="aa10c-165">Расположить форму "Список продуктов" в правом нижнем правом месте формы "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="aa10c-165">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

