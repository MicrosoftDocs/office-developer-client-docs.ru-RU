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
# <a name="moveandsizewindow-macro-action"></a><span data-ttu-id="697c9-102">Макрокоманда MoveAndSizeWindow</span><span class="sxs-lookup"><span data-stu-id="697c9-102">MoveAndSizeWindow macro action</span></span>

<span data-ttu-id="697c9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="697c9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="697c9-104">Если вы настроили параметры окна документов для использования перекрывающихся окон вместо вкладки документов, вы можете использовать действие **MoveAndSizeWindow** для перемещения или повторного использования активного окна.</span><span class="sxs-lookup"><span data-stu-id="697c9-104">If you have set your document window options to use overlapping windows instead of tabbed documents, you can use the **MoveAndSizeWindow** action to move or resize the active window.</span></span> <span data-ttu-id="697c9-105">Сведения о том, как установить параметры окна документов, см. в разделе Примечание.</span><span class="sxs-lookup"><span data-stu-id="697c9-105">For information on how to set document window options, see the Remarks section.</span></span>

## <a name="setting"></a><span data-ttu-id="697c9-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="697c9-106">Setting</span></span>

<span data-ttu-id="697c9-107">Действие **MoveAndSizeWindow** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="697c9-107">The **MoveAndSizeWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="697c9-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="697c9-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="697c9-109">Описание</span><span class="sxs-lookup"><span data-stu-id="697c9-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="697c9-110"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="697c9-110"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="697c9-111">Новое горизонтальное положение верхнего левого угла окна, измеряемого с левого края его содержащего окна.</span><span class="sxs-lookup"><span data-stu-id="697c9-111">The new horizontal position of the window's upper-left corner, measured from the left edge of its containing window.</span></span> <span data-ttu-id="697c9-112">Введите позицию в <strong>правом</strong> окне в разделе <strong>Аргументы</strong> действий в области Macro Builder.</span><span class="sxs-lookup"><span data-stu-id="697c9-112">Enter the position in the <strong>Right</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="697c9-113"><strong>Down</strong></span><span class="sxs-lookup"><span data-stu-id="697c9-113"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="697c9-114">Новое вертикальное положение верхнего левого угла окна, измеряемого с верхнего края его содержащего окна.</span><span class="sxs-lookup"><span data-stu-id="697c9-114">The new vertical position of the window's upper-left corner, measured from the top edge of its containing window.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="697c9-115"><strong>Width</strong></span><span class="sxs-lookup"><span data-stu-id="697c9-115"><strong>Width</strong></span></span></p></td>
<td><p><span data-ttu-id="697c9-116">Новая ширина окна.</span><span class="sxs-lookup"><span data-stu-id="697c9-116">The window's new width.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="697c9-117"><strong>Height</strong></span><span class="sxs-lookup"><span data-stu-id="697c9-117"><strong>Height</strong></span></span></p></td>
<td><p><span data-ttu-id="697c9-118">Новая высота окна.</span><span class="sxs-lookup"><span data-stu-id="697c9-118">The window's new height.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="697c9-119">Если оставить аргумент пустым, Microsoft Access использует текущий параметр окна.</span><span class="sxs-lookup"><span data-stu-id="697c9-119">If you leave an argument blank, Microsoft Access uses the window's current setting.</span></span>

<span data-ttu-id="697c9-120">Необходимо ввести значение по крайней мере для одного аргумента.</span><span class="sxs-lookup"><span data-stu-id="697c9-120">You must enter a value for at least one argument.</span></span>

> [!NOTE]
> <span data-ttu-id="697c9-121">Каждое измерение находится в дюймах или сантиметрах в зависимости от региональных параметров Windows панели управления.</span><span class="sxs-lookup"><span data-stu-id="697c9-121">Each measurement is in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span>

## <a name="remarks"></a><span data-ttu-id="697c9-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="697c9-122">Remarks</span></span>

<span data-ttu-id="697c9-123">Чтобы настроить приложение для использования перекрывающихся окон вместо вкладки документов, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="697c9-123">To set up an application to use overlapping windows instead of tabbed documents, use the following procedure:</span></span>

1.  <span data-ttu-id="697c9-124">Щелкните **Параметры**</span><span class="sxs-lookup"><span data-stu-id="697c9-124">Click **Options**</span></span>

2.  <span data-ttu-id="697c9-125">Щелкните **текущую базу данных**.</span><span class="sxs-lookup"><span data-stu-id="697c9-125">Click **Current Database**.</span></span>

3.  <span data-ttu-id="697c9-126">В разделе **Параметры приложений** в **разделе Параметры окна документов** нажмите **кнопку Перекрытие Windows**.</span><span class="sxs-lookup"><span data-stu-id="697c9-126">In the **Application Options** section, under **Document Window Options**, click **Overlapping Windows**.</span></span>

4.  <span data-ttu-id="697c9-127">Нажмите **кнопку ОК,** а затем закрыть и открыть базу данных.</span><span class="sxs-lookup"><span data-stu-id="697c9-127">Click **OK**, and then close and reopen the database.</span></span>

<span data-ttu-id="697c9-128">Это действие аналогично нажатию **кнопки Move** или **Size** в меню **"Управление** окном".</span><span class="sxs-lookup"><span data-stu-id="697c9-128">This action is similar to clicking **Move** or **Size** on the window's **Control** menu.</span></span> <span data-ttu-id="697c9-129">В командах меню для перемещения или повторного использования окна используются клавиши со стрелками клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="697c9-129">With the menu commands, you use the keyboard's arrow keys to move or resize the window.</span></span> <span data-ttu-id="697c9-130">С помощью **действия MoveAndSizeWindow** вы вводите измерения положения и размера напрямую.</span><span class="sxs-lookup"><span data-stu-id="697c9-130">With the **MoveAndSizeWindow** action, you enter the position and size measurements directly.</span></span> <span data-ttu-id="697c9-131">Вы также можете использовать мышь для перемещения и размера окон.</span><span class="sxs-lookup"><span data-stu-id="697c9-131">You can also use the mouse to move and size windows.</span></span>

<span data-ttu-id="697c9-132">Это действие можно использовать в любом окне, в любом представлении.</span><span class="sxs-lookup"><span data-stu-id="697c9-132">You can use this action on any window, in any view.</span></span>

> [!TIP]
> - <span data-ttu-id="697c9-133">Чтобы переместить окно без его повторного использования, введите значения аргументов **"Право"** и "Вниз", но оставьте аргументы **Ширина** и Высота пустыми.  </span><span class="sxs-lookup"><span data-stu-id="697c9-133">To move a window without resizing it, enter values for the **Right** and **Down** arguments but leave the **Width** and **Height** arguments blank.</span></span>
> - <span data-ttu-id="697c9-134">Чтобы повторное значение окна не перемещалось, введите  значения для аргументов **Ширина** и Высота, но оставьте аргументы **Right** and **Down** пустыми.</span><span class="sxs-lookup"><span data-stu-id="697c9-134">To resize a window without moving it, enter values for the **Width** and **Height** arguments but leave the **Right** and **Down** arguments blank.</span></span>

<span data-ttu-id="697c9-135">Чтобы выполнить действие **MoveAndSizeWindow** в модуле Visual Basic для приложений (VBA), используйте метод **MoveSize** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="697c9-135">To run the **MoveAndSizeWindow** action in a Visual Basic for Applications (VBA) module, use the **MoveSize** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="697c9-136">Пример</span><span class="sxs-lookup"><span data-stu-id="697c9-136">Example</span></span>

<span data-ttu-id="697c9-137">**Синхронизация форм с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="697c9-137">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="697c9-138">Следующий макрос открывает форму Списка продуктов в нижнем правом углу формы Поставщики, отображая продукты текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="697c9-138">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="697c9-139">В нем показано использование действий **Echo,** **MessageBox,** **GoToControl,** **StopMacro,** **OpenForm** и **MoveAndSizeWindow.**</span><span class="sxs-lookup"><span data-stu-id="697c9-139">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="697c9-140">В нем также показано использование условного выражения с **действиями MessageBox,** **GoToControl** и **StopMacro.**</span><span class="sxs-lookup"><span data-stu-id="697c9-140">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="697c9-141">Этот макрос следует прикрепить к кнопке Review Products в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="697c9-141">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="697c9-142">Условие</span><span class="sxs-lookup"><span data-stu-id="697c9-142">Condition</span></span></p></th>
<th><p><span data-ttu-id="697c9-143">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="697c9-143">Action</span></span></p></th>
<th><p><span data-ttu-id="697c9-144">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="697c9-144">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="697c9-145">Примечание</span><span class="sxs-lookup"><span data-stu-id="697c9-145">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="697c9-146"><strong>ВыводНаЭкран</strong></span><span class="sxs-lookup"><span data-stu-id="697c9-146"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="697c9-147"><strong>Включить вывод</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="697c9-147"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="697c9-148">Приостанавливает обновление экрана, пока выполняется макрос.</span><span class="sxs-lookup"><span data-stu-id="697c9-148">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="697c9-149">IsNull([Поставщик ID])</span><span class="sxs-lookup"><span data-stu-id="697c9-149">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="697c9-150"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="697c9-150"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="697c9-151"><strong>Сообщение.</strong>Перейдите к записи поставщика, продукты которого вы хотите видеть, а затем нажмите кнопку Обзор продуктов снова.</span><span class="sxs-lookup"><span data-stu-id="697c9-151"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="697c9-152"><strong>Звуковой сигнал</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Выберите поставщика</span><span class="sxs-lookup"><span data-stu-id="697c9-152"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="697c9-153">Если в форме Поставщики нет текущего поставщика, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="697c9-153">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="697c9-154"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="697c9-154"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="697c9-155"><strong>Имя управления:</strong>CompanyName</span><span class="sxs-lookup"><span data-stu-id="697c9-155"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="697c9-156">Переместите фокус на управление CompanyName.</span><span class="sxs-lookup"><span data-stu-id="697c9-156">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="697c9-157">...</span><span class="sxs-lookup"><span data-stu-id="697c9-157">...</span></span></p></td>
<td><p><span data-ttu-id="697c9-158"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="697c9-158"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="697c9-159">Остановите макрос.</span><span class="sxs-lookup"><span data-stu-id="697c9-159">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="697c9-160"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="697c9-160"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="697c9-161"><strong>Имя формы</strong>: Представление списка <strong>продуктов:</strong> <strong>Имя DatasheetFilter</strong>: Where <strong>Condition</strong>: [Supplier ID] = [Forms]! [Поставщики]! [SupplierID] <strong>Режим данных:</strong> <strong>Режим чтения OnlyWindow</strong>: <strong>Нормальный</strong></span><span class="sxs-lookup"><span data-stu-id="697c9-161"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="697c9-162">Откройте форму списка продуктов и покажите продукты текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="697c9-162">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="697c9-163"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="697c9-163"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="697c9-164"><strong>Справа</strong>: 0.7799 &quot; <strong>Вниз</strong>: 1.8&quot;</span><span class="sxs-lookup"><span data-stu-id="697c9-164"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="697c9-165">Расположить форму списка продуктов в нижнем праве формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="697c9-165">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

